# System

This is just a simple document to help remind me how I manage my system.

## Persistant Repositories

Using [ghq](https://github.com/x-motemen/ghq) as much as I can to install repositories I want to persist on my system `~/Repos` so I don't have to keep track of all the repos I have installed. I _may_ symlink to them.

- The configuration for `ghq` is in [vcsh-git/.gitconfig](https://github.com/aubreypwd/vcsh-git/blob/master/.gitconfig) under the `ghq` heading.

## System files (dot-files)

I use [vcsh](https://github.com/RichiH/vcsh) which version controls my `$HOME` using [many repositories](https://github.com/aubreypwd?tab=repositories&q=vcsh-*&type=&language=).

## Applications

[`brew`](https://brew.sh), [`brew cask`](https://github.com/Homebrew/homebrew-cask), [`mas`](https://formulae.brew.sh/formula/mas) for App Store.

- I use [vcsh-homebrew](http://github.com/aubreypwd/vcsh-homebrew) and `brew bundle` to track what's installed with these in a `Brewfile`
- Use `brew bundle Brewfile` to install all the things

## Sublime Text 3

- Use [vcsh-sublime-text-3](https://github.com/aubreypwd/vcsh-sublime-text-3) to track my config files in `$HOME/Library/Application Support/Sublime Text 3/*`

### Snippets

- Use [vcsh-sublime-text-3-snippets](https://github.com/aubreypwd/vcsh-sublime-text-3-snippets) to track Snippets in `$HOME/Library/Application Support/Sublime Text 3/Packages/User/Snippets`

...but I may move this to `ghq` or something later on.

---

This document is a work in progress and likly still misses a ton of stuff. 
