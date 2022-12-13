# Linux Bootstrap by @marcusoftnet

This repository is my take on setting up a new Linux machine from scratch.
I have tweaked it from <https://github.com/joshukraine/linux-bootstrap>

This bootstrap script will install my dotfiles from here <https://github.com/marcusoftnet/linux-dotfiles>

## Installation

To install with a one-liner, run this:

```sh
bash <(wget -qO- https://raw.githubusercontent.com/marcusoftnet/linux-bootstrap/main/bootstrap) 2>&1 | tee ~/bootstrap.log
```

Want to read through the script first?

```sh
wget -qO- https://raw.githubusercontent.com/marcusoftnet/linux-bootstrap/main/bootstrap > bootstrap
less bootstrap
bash bootstrap 2>&1 | tee ~/bootstrap.log
```

## What does it do?

When you invoke `bootstrap`, this is what it does in a nutshell:

* Patch the system
* Install various software packages (see [`bootstrap`](./bootstrap) script for details)
* Install [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh).
* Install [my Linux dotfiles and settings](https://github.com/marcusoftnet/linux-dotfiles)
* Symlink dotfiles to `$HOME`
* Install several fixed-width fonts.
* Installs other softeware
  * Install Vundle and plugins for vim.
  * Set up Tmuxinator.
  * VS Code
  * IntelliJ