Other notes about using the computer.

# Clear the Open With Menu [OS X]

Launch services doesn't do a very good job of keeping track of which
applications and services are around. There are many duplicates and
zombie services after some use. To rebuild the launch services database:

    /System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support/lsregister -kill -r -domain local -domain system -domain user

(from http://macs.about.com/od/usingyourmac/qt/remove-duplicate-applications-from-open-with.htm)

# Setup Vim on Windows

There are "steps" to set up on Windows related to Vundle. But first
you'll want to use Github for Windows to clone dotfiles to your
computer. Then make a `.vimrc` like the following:

    :source ~\Documents\GitHub\dotfiles\vim\vimrc.symlink

This causes vim to run that file, so your canonical configuration is
always living inside a Git repo.

Following that, use these instructions to do the Vundle magic:

https://github.com/gmarik/vundle/wiki/Vundle-for-Windows

& you should be good to go.
