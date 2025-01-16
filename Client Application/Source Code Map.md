## Client-side software

1. Client
1. Manager (desktop GUI)
1. Screensaver (Win/Mac/Linux)
1. App API (linked with applications)
1. Wrappers (wrapper, vboxwrapper)
1. Demo applications
1. boinctray (Windows program to detect user input)


##Server-side software

1. CGI programs (scheduler, file upload handler)
1. Daemons (feeder, validators, assimilators)
1. Command-line tools (job submission, file management)
1. Web (user and admin web sites; RPC handlers)


##Source code tree map

1. Directory:	Contents
1. android:	the Android GUI (java, kotlin)
1. api:	the App API
1. apps:	demo applications
1. client:	the client (C++)
1. clientgui:	the Manager
1. clienscr:	the screensaver
1. clientsetup/win:	C++ 'custom actions' for Win installer
1. clienttray:	boinctray
1. db:	database schema and C++ access library (used by all server programs)
1. html/inc:	utility functions for web interfaces
1. html/ops:	admin web interface
1. html/project.sample:	sample project web configuration files
1. html/user:	public web interface
1. lib:	utility functions used by all C++ code
1. mac_build:	scripts for building the Mac client software
1. mac_installer:	scripts and C++ code for building Mac installers
1. py/Boinc:	scripts for project creation and control
1. samples/vbox_wrapper:	the Vbox wrapper
1. samples/wrapper:	the wrapper
1. sched:	C++ code for CGI programs, daemons, and some command-line tools
1. tools:	command-line tools (C++, PHP, Python)
1. win_build:	Visual Studio project files for Win build
