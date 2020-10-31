## Intro

The repository describes the basic setup of my MacBook.

## Table of Contents

- [Intro](#intro)
- [Table of Contents](#table-of-contents)
- [Software](#software)
  - [Small tools](#small-tools)
- [Manual installation](#manual-installation)
- [VS Code](#vs-code)
- [Oh My Zsh](#oh-my-zsh)
- [iTerm](#iterm)
- [OS Settings](#os-settings)
  - [Login Message](#login-message)
  - [Screenshots](#screenshots)
  - [Finder](#finder)
  - [Terminal](#terminal)
  - [Menu bar](#menu-bar)
  - [Other](#other)

## Software

Make the life as easy as possible. I don't use any Application from the AppStore. I rather use Homebrew for nearly everything.

Install Homebrew by:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

After the installation is completed, trigger the installation of all other software:

```sh
brew cask install aerial
brew cask install anaconda
brew cask install bettertouchtool
brew cask install cakebrew
brew cask install coderunner
brew cask install cyberduck
brew cask install drawio
brew cask install firefox
brew cask install istat-menus
brew cask install iterm2
brew cask install jiggler
brew cask install keepassxc
brew cask install keka
brew cask install pgadmin4
brew cask install quicklook-json
brew cask install r
brew cask install rstudio
brew cask install suspicious-package
brew cask install virtualbox
brew cask install visual-studio-code
brew cask install vlc
brew cask install wireshark

# Hack Font
brew cask install font-hack

# Markdown App
brew cask install joplin

# Research Assistant
brew cask install zotero

# If you have to manage VMs in your env
brew cask install vmware-remote-console

# If you stick to MSFT
brew cask install microsoft-azure-storage-explorer
# Includes OneDrive
brew cask install microsoft-office
brew cask install microsoft-teams
```

### Small tools

```sh
brew install autojump
brew install jq
brew install nmap
brew install telnet
brew install thefuck
brew install zsh
brew install zsh-completions
```

## Manual installation

In addition you need to manually install [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio), [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12), Microsoft Office.

## VS Code

Extension I'm using:

```sh
code-settings-sync
code-spell-checker
gitflow
gitlens
markdown-all-in-one
markdown-shortcuts
markdown-table-formatter
prettier-vscode
psi-header
python
sftp
template-finder v1.3.2
Theme-1337
vscode-ansible
vscode-diff
vscode-edit-csv
vscode-format-context-menu
vscode-todo-highlight
```

If these extensions are installed I recommend the following additional configuration on the `vscode/settings.json` file.

## Oh My Zsh

In my `.zshrc` configuration file adjust the following line

```sh
HIST_STAMPS="dd.mm.yyyy"
```

Add the following lines:

```sh
source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh
```

## iTerm

Take a minute to configure iTerm to your personal needs. My configuration is in the attached configuration.

[Default.json](:/7c3fb3f0bd4f46ae9e8b729c10e22247)

## OS Settings

### Login Message

Sets a custom message on the Login Window. Always useful if you forgot your MAC somewhere at work.

```sh
defaults write /Library/Preferences/com.apple.loginwindow LoginwindowText "I'm living at ground flor desk x on building y. Please return me."
```

### Screenshots

This disables the shadows from a screenshot taken from a Application

```sh
defaults write com.apple.screencapture disable-shadow -bool true
```

### Finder

```sh
echo "Finder: Show all filename extensions"
defaults write NSGlobalDomain AppleShowAllExtensions -bool true

echo "Finder: Show hidden files by default"
defaults write com.apple.Finder AppleShowAllFiles -bool true

echo "Finder: Expand save dialog by default"
defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true

echo "Finder: Show the ~/Library folder"
chflags nohidden ~/Library

echo "Finder: Show Path bar"
defaults write com.apple.finder ShowPathbar -bool true

echo "Finder: Show Status bar"
defaults write com.apple.finder ShowStatusBar -bool true
```

### Terminal

```sh
# echo "Only use UTF-8 in Terminal.app"
defaults write com.apple.terminal StringEncodings -array 4
```

### Menu bar

```sh
echo "Enable Show remaining battery time"
defaults write com.apple.menuextra.battery ShowPercent -string "YES"

echo "Don't show the remaining time on battery"
defaults write com.apple.menuextra.battery ShowTime -string "NO"

echo "Set date display in menu bar"
defaults write com.apple.menuextra.clock "DateFormat" "EEE MMM d H.mm"

echo "Show bluetooth and volume and other in the menubar"
defaults write com.apple.systemuiserver menuExtras -array "/System/Library/CoreServices/Menu Extras/Bluetooth.menu" "/System/Library/CoreServices/Menu Extras/Volume.menu"
```

### Other

```sh
echo "Stop iTunes from responding to the keyboard media keys"
launchctl unload -w /System/Library/LaunchAgents/com.apple.rcd.plist 2> /dev/null

echo "Disabling smart quotes and dashes..."
defaults write NSGlobalDomain NSAutomaticQuoteSubstitutionEnabled -bool false
defaults write NSGlobalDomain NSAutomaticDashSubstitutionEnabled -bool false

echo "Expand save panel by default"
defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true
defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode2 -bool true

echo "Expand print panel by default"
defaults write NSGlobalDomain PMPrintingExpandedStateForPrint -bool true
defaults write NSGlobalDomain PMPrintingExpandedStateForPrint2 -bool true
```
