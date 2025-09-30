# mARCH

My collection of configurations, dotfiles, and projects used for setting up my Arch Linux environment on a new PC. Shoutout kbujari!

## Usage

This is a bare git repo in `$HOME`. This alias has been added to the `.bashrc` file:

```sh
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
```

To clone the configs, run:

```sh
git clone --bare <git-repo-url> $HOME/.dotfiles
alias dotfiles='/usr/bin/git --git-dir="$HOME/.dotfiles/" --work-tree="$HOME"'
dotfiles checkout
dotfiles config --local status.showUntrackedFiles no
```

To pull down all submodules to the latest version, run:
```sh
dotfiles submodule update --init --recursive
dotfiles submodule update --remote --merge
```
