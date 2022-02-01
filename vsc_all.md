# Visual Studio Code

My favourite editors: ST, VSC

## Installation
> For Mac OS & Win OS

* Add to terminal [source](https://stackoverflow.com/a/36882426)
```
1. Open VSC & type `cmd+shift+p`
2. Type "Shell" & select 'Shell Command : Install code in PATH'
3. Use `$ code <project-folder-name>`
```
* For permanence, follow this:
  1. Open profile in `$ subl ~/.zprofile`
  2. Add this line
```
# install code on terminal
export PATH="/usr/local/bin/code:$PATH"
```
  3. `$ source ~/.zprofile`
  4. Now, use `$ code <folder_or_file_path>` from terminal

## Packages
> This is for MacOS

* [x] [Atom One Light theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onelight)
* [x] [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
* [x] [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=SimonSiefke.prettier-vscode) 
* [x] [Slither](https://marketplace.visualstudio.com/items?itemName=trailofbits.slither-vscode)
* [x] [solidity](https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity)
* [x] [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
  - This would enable to work with keyboard shortcuts used in ST
* [x] Work with WSL Ubuntu Server (Applicable for Win OS)
* [x] [Semicolon Insertion Shortcut](https://marketplace.visualstudio.com/items?itemName=chrisvltn.vs-code-semicolon-insertion)
  - <kbd>cmd+shift+p</kbd> >> "Open Keyboard Shortcuts (Default)" >> Search for 'semicolon' >> Toggle the 2 shortcut keys from <kbd>cmd+/</kbd> & <kbd>cmd+shift+/</kbd> to <kbd>cmd+;</kbd> & <kbd>cmd+shift+;</kbd>
  - There would be another duplicate usage of this keyboard shortcut <kbd>cmd+shift+;</kbd>. Change that to some other shortcut key.

## Shortcut keys (Mac OS)
> First install the [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), then follow this shortcut keys along with [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/sublime_all.md#shortcut-keys):

* <kbd>cmd+k+t</kbd>, <kbd>ctrl+t</kbd> - change the color theme
* <kbd>cmd+shift+p</kbd> - open the command palette
* <kbd>ctrl+`</kbd> - toggle the terminal
* <kbd>ctrl+l</kbd> - select multiple lines
* <kbd>ctrl+shift+l</kbd> - edit multiple lines at a time
* <kbd>cmd+k,f</kbd> - close the opened folder
* <kbd>cmd+k+b</kbd> - toggle the explorer
* <kbd>cmd+shift+k</kbd> - delete the line cursor is at
* press <kbd>cmd</kbd> & hold - Edit multiple lines at different line no. simultaneously.
* <kbd>cmd+opt+1</kbd> - Only one screen
* <kbd>cmd+opt+2</kbd> - 2 screens side by side. In order to have 3 screens, just select one file opened & then press this shortcut key.
* <kbd>ctrl+g</kbd> - Go to a line
* <kbd>cmd+shift+f</kbd> - Find all references of a function in entire project files.
* <kbd>opt+click</kbd> - Go to the file, function, folder directly

## Shortcut keys (Win OS)
> First install the [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), then follow this shortcut keys along with [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/sublime_all.md#shortcut-keys):

* <kbd>ctrl+k+t</kbd>, <kbd>ctrl+t</kbd> - change the color theme
* <kbd>ctrl+shift+p</kbd> - open the command palette
* <kbd>ctrl+`</kbd> - toggle the terminal
* <kbd>ctrl+k,f</kbd - close the opened folder
* <kbd>ctrl+k+b</kbd - toggle the explorer
* <kbd>ctrl+shift+k</kbd - delete the line cursor is at
* press <kbd>ctrl</kbd> & hold - Edit multiple lines at different line no. simultaneously.
