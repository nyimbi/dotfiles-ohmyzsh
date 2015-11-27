# Nyimbi's dotfiles

## Installation
## A Bit of Background
I have tweaked this set of dotfiles to suit my development workflow. The tools I generally use are:
- macports: does all the linux/unix FOSS goodness for me (I know about homebrew, but hey...)
- SublimeText
- Atom.io: with emmet, elixir, rust, packages
- Brackets.io: For HTML style stuff, when I need visual feedback quick
- Jekyll and Nanoc: for generating static websites post haste
- iTerm2: as a souped up terminal
- QuickSilver: As a launcher (don't want to pay for alfred :-)
- Postgres.app: For a self contained Postgresql when I need it
- Dropbox: And my src directory is kept here too


The Bootstrap Script will download and setup my day-to-day programming languages and tools
- Rust: IUP, wxwidgets
- Python: Numpy, scipy, sympy, matplotlib, opencv, pyqt, ipython, pandas, orange, wxPython, simplecv
- Julia
- gcc and LLVM



## What this does
- Added a .extra file to hold my custom configs for all my macs, change to suit you
- I use macports. not homebrew (silly I know, but hey)
- It seems generally necessary to setup LC_ALL, LC_LANG, LC_LANGUAGE on remote servers so I do that
- (toDo) Modified ssh ServerKeepAlive
- my code directory is generall ~/src so I point to that alot
- My favorite tools: Sublime Text, Atom.io, Brackets.io
- My current slew of languages: Rust, Rackets, Python
- Web tools: Jekyll, Nanoc
- Of course I am using ohmyz.sh and iTerm2
- I like Dash (https://kapeli.com/dash)
- Since I am totally silly I install all my python packages in the system folders. so I set PYTHONPATH (Helps macports install opencv)
- the  .osx seems particularly dangerous. so commented out everything. Enable only what you need




### Using Git and the bootstrap script

You can clone the repository wherever you want. (I like to keep it in `~/Projects/dotfiles`, with `~/dotfiles` as a symlink.) The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/mattstauffer/ohmyzsh-dotfiles.git
```

The bootstrap.sh file currently doesn't work, so just copy any of the dotfiles you like into your home directory.

### Git-free install

To install these dotfiles without Git:

```bash
cd; curl -#L https://github.com/mattstauffer/ohmyzsh-dotfiles/tarball/master | tar -xzv --strip-components 1 --exclude={README.md,bootstrap.sh}
```

To update later on, just run that command again.

### Specify the `$PATH`

If `~/.mix-path` exists, it will be sourced along with the other files, before any feature testing (such as [detecting which version of `ls` is being used](https://github.com/mathiasbynens/dotfiles/blob/aff769fd75225d8f2e481185a71d5e05b76002dc/.aliases#L21-26)) takes place.

Here’s an example `~/.mix-path` file that adds `~/utils` to the `$PATH`:

```bash
export PATH="$HOME/utils:$PATH"
```

### Add custom commands without creating a new fork

If `~/.mix-extra` exists, it will be sourced along with the other files. You can use this to add a few custom commands without the need to fork this entire repository, or to add commands you don’t want to commit to a public repository.

### Install Homebrew formulae

When setting up a new Mac, you may want to install some common [Homebrew](http://brew.sh/) formulae (after installing Homebrew, of course):

```bash
brew bundle .brewfile
```

## Original (Bash dotfiles) Author

| [![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](http://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](http://mathiasbynens.be/) |

## Thanks to…

* @ptb and [his _OS X Lion Setup_ repository](https://github.com/ptb/Mac-OS-X-Lion-Setup)
* [Ben Alman](http://benalman.com/) and his [dotfiles repository](https://github.com/cowboy/dotfiles)
* [Chris Gerke](http://www.randomsquared.com/) and his [tutorial on creating an OS X SOE master image](http://chris-gerke.blogspot.com/2012/04/mac-osx-soe-master-image-day-7.html) + [_Insta_ repository](https://github.com/cgerke/Insta)
* [Cãtãlin Mariş](https://github.com/alrra) and his [dotfiles repository](https://github.com/alrra/dotfiles)
* [Gianni Chiappetta](http://gf3.ca/) for sharing his [amazing collection of dotfiles](https://github.com/gf3/dotfiles)
* [Jan Moesen](http://jan.moesen.nu/) and his [ancient `.bash_profile`](https://gist.github.com/1156154) + [shiny _tilde_ repository](https://github.com/janmoesen/tilde)
* [Lauri ‘Lri’ Ranta](http://lri.me/) for sharing [loads of hidden preferences](http://lri.me/osx.html#hidden-preferences)
* [Matijs Brinkhuis](http://hotfusion.nl/) and his [dotfiles repository](https://github.com/matijs/dotfiles)
* [Nicolas Gallagher](http://nicolasgallagher.com/) and his [dotfiles repository](https://github.com/necolas/dotfiles)
* [Sindre Sorhus](http://sindresorhus.com/)
* [Tom Ryder](http://blog.sanctum.geek.nz/) and his [dotfiles repository](https://github.com/tejr/dotfiles)

* anyone who [contributed a patch](https://github.com/mathiasbynens/dotfiles/contributors) or [made a helpful suggestion](https://github.com/mathiasbynens/dotfiles/issues)
