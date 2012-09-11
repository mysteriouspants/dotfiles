# NSError's Dotfiles

Largely pilfered from [skwp][skwp-dotfiles] and [holman][holman-dotfiles]'s
dotfiles. In fact, the whole rakefile is holman's.

These are my dotfiles. I do not maintain these at a high enough level of
standard to support other people trying to use this. You're welcome to
grab whatever you want, but it's not a full-stack. Any documentation is
actually notes to myself - because we all want docs when we're unboxing
that shiny new computer and thinking "this is nice and all, but where's
my vim plugins?"

# Step 1: Prereqs

In no specific order, yet some kind of forethought has been taken in the
order anyway:

* Xcode
* Xcode CLI tools
* Homebrew
  * Install `macvim`
  * Install `autoenv`
  * If still behind that freakin annoying work firewall, install
    `corkscrew`
* Set default shell to ZSH
* Install Oh-My-ZSH
* Install RVM (don't install rubies or gems yet until dotfiles are
  cloned, unless you like having megabytes of ri/rdoc nonsense floating
  around).
* Install my SSH keys (they should be floating around Dropbox
  somewhere...)
* SSH to some server to put the auth in Keychain (for no more annoying
  'type the password for `id_rsa`)

Finally...

# Step 2: Clone me!

Clone this here repo to `~/.dotfiles` or somewhere nice and quiet.

Remember to add `--recursive` and `--recursive-submodules` or you'll
have to thunk around with Janus a lot more than should be necessary.

# Step 3: Secrets

Add a `~/.secrets` file for user-specific information. It should look
something like this:

    export GIT_AUTHOR_NAME=''
    export GIT_AUTHOR_EMAIL=''
    export GIT_COMMITTER_NAME=''
    export GIT_COMMITTER_EMAIL=''
    export GITHUB_USER='NSError'
    export GITHUB_TOKEN=wtf was this?

# Step 4: Janus

    cd ~/.vim
    rake

[skwp-dotfiles]: https://github.com/skwp/dotfiles
[holman-dotfiles]: https://github.com/holman/dotfiles
