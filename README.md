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
Setup cron file
```
crontab ~/.crontab
```

Additional Rails Stuff
```
# Install the right version of ruby
rbenv install 2.0.0-p247
# Install bundler for the correct Ruby Version
gem install bundler
# Create a default postgres user
createuser -s -r postgres
# Generate & upload a public key to Heroku
heroku keys:add
# Add git remotes
git remote add build git@heroku.com:hhr-build.git
git remote add demo git@heroku.com:hhr-demo.git
git remote add production git@heroku.com:hhr-production.git
git remote add qa git@heroku.com:hhr-qa.git
git remote add staging git@heroku.com:hhr-staging.git
git remote add temp git@heroku.com:hhr-temp.git
git remote add test git@heroku.com:hhr-test.git
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

Finally, install software
- Adobe CS6
- Microsoft Office 2011
- Aperture

