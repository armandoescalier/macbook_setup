# Macbook Setup
Initial setup for a new Macbook.

## Index

- [MacOS Settings](#macos-settings)
- [Code stuff](#code-stuff)
- [Terminal](#terminal)
- [VS Code](#vscode)
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
Add this line to `~/.zshrc`
``` batch
if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi
```
Versions
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

## Terminal

### iTerm2
- [iterm 2](https://iterm2.com/)
- ohmyzsh theme setup by Josean Martinez
    - [YT Video](https://www.youtube.com/watch?v=CF1tMjvHDRA)
    - [Blog post](https://www.josean.com/posts/terminal-setup)

### ohmyzsh
Run this to install ohmyzsh
``` batch
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### PowerLevel10K
Run this to install PowerLevel10K:
``` batch
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
``` 
Now that it's installed, open the `~/.zshrc` file with your preferred editor and change the value of `ZSH_THEME` as shown below:
``` batch
ZSH_THEME="powerlevel10k/powerlevel10k"
```
To reflect this change on your terminal, restart it or run this command:
``` batch
source ~/.zshrc
```
Overwrite Powerlevel10k config
``` batch
p10k configure
```

#### ZSH Plugins
Install zsh-autosuggestions:
``` batch
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
Install zsh-syntax-highlighting:
``` batch
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Open the "~/.zshrc" file in your desired editor and modify the plugins line to what you see below.
``` batch
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```
Load these new plugins by running:
``` batch
source ~/.zshrc
```

## VSCode
- [VS Code](https://code.visualstudio.com/)
- Theme: `Omni Owl Theme` by `Guilherme Rodz`

#### Custom VS Code
Add this code within `~/Library/Application Support/Code/User/settings.json`
``` json
{
    "workbench.colorTheme": "Omni Owl",
    "window.zoomLevel": 1,
    "editor.minimap.enabled": false,
    "workbench.colorCustomizations": {
        "list.inactiveSelectionBackground": "#7c12e6",
        "statusBar.background": "#7c12e6",
        "list.hoverBackground": "#7c12e6",
        "editor.findMatchBackground" : "#f0f0f0",
        "editor.findMatchHighlightBackground": "#f0f0f0"
    }
}
```
Add `code .` to path in order to be allowed to open VS Code from terminal.
``` batch
nano ~/.zshrc
```
Add this at the end of the file
``` batch
# VS Code
export PATH="$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
```

## Tools
### Rectangle App
Move and resize windows in macOS using keyboard shortcuts.
``` batch
opt + cmd + arrow
```
- [rectangle app](http://rectangleapp.com/)
