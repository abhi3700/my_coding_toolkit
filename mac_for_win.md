# MacOS for Windows users

## Installation

## Folders
* Root: `/`
* Temp: `/tmp`
* Home: `~`
* Desktop: `~/Desktop`

### Update
* After updating, update the CLI tools using `xcode-select --install` in terminal.

## Glossary (Win <--> Mac)
* Explorer <--> Finder
* Taskbar <--> Dock
* Action center <--> Notification Center
* `.exe` <--> `.dmg`
* Properties <--> Quick look
* Task Manager <--> Activity Monitor
* Spotlight: help you quickly find apps, documents, and other files on your Mac.

## Keyboard shortcuts
| Mac | Win |
|---|---|
| cmd | ctrl, win |
| opt | alt |

* <kbd>command+c</kbd>: copy
* <kbd>command+v</kbd>: paste
* <kbd>command+m</kbd>: minimize an opened windows 
* <kbd>command+w</kbd>: close the App, but still open in background. ~ `ctrl+w`
* <kbd>command+q</kbd>: quit the App
* <kbd>command+[</kbd>: Go Back on browser
* <kbd>command+]</kbd>: Go Forward on browser ~ `backspace`
* <kbd>command+F3</kbd>: Show Desktop ~ `win+d`
* <kbd>command+shift+c</kbd>: Go to computer ~ `win+e`
> NOTE: It won't work on browser
* <kbd>command+tab</kbd>: Go forward in opened applications ~ `alt+tab`
* <kbd>command+shift+tab</kbd>: Go backward in opened applications ~ `alt+shift+tab`
* <kbd>command+shift+n</kbd>: create a new folder at selected directory
* <kbd>option+ <-</kbd>: skip to character after space ~ `ctrl+ <-`
* <kbd>option+ -></kbd>: skip to character before space ~ `ctrl+ ->`
* <kbd>option+command+delete</kbd>: permanent delete ~ `shift+delete`
* open terminal in a finder at a location: open terminal >> type cd << drag the folder into the terminal >> enter
* <kbd>command+shift+3</kbd>: Full capture
* <kbd>command+shift+4</kbd>: Custom capture. To copy, press & hold the `control` key during the capture. And paste into wherever you want.
* <kbd>command+shift+4</kbd>: More features related to capture
* <kbd>control+ <-</kbd>: Switch to workspace towards right ~ `ctrl+alt+ <-`
* <kbd>control+ -></kbd>: Switch to workspace towards left ~ `ctrl+alt+ ->`
* <kbd>command+spacebar</kbd>: Open Spotlight menu which helps in searching anything
* <kbd>command+shift+spacebar</kbd>: Open Spotlight in the Finder
* Cut & Paste file:
  1. Copy <kbd>command+c</kbd>
  2. Paste with replacing the copied file <kbd>command+option+v</kbd>
* <kbd>command+tab</kbd>: Switch to an Application
* <kbd>command+`</kbd>: Switch to a window of an Application
* <kbd>control+down</kbd>: show all opened windows of an App. Restore back by opening the current window via <kbd>control+up</kbd>
* <kbd>command+up</kbd>: Home
* <kbd>command+down</kbd>: End
* Add your own shortcut key using [this](https://apple.stackexchange.com/a/212607/435627)
* [custom] <kbd>ctrl+opt+leftarrow</kbd>: Tile to the left of the window
* [custom] <kbd>ctrl+opt+rightarrow</kbd>: Tile to the right of the window
* <kbd>command+option+d</kbd>: Hide the dock (or taskbar in Windows)
* <kbd>command+shift+.</kbd>: Show/Hide the hidden files (starting with ., ).
* <kbd>command+t</kbd> on Finder creates a separate tab.
* <kbd>command+i</kbd>: Get info on an App i.e. basically right click >> Select "Get Info"
* <kbd>cmd+ctrl+f</kbd>: Go & Escape fullscreen for an App
                                                                                                                                      
## Installation
* Install:
  - M-1: Go to App store, then press `GET` to install.
  - M-2: From internet download the file (`.dgm` preferrred) >> install >> drag & drop to "Applications" 
* Uninstall:
  - Go to "Finder", search for App >> drag & drop the App to "Bin"

## Apps
* Numbers: a quick analysis app like Excel for data analytics.
* Pages: a document app like Word, but with PPT type of styling. Easy to add cards, etc.
* Notes: a note app for TODO list
* Miro: Architecture, Mind Map, Whiteboard
* [UTM](https://mac.getutm.app/): A FREE virtual environment for Linux, Windows on Mac OS

## Display
* Night light/effect: "System Preferences" >> Displays >> Night Shift >> Schedule: On, Manual
* Resolution: Choose 2nd i.e. `1280 x 800`

## Touchpad
* three touch towards up: Show all the opened apps & also create new workspace or switch to a workspace.
* Single clicked with 2 fingers on the touchpad ~ `Right click` on Windows.
* Touchpad settings can be changed.

## Browser (chrome-based)
* <kbd>cmd+opt+leftarrow</kbd>: switch to left tab
* <kbd>cmd+opt+rightarrow</kbd>: switch to right tab
* <kbd>cmd+w</kbd>: close tab
* <kbd>cmd+shift+w</kbd>: close window

## Terminal
### Shortcut keys
* <kbd>ctrl+l</kbd>: clear the console
* <kbd>command+l</kbd>: clear console by 1 command

### Commands
* `$ open .`: open the Finder in the directory
* Run `.sh` file: `sh /path/to/file/with/extension`
* `$ which <command>`: gives the location of the command file

### PATH
* Stored in `/etc/profile`
* Add current directory to the PATH:
  - Open the file in ST editor, `$ subl ~/.zprofile`.
  - add this line `export PATH=$PWD/bin:$PATH` to the End of File (EOF). If a specific directory, then `export PATH=<custom-directory>:$PATH` e.g. `export PATH="/Users/abhi3700/Desktop/solana-1.8.5/bin:$PATH"`
  - Run this to activate `$ source ~/.zprofile`
  - Now, use the command in the current/new terminal. 

### Beautify
#### 1. Preparation
Recommend to install homebrew first:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Install zsh if you are on macOS version prior to Catalina:

* Install zsh `brew install zsh`
* Set zsh as your default shell `chsh -s /usr/local/bin/zsh`

#### 2. Install oh-my-zsh
* `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

#### 3. Install oh-my-zsh theme & must-have plugins
* config `.zshrc` (present in `~` location)
* open via `nano ~/.zshrc` & set these
* Set `ZSH_THEME` to your favorite theme name (preferred `intheloop`). Select from [link1](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes), [link2](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes)
* must-have plugins
```
plugins=(
  git
  extract
  autojump
  zsh-autosuggestions
  zsh-syntax-highlighting
)
```

## How-to
* [Force Shutdown using Key](https://www.youtube.com/watch?v=ePhnDneb19M)
* Hibernate: Go to Apple icon >> Shutdown >> tick the "Reopen the windows..." >> Press shutdown button. 

## Troubleshoot
### 1. Error: 'This Apple ID has not yet been used with the App Store'
* This error occurs after login into "App Store" >> press Review button >> Error >> Again login >> Review >> Error .....likewise infinite times. 
* __Solution__: Open "Apple Music" App. Go to Account on the top >> Login using Apple ID >> Set the payment (as None or other method) & billing address >> Done.

### 2. Unable to run unverified App
1. Open __Finder__
1. Search for the App
1. Select and `ctrl+click (on touchpad)` >> open
1. Thereafter, it's added into the list of unverified Apps & it will automatically open just like other verified Apps.

### 3. Unable to use Software requiring x86_64 architecture on M1 Macbook
* Below is the error for `eosio` installation
```
eosio: The intel architecture is required for this software.
Error: An unsatisifed requirement failed this build.
```
* Solution: Follow [this](https://benobi.one/posts/running_brew_on_m1_for_x86/)
  - Install Rosetta (this will fail if your Terminal is set to “Open using Rosetta") by running: `softwareupdate --install-rose`
  - Run this command to install the Intel architecture Homebrew: `arch -x86_64 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
  - Add this to your ZSH config (I recommend using OhMyZSH + add a file called `~/.oh-my-zsh/custom/brew.zsh`) with the contents:
     + `touch ~/.oh-my-zsh/custom/brew.zsh`
  - `export PATH="/opt/homebrew/bin:/usr/local/bin:$PATH"`
  - `alias ibrew='arch -x86_64 /usr/local/bin/brew'`
  - Re-source your zsh term `source ~/.zshrc`
  - Run Intel brew as `ibrew install <whatever>`

### 4. Error: xcrun: error: invalid active developer path
* Reason: After updating MacOS, the CLI needs to be updated.
* Solution: Run `xcode-select --install` in terminal.

### 5. The command is not activated even after `export PATH=$PWD/bin:$PATH`
* Reason: the command is not mentioned into the `~/.zprofile`
* Solution:
  - Open the file in ST editor, `$ subl ~/.zprofile`.
  - add this line `export PATH=$PWD/bin:$PATH` to the End of File (EOF).
  - Run this to activate `$ source ~/.zprofile`
  - Now, use the command in the current/new terminal.

## References
* Apple keyboard shortcuts - https://support.apple.com/en-in/HT201236
* Apple Q & A - https://apple.stackexchange.com/
