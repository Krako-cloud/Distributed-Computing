[Link](https://github.com/BOINC/boinc/wiki/SoftwareDevelopment)


## Client data model
This document describes changes in 6.13 to the client to support distributed storage.

### Current
FILE_INFO elements

 - status (present, not present, error)
 - urls
 - bool generated_locally
 - bool upload_when_present
 - bool uploaded
 - bool sticky
