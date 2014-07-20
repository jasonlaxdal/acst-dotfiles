# Sean's dotfiles

Sean's dot, brew, cask, and shell files for new machine setup

## Installation

### Download this stuff to your ~ directory.

`git clone https://github.com/srankin/dotfiles.git


### Install X-code command line tools
`xcode-select --install

````
# Show all files
defaults write com.apple.finder AppleShowAllFiles YES

```

```
# Install thoughtbot/laptop script: https://github.com/thoughtbot/laptop
bash <(curl -s https://raw.githubusercontent.com/thoughtbot/laptop/master/mac)
# Then, switch bash back to the default bash for good
chsh -s /bin/bash

```

```
# Additional Rails Stuff
# Install the right version of ruby
rbenv install 2.0.0-p247
# Install bundler for the correct Ruby Version
gem install bundler
# Create a default postgres user
createuser -s -r postgres
# All clear to run the setup script!
```

```
# Brewfile & Caskfile
# brew bundle Brewfile
# brew bundle Caskfile
```


```
# Sync Settings with Mackup
mackup restore
```

# Go get everything from the Apple App Store

```
# Run Download/Setup/.osx to Tweak OSX
# ./.osx
```
