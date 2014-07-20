# Sean's dotfiles

Sean's dot, brew, cask, and shell files for new machine setup

#### Installation

First, show all files
```
defaults write com.apple.finder AppleShowAllFiles YES
```

Download this repo to your ~ directory.

```
git clone https://github.com/srankin/dotfiles.git
```

Install X-code command-line tools
```
xcode-select --install
```

#### Install ThoughtBot/Laptop Script
```
bash <(curl -s https://raw.githubusercontent.com/thoughtbot/laptop/master/mac)
# Then, switch bash back to the default bash for good
chsh -s /bin/bash
```

#### Additional Rails Stuff
```
# Install the right version of ruby
rbenv install 2.0.0-p247
# Install bundler for the correct Ruby Version
gem install bundler
# Create a default postgres user
createuser -s -r postgres
# All clear to run the setup script!
```

#### Brewfile & Caskfile
```
brew bundle Brewfile
brew bundle Caskfile
```

#### Go get everything from the Apple App Store

### # Run ./.osx to tweak OSX
```
# ./.osx
```

#### Login To Dropbox

#### Sync Settings with Mackup
```
mackup restore
```
