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

Copy dotfiles/dotfiles to user folder

Make sure that .laptop.local us updated.

Install ThoughtBot/Laptop Script
```
bash <(curl -s https://raw.githubusercontent.com/thoughtbot/laptop/master/mac) 2>&1 | tee ~/laptop.log
```

Then, switch bash back to the default bash for good
```
chsh -s /bin/bash
```

Setup cron file
```
crontab ~/.crontab
```

Additional Setup (Move gems to laptop.local?)
```
# Install an updated version of Ruby, as specified 2.2.0 in my ~/.ruby-version file.
rbenv install 2.2.0
rbenv install 2.0.0-p48

# Update Rubygems
gem update --system 

# Install Rails
gem install rails

# Install Bundler
gem install bundler

# Under Yosemite, I had to install libv8 like this:
# I didn't have to do this last time...
# gem install libv8 -v '3.16.14.3' -- --with-system-v8

# Create a default postgres user
createuser -s -r postgres

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

Finally, install software
- Adobe CS6
