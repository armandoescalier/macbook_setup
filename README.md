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
- Trackpad/mouse
    - Natural Scrolling Disabled
- Keyboard
    - Spanish (not latam)
- Control Center
    - Enable Hot Corners
- Finder
    - Visualization/Show path


## Code stuff

### Brew
``` batch
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Git
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

## Ruby On Rails
Check this guide by GoRails:
- [Install Ruby On Rails on macOS](https://gorails.com/setup/macos/11-big-sur)

### Rbenv
[rbenv](https://github.com/rbenv/rbenv) is a version manager tool for the `Ruby`.

``` batch
brew install rbenv ruby-build
```
Add this line to `~/.zshrc`
``` batch
if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi
```
#### Versions
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
open ~/.zshrc
```
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

### ZSH Plugins
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
open ~/.zshrc
```
``` batch
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```
Load these new plugins by running:
``` batch
source ~/.zshrc
```

## VSCode
### VSCode Extensions
- [Omni Owl Theme](https://marketplace.visualstudio.com/items?itemName=guilhermerodz.omni-owl) by `Guilherme Rodz`
- [Ruby](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby) by `Peng Lv`
- [VSCode Ruby](https://marketplace.visualstudio.com/items?itemName=wingrunr21.vscode-ruby) by `Stafford Brunk`
- [endwise](https://marketplace.visualstudio.com/items?itemName=kaiwood.endwise) by `Kai Wood`
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) by `Jun Han`

### Custom settings
Add this code within `~/Library/Application Support/Code/User/settings.json`
``` json
{
    "window.zoomLevel": 1,
    "editor.minimap.enabled": false,
    "workbench.colorTheme": "Omni Owl",
    "editor.multiCursorModifier": "alt",
    "files.trimTrailingWhitespace": true,
    "ruby.useLanguageServer": true,
    "ruby.intellisense": "rubyLocate",
    "editor.rulers": [120],
    "workbench.colorCustomizations": {
        "list.inactiveSelectionBackground": "#7c12e6",
        "statusBar.background": "#7c12e6",
        "list.hoverBackground": "#7c12e6",
        "editorGutter.addedBackground": "#28a745", // Color for added lines (green)
        "editorGutter.modifiedBackground": "#2188ff", // Color for modified lines (blue)
        "editorGutter.deletedBackground": "#cb2431", // Color for removed lines (red)
        "diffEditor.insertedTextBackground": "#28a74533", // Background color for added text (green with transparency)
        "diffEditor.removedTextBackground": "#cb243133", // Background color for removed text (red with transparency)
        "editorRuler.foreground": "#ff4081"
        // "editor.findMatchBackground" : "#ffffff",
        // "editor.findMatchHighlightBackground": "#9c9c9c"
    }
}
```
Add `code .` to path in order to be allowed to open VS Code from terminal.
``` batch
open ~/.zshrc
```
Add this at the end of the file
``` batch
# VS Code
export PATH="$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
```

## Tools
- [rectangle app](http://rectangleapp.com/)
  - Move and resize windows in macOS using keyboard shortcuts.
- [Github Desktop](https://desktop.github.com/)
  - Focus on what matters instead of fighting with Git.
- [RapidAPI](https://paw.cloud/)
  - a full-featured HTTP client that lets you test and describe the APIs you build or consume.
- [Postico2](https://eggerapps.at/postico2/)
  - Postico 2 is a database app.
