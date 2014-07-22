# Sean's Dotfiles

This repo contains all the scripts to provision a shiny new Mac.

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
git clone https://github.com/srankin/dotfiles.git Projects/dotfiles
```

Copy dotfiles to the root
```
cp -r ~/Projects/dotfiles/dotfiles ~
```

Install ThoughtBot/Laptop Script
```
bash <(curl -s https://raw.githubusercontent.com/thoughtbot/laptop/master/mac)
# Then, switch bash back to the default bash for good
chsh -s /bin/bash
```

Additional Rails Stuff
```
# Install the right version of ruby
rbenv install 2.0.0-p247
# Install bundler for the correct Ruby Version
gem install bundler
# Create a default postgres user
createuser -s -r postgres
# All clear to run the setup script!
```

Brewfile & Caskfile
```
brew bundle Projects/dotfiles/Brewfile
brew bundle Projects/dotfiles/Caskfile
```

Go get everything from the Apple App Store

Run ./.osx to tweak OSX
```
Projects/dotfiles/.osx
```

Login To Dropbox & Google Drive

Sync with Mackup
```
mackup restore
```
Install Airmail
Symlink Airmail
```
ln -s /Users/Sean/Dropbox/Apps/Airmail/General ~/Library/Containers/it.bloop.airmail/Data/Library/Application\ Support/Airmail/General
```
