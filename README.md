# Macbook Setup
Initial setup for a new Macbook.

## Index

- [MacOS Settings](#macos-settings)
- [Code stuff](#code-stuff)
- [Tools](#tools)


## MacOS Settings
Customize:
- Trackpad
- Keyboard
- Control Center


## Code stuff

### Brew
``` batch
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Git
``` batch
git config user.name "Joe Doe"
git config user.email your@email.example
```
``` batch
git config --global user.name "Your Name Here"
git config --global user.email your@email.example
```
Check with:
``` batch
git config user.name && git config user.email
```

### Command Line Tools (xcode)
``` batch
xcode-select --install
```

### Ruby On Rails
Check this guide by GoRails:
- [Install Ruby On Rails on macOS](https://gorails.com/setup/macos/11-big-sur)

#### Rbenv
[rbenv](https://github.com/rbenv/rbenv) is a version manager tool for the `Ruby`.

``` batch
brew install rbenv ruby-build
```

``` batch
# list latest stable versions:
rbenv install -l

# list all local versions:
rbenv install -L

# install a Ruby version:
rbenv install 3.1.2
```

- set the default Ruby version for this machine
``` batch
rbenv global 3.1.2
```
- set the Ruby version for this directory
``` batch
rbenv local 3.1.2
```

## Tools

### iTerm2
- [iterm 2](https://iterm2.com/)
- [ohmyzsh theme setup by Josean Martinez](https://www.youtube.com/watch?v=CF1tMjvHDRA)

### VS Code
- [VS Code](https://code.visualstudio.com/)
- Theme: `Omni Owl Theme` by `Guilherme Rodz`

### Rectangle App
Move and resize windows in macOS using keyboard shortcuts.
``` batch
opt + cmd + arrow
```
- [rectangle app](http://rectangleapp.com/)