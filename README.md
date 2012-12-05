# NSError's Dotfiles

Largely pilfered from [skwp][skwp-dotfiles] and
[holman][holman-dotfiles]'s dotfiles. In fact, the whole rakefile is
holman's.

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
* OS X GCC installer (if you plan on using any version of ruby before
  1.9.3 - otherwise this can be skipped).
* Xcode CLI tools
* Homebrew
  * Install `macvim`
  * Install `autoenv`
  * Install `rbenv`,  `rbenv-bundler`, and `ruby-build`
  * If still behind that freakin annoying work firewall, install
    `corkscrew`
* Set default shell to ZSH
* Install my SSH keys (they should be floating around Dropbox
  somewhere...)
* SSH to some server to put the auth in Keychain (for no more annoying
  'type the password for `id_rsa`)

Finally...

# Step 2: Clone me!

Clone this here repo to `~/.dotfiles` or somewhere nice and quiet.

Remember to add `--recursive` and `--recursive-submodules` or you'll
have to thunk around with Janus a lot more than should be necessary.

    git clone --recursive git@github.com:NSError/dotfiles.git ~/.dotfiles

# Step 3: Secrets

Add a `~/.secrets` file for user-specific information. It should look
something like this:

    export GIT_AUTHOR_NAME=''
    export GIT_AUTHOR_EMAIL=''
    export GIT_COMMITTER_NAME=''
    export GIT_COMMITTER_EMAIL=''
    export GITHUB_USER='NSError'
    export GITHUB_TOKEN=wtf was this?

# Step 4: Vim!

My Vim config has finally left the era of Janus. I'm now rocking a
custom setup which is something of a hybrid between Janus and spf13's
vim setup. This has created a very nice situation where I don't have a
(lot) of stuff I don't use, and I'm not constantly hitting keys and
finding it doing things I'm not familiar with.

Install the right bundles by simply telling Vim (and Vundle) to do so:

    vim +BundleInstall +qall

Next, install the patched powerline font; I used the Menlo font found at
here (though it is included in the repo for the sake of laziness; just
`cd ~/.dotfiles; open .` in order to get at it in OS X):

* https://github.com/Lokaltog/vim-powerline/wiki/Patched-fonts
* https://gist.github.com/1627888

Pick one that works on the platform you're using; consider writing some
conditionals in .vimrc to handle that, too.

# Step 5: ???

# Step 6: Profit!

# iTerm2

Install iTerm2. In Preferences > General under the Preferences
sub-heading, check "Load preferences from a user-defined folder or URL:"
and then set that folder or URL to:

    /Users/cmiller/.dotfiles/iTerm2

Obviously you'll want to mangle that based on the local username. Reload
iTerm2, and everything should be exactly as it should be. Fun, no?

If the theme doesn't come on over, try installing [Liquid Carbon][lq].

[skwp-dotfiles]: https://github.com/skwp/dotfiles
[holman-dotfiles]: https://github.com/holman/dotfiles
[lq]: https://github.com/markcho/iTerm2_LiquidCarbon
