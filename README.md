The repo decribes the basic setup of my MAC OSX. 

# Tools

## Audio and Video Tools

VLC media player - http://www.videolan.org/index.html

## Browsers

Firefox - https://www.mozilla.org/de/firefox/

## Communication

### File Sharing

Cyberduck - https://cyberduck.io/

## Cloud Storage

Nextcloud - https://nextcloud.com/
If you have a private setup where you want to keep your files in sync.

## Developer Tools

### API Development and Analysis

Insomnia - https://insomnia.rest/

### Command Line Tools

Homebrew - https://brew.sh/index_de

iTerm2 - https://www.iterm2.com/
An alternative terminl.

tmux - https://github.com/tmux/tmux

Oh My Zsh - https://github.com/robbyrussell/oh-my-zsh

### Database Tools

PSequel - http://www.psequel.com/

Sequel - http://www.sequelpro.com/

### Network Analysis

Proxyman - https://proxyman.io/

Wireshark https://www.wireshark.org/

### Other

TAD Viewer - https://www.tadviewer.com/

Cacher - https://www.cacher.io/

### Version Control

Git - https://git-scm.com/download/mac

GitHub Desktop - https://desktop.github.com/

###  Virtualization

Docker - https://www.docker.com/

Virutal Box - http://www.virtualbox.org/

## Text Editors

### Text and Code Editors

Sublime Text - https://www.sublimetext.com/
Advanced Editor.

Visual Studio Code -  https://code.visualstudio.com/

### Office

Libre Office - https://www.libreoffice.org/
I like it esxpecially when working with other non-MAC users on docments.

OneNote - https://products.office.com/de-de/onenote/

### RSS

RSS Reader NetNewsWire - https://ranchero.com/netnewswire/

## Utilities

### Clipboard Tools

Clipy - https://github.com/Clipy/Clipy
I love this app to store often used phrases or snippets into it.

### File Tools

Keka - https://www.keka.io/en/

### Menu Bar Tools

Dozer - https://github.com/Mortennn/Dozer

### Other 

BetterRename - https://www.publicspace.net/BetterRename/

PopClip - https://pilotmoon.com/popclip/
Helpful in daily work on nearly all applications.

### Password Management

KeePassXC - https://keepassxc.org

Password Safe - https://pwsafe.org

### Productivity

BetterTouchTool - https://folivora.ai/
Set custom shortcuts and gestures for your MAC.

### Security

KnockKnock - https://objective-see.com/products/knockknock.html

LuLu - https://objective-see.com/products/lulu.html

Little Snitch 4 - https://www.obdev.at/products/littlesnitch/download.html

Netiquette - https://objective-see.com/products/netiquette.html

# System Configuration

## Login Message

Sets a custom message on the Login Window. Always useful if you forgot your MAC somewhere at work.

`
defaults write /Library/Preferences/com.apple.loginwindow LoginwindowText "I'm living at ground flor desk x."
`

## Screenshots

This disables the shadows from a screenshot taken from a Application

`
defaults write com.apple.screencapture disable-shadow -bool true
killall SystemUIServer
`