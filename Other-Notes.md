Other notes about using the computer.

# Clear the Open With Menu [OS X]

Launch services doesn't do a very good job of keeping track of which
applications and services are around. There are many duplicates and
zombie services after some use. To rebuild the launch services database:

    /System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support/lsregister -kill -r -domain local -domain system -domain user

(from http://macs.about.com/od/usingyourmac/qt/remove-duplicate-applications-from-open-with.htm)
