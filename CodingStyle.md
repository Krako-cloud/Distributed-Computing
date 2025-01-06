CodingStyle
David Anderson edited this page on Aug 21, 2024 · 4 revisions
Software and information architecture
Since I first wrote it in 2002, BOINC has evolved continuously and fairly smoothly. It's now an extremely powerful system, but its code size is fairly small, and the code is malleable (easy to change and extend). I don't see any barriers to BOINC's continued evolution.

This success is due in large part to BOINC's architecture. I'll try to articulate some of the principles behind this architecture.

Simplicity and brevity
The most important principle is: make the code as simple as possible.

To a large extent, shorter is simpler. So:

Given two possible implementation, use the shorter one.
If you're writing something new, and it needs a function that might be of general utility, check whether it already exists (in lib/ or html/inc) rather than writing it yourself.
If code is repeated, factor it out and make it into a function. Don't copy and paste code.
Related principles:

If you're adding a new mechanism, try to make it more general than the immediate need, without making it more complicated.
If a function becomes longer than 100 lines or so, split it up.
If a file is becoming too big, or has a bunch of unrelated stuff, split it up.
Uniformity
Imitate the style and structure of the code that's already there, even if you don't like it.

Data architecture
BOINC stores information in various forms. Guidelines:

MySQL database: The DB server is a potential performance bottleneck, and there is a code overhead for DB tables (you need to write interface functions in C++ and/or PHP, and you need to write web pages or scripts for editing data). So use the DB only when it's necessary (e.g. because you need indices for large data) and avoid creating new tables. Don't use referential constraints; instead, check for lookups returning null.
XML fields in DB tables: Simplify DB design by storing information in XML in DB fields (for example, computing preferences and job file lists). This can eliminate the need for separate tables.
XML files: BOINC uses XML format both for internal state (e.g. client_state.xml) and configuration files (cc_config.xml on the client, project.xml on the server). Sometimes we use enclosing tags for multiple items (e.g. <tasks> in project.xml); sometimes we don't. Either is fine - imitate what's already there.
PHP and/or C++ code: If data is used only in PHP, put it in a PHP data structure. You can assume that project admins are able to edit these (e.g. html/project/project.inc).
Avoid over-engineering
If you make a big change to solve a problem that never actually arises, that's over-engineering. Avoid it.

There are various things (HTTP headers, message boards, XML parsing) where we've had to choose between using someone else's library or doing it ourselves. There are always tradeoffs. If we have something that works and is stable (e.g. XML parsing), leave it.

In general, big changes should be undertaken only if it's certain that there's going to be a big reward. Big changes introduce bugs, and end up costing more than you think. One exception: occasionally I'll make a change whose only effect is to shorten or simplify the code.

Coding style
All languages
Error codes
Most functions should return an integer error code. Nonzero means error. See lib/error_numbers.h for a list of error codes. Exceptions:

PHP database access functions, which use the mysql_* convention that zero means error, and you call mysql_error() or mysql_error_string() to find details.
Functions that return whether a condition holds; such functions should have descriptive names like is_job_finished().
Functions that return a number or other type, and for which no errors are possible.
Calls to functions that return an error code should check the code. Generally they should return non-zero on error, e.g.:

retval = blah();
if (retval) return retval;
Code documentation
All files have a comment at the top saying what's in the file (and perhaps what isn't).
Functions are preceded by a comment saying what they do.
structs and classes are preceded by a comment saying what they represent.
Naming
Names should be descriptive without being verbose (local variables names may be short).
Class and type names, and #defined symbols, are all upper case, with underscores to separate words.
Variable and function names are all lower case, with underscores to separate words.
No mixed case names.
Indentation
Each level of indentation is 4 spaces (not a tab).
Multi-line function call:
func(
    blah, blah, blah, blah, blah,
    blah, blah, blah, blah, blah
);
switch statements: case labels are at same indent level as switch
switch (foo) {
case 1:
    ...
    break;
case 2:
    ...
    break;
}
Constants
There should be few numeric constants in code. Generally they should be #defines.
Braces (C++ and PHP)
Opening curly brace goes at end of line (not next line):
if (foobar) {
    ...
} else if (blah) {
    ...
} else {
    ...
}
Always use curly braces on multi-line if statements.
if (foo)
    return blah;     // WRONG
1-line if() statements are OK:
if (foo) return blah;
Comments and #ifdefs
For C++ and PHP, use // for all comments.
End multi-line comments with an empty comment line, e.g.
// This function does blah blah
// Call it when blah blah
//
function foo() {
}
C++ specific
C++ .h files often contain both interface and implementation. Clearly divide these.
Includes
A .cpp file should have the minimum set of #includes to get that particular file to compile (e.g. the includes needed by foo.cpp should be in foo.cpp, not foo.h).
For readability, includes should be ordered from general (<stdio.h>) to specific (foo.h). However, this order shouldn't matter.
Extern declarations
foo.h should have extern declarations for all public functions and variables in foo.cpp. There should be no extern statements in .cpp files.
Use of static
If a function or variable is used in only one file, declare it static.
Things to avoid unless there's a compelling reason:
Operator and function overloading.
Templates.
Stream I/O; use printf() and scanf().
Things to avoid
Use typedef (not #define) to define types.
Don't use memset() or memcpy() to initialize or copy classes that are non-C compatible. Write a default constructor and a copy constructor instead.
Dynamic memory allocation. Functions shouldn't return pointers to malloc'd items.
Structure definitions
struct FOO {
    ...
};
You can then declare variables as:

FOO x;
Comments
Comment out blocks of code as follows:

#if 0
    ...
#endif
PHP specific
HTML
PHP scripts should output "HTML 4.01 Transitional". The HTML should pass the W3C validator. This means, e.g., you must have quotes around attributes that have non-alpha characters in them. However, all-alpha attributes need not have quotes, and tags like <br> and <p> need not be closed.

The HTML need not be XHTML.

This means no self-closing tags like <br />.

Getting POST and GET data
Do not access $_POST or $_GET directly. Use get_int(), get_str(), post_int() and post_str() (from util.inc) to get POST and GET data. These undo the effects of PHP magic quotes.

Database access
Use the database abstraction layer.
If a POST or GET value will be used in a database query, use BoincDb::escape_string to escape it.
