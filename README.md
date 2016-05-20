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
cp .* ~/
```

Make sure that .laptop.local us updated.

Install ThoughtBot/Laptop Script
```
bash <(curl -s https://raw.githubusercontent.com/thoughtbot/laptop/master/mac) 2>&1 | tee ~/laptop.log
```


Additional Setup (Move gems to laptop.local?)
```
# Install an updated version of Ruby, as specified 2.2.0 in my ~/.ruby-version file.
rbenv install 2.2.0
rbenv install 2.0.0-p481

# REHASH rbenv
rbenv rehash

# Automate rbenv rehash
git clone https://github.com/sstephenson/rbenv-gem-rehash.git ~/.rbenv/plugins/rbenv-gem-rehash

# Update Rubygems
gem update --system

# Install Rails
gem install rails

# Install Bundler
gem install bundler

# For VPN Subnet routing, install the ip-up file

```

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
