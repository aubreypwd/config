# Config

This is just a simple document to help remind me how I manage my system.

---

## Persistant Repositories _via_ `ghq`

Using [ghq](https://github.com/x-motemen/ghq) as much as I can to install repositories I want to persist on my system `~/Repos` so I don't have to keep track of all the repos I have installed. I _may_ symlink to them.

- The configuration for `ghq` is in [vcsh-git/.gitconfig](https://github.com/aubreypwd/vcsh-git/blob/master/.gitconfig) under the `ghq` heading.
- Also [`vcsh-zsh/.zshrc`](https://github.com/aubreypwd/vcsh-zsh/blob/master/.zshrc#L124) will also install some persistent repositores for you

---

## System files (dot-files) _via_ `vcsh`

I use [vcsh](https://github.com/RichiH/vcsh) which version controls my `$HOME` using [many repositories](https://github.com/aubreypwd?tab=repositories&q=vcsh-*&type=&language=).

- Install using `vcsh clone repo <repo-name>`
- If you have files already on the system you will have to use `vcsh <repo-name> reset --hard FETCH_HEAD` afterwards, and `vcsh write-gitignore <repo-name>`

### To install a `vcsh-*` repo:

```bash
vcsh clone <repo> <name>
```

When you do this, if the files tracked are already in your filessystem, you will get a warning:

```bash
vcsh: error: '<file>' exists.
vcsh: fatal: will stop after fetching and not try to merge!
  Once this situation has been resolved, run 'vcsh sublime-text-3 pull' to finish cloning.
```
To remedy this, just use `vcsh <name> reset --hard origin/master` to sync up with the remote.


### Sublime Text 3

- Use [vcsh-sublime-text-3](https://github.com/aubreypwd/vcsh-sublime-text-3) to track my config files in `$HOME/Library/Application Support/Sublime Text 3/*`

#### Snippets

- Use [vcsh-sublime-text-3-snippets](https://github.com/aubreypwd/vcsh-sublime-text-3-snippets) to track Snippets in `$HOME/Library/Application Support/Sublime Text 3/Packages/User/Snippets`

...but I may move this to `ghq` or something later on.

---

## Applications _via_ `brew, brew cask, mas`

[`brew`](https://brew.sh), [`brew cask`](https://github.com/Homebrew/homebrew-cask), [`mas`](https://formulae.brew.sh/formula/mas) for App Store.

- I use [vcsh-homebrew](http://github.com/aubreypwd/vcsh-homebrew) and `brew bundle dump` to track what's installed with these in a `Brewfile`
- Use `brew bundle Brewfile` to install all the things

I can then, at any time run `brew bundle "$HOME/Brewfile"` to install anything tracked there.

### My Applications _via_ `brew cask`

I have some applications I build as [electron](https://www.electronjs.org/) apps, e.g. [Reedsy](https://github.com/aubreypwd/reedsy-mac) that can be installed using `brew cask` as well. I manage a [tap](https://github.com/aubreypwd/homebrew-cask/) for all the apps you can install.

Once you add the tap, you can find the repo for the tap at `/usr/local/Homebrew/Library/Taps/aubreypwd/homebrew-cask`.

---

## Custom zsh aliases and custom functions via `antigen`

All my aliases and custom functions are `oh-my-zsh` [plugins](https://github.com/aubreypwd?tab=repositories&q=zsh-plugin-&type=&language=) that can be installed using `antigen`, e.g. [aubreypwd/zsh-plugin-x](https://github.com/aubreypwd/zsh-plugin-x#development). 

If you install them using SSH, you can contribute to the repo by simply going to `$HOME/.antigen/bundles/aubreypwd/zsh-plugin-<name>`.

- [Template for creating new plugins](https://github.com/aubreypwd/zsh-plugin-template)

---

This document is a work in progress and likely still misses a ton of stuff. 
