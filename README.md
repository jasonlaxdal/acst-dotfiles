# Jason's ACST Dotfiles (forked from Sean)

This repo contains all the scripts to provision a silver matte new Mac.

#### Installation

First, show all files
```
defaults write com.apple.finder AppleShowAllFiles YES
```

Install X-code command-line tools
```
xcode-select --install
```

Download this repo to your ~/Projects directory

```
git clone https://github.com/jasonlaxdal/acst-dotfiles.git src/acst-dotfiles
```

Copy dotfiles/dotfiles to user folder

```
cd ~/src/acst-dotfiles
cp -r ./dotfiles/ ~/
```

Make sure that .laptop.local us updated.

Install ThoughtBot/Laptop Script
```
bash <(curl -s https://raw.githubusercontent.com/thoughtbot/laptop/master/mac) 2>&1 | tee ~/laptop.log
```

Install ThoughtBot/dotfiles
```
git clone git://github.com/thoughtbot/dotfiles.git
brew tap thoughtbot/formulae
brew install rcm
env RCRC=$HOME/dotfiles/rcrc rcup
```

Additional Setup (Move gems to laptop.local?)

Go get everything from the Apple App Store

Run ./.osx to tweak OSX

```
Projects/dotfiles/.osx
```

```
# Install Atom packages
apm stars --install
```

Login To Dropbox & Google Drive

Finally, install software
- Adobe CS6
