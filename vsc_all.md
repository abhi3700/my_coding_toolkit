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
  export PATH="/Applications/Visual Studio Code.app/Contents/Resources/app/bin:$PATH"
  OR
  alias code="open -a /Applications/Visual\ Studio\ Code.app"
  ```
  3. `$ source ~/.zprofile`
  4. Now, use `$ code <folder_or_file_path>` from terminal

## Packages
> This is for MacOS

* [x] [Atom One Light theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onelight)
* [x] [Atom One Dark Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)
* [x] [autoDocstring - Python Docstring Generator](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring)
* [x] [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
* [x] [Better C++ Syntax](https://marketplace.visualstudio.com/items?itemName=jeff-hykin.better-cpp-syntax)
* [x] [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)
* [x] [Better TOML](https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml)
* [x] [C/C++ Advanced Lint](https://marketplace.visualstudio.com/items?itemName=jbenden.c-cpp-flylint)
  - pre-requisite: install `cppcheck` using `$ brew install cppcheck`. Try `$ cppcheck` command on terminal
  - open the global settings <kbd>cmd+,</kbd> >> "Extensions" >> "C/C++ Lint configuration" >> untick these:
  ```
  Flawfinder: Enable
  Flexelint: Enable
  Lizard: Enable
  ```
  which looks like this
  
  <img width="462" alt="image" src="https://user-images.githubusercontent.com/16472948/160075374-64b18202-5dbb-49e4-9cc1-e9fc799d8457.png">

* [x] [CodeSnap](https://marketplace.visualstudio.com/items?itemName=adpyke.codesnap)
<img width="1166" alt="image" src="https://user-images.githubusercontent.com/16472948/163014636-3988cce0-7219-43c4-ad3d-01800af25286.png">

* [x] [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
<img width="253" alt="image" src="https://user-images.githubusercontent.com/16472948/163014762-b5a8fdce-7281-4249-a7b3-bdee8cf3c7a1.png">

* [x] [Color Manager](https://marketplace.visualstudio.com/items?itemName=RoyAction.color-manager)
<img width="832" alt="image" src="https://user-images.githubusercontent.com/16472948/163014306-88928ad8-4ec2-4790-9f9b-381cfa27f764.png">

* [x] [Emoji](https://marketplace.visualstudio.com/items?itemName=Perkovec.emoji)
  - Refer to its usage section
* [x] [ES Lint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint): Linting for JS, TS
* [x] [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  - [Documentation](https://gitlens.amod.io/)
* [x] [Identical Sublime Text Monokai theme](https://marketplace.visualstudio.com/items?itemName=maximetinu.identical-sublime-monokai-csharp-theme-colorizer)
* [x] [Include Autocomplete](https://marketplace.visualstudio.com/items?itemName=ajshort.include-autocomplete)
  - For C/C++ include directive
* [x] [json](https://marketplace.visualstudio.com/items?itemName=ZainChen.json)
* [x] [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
  - Activate this
* [x] [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
* [x] [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
* [x] [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
* [x] [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script) 
* [x] [One Monokai Theme](https://marketplace.visualstudio.com/items?itemName=azemoh.one-monokai)
* [x] [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
* [x] [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=SimonSiefke.prettier-vscode)
* [x] [Pretty js/json](https://marketplace.visualstudio.com/items?itemName=supperchong.pretty-json)
  - Refer "Usage"
* [x] [Python Indent](https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent)
* [x] [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
* [x] [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=matklad.rust-analyzer)
* [x] [Slither](https://marketplace.visualstudio.com/items?itemName=trailofbits.slither-vscode)
* [x] [solidity](https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity)
* [x] [Sublime Oceanic After Next Theme](https://marketplace.visualstudio.com/items?itemName=christophwolff.sublime-oceanic-after-next-theme)
* [x] [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
  - This would enable to work with keyboard shortcuts used in ST
* [x] [Semicolon Insertion Shortcut](https://marketplace.visualstudio.com/items?itemName=chrisvltn.vs-code-semicolon-insertion)
  - <kbd>cmd+shift+p</kbd> >> "Open Keyboard Shortcuts (Default)" >> Search for 'semicolon' >> Toggle the 2 shortcut keys from <kbd>cmd+/</kbd> & <kbd>cmd+shift+/</kbd> to <kbd>cmd+;</kbd> & <kbd>ctrl+shift+;</kbd>
  - There would be another duplicate usage of this keyboard shortcut <kbd>cmd+shift+;</kbd>. Change that to some other shortcut key.
* [x] [TabNine](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode)
* [x] [Terminal Here](https://marketplace.visualstudio.com/items?itemName=Tyriar.vscode-terminal-here)
  -  <kbd>cmd+shift+p</kbd> >> "Open Keyboard Shortcuts (Default)" >> Search for 'terminal here' >> set <kbd>ctrl+shift+t</kbd> as shortcut key
* [x] Work with WSL Ubuntu Server (Applicable for Win OS)  

## Shortcut keys

### Mac OS
> First install the [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), then follow this shortcut keys along with [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/sublime_all.md#shortcut-keys):

* <kbd>cmd+,</kbd> - Open preferences (global)
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
* <kbd>ctrl+w</kbd> - Switch to workspace/window
* <kbd>cmd+shift+.</kbd> - View a navigation pane for a file
* <kbd>opt+ 🔼/🔽</kbd> - Keeping the cursor on a line, use this move the line up or down
* <kbd>cmd+f</kbd> - find in the current file
* <kbd>cmd+shift+f</kbd> - find in the current workspace
* <kbd>cmd+opt+f</kbd> - Replace in the current file
* <kbd>ctrl+spacebar</kbd> - give suggestions at any red color cursor point
* <kbd>cmd+shift+e</kbd> - show the active file in the explorer

### Win OS
> First install the [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), then follow this shortcut keys along with [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/sublime_all.md#shortcut-keys):

* <kbd>ctrl+k+t</kbd>, <kbd>ctrl+t</kbd> - change the color theme
* <kbd>ctrl+shift+p</kbd> - open the command palette
* <kbd>ctrl+`</kbd> - toggle the terminal
* <kbd>ctrl+k,f</kbd - close the opened folder
* <kbd>ctrl+k+b</kbd - toggle the explorer
* <kbd>ctrl+shift+k</kbd - delete the line cursor is at
* press <kbd>ctrl</kbd> & hold - Edit multiple lines at different line no. simultaneously.

## Preferences
* In VSCode, 2 ways to be dependent on settings for a language:
  - global: <kbd>cmd+shift+p</kbd>  >>  "Preferences: Open Settings"
  - local: create a language properties for a repository like "c_cpp_properties.json" inside ".vscode/" folder.

> NOTE: By default, the local settings (if defined) supersedes global settings.

## Languages
### C/C++

#### Package
* Look at the packages to be installed above.

#### Linting
* Maintain this settings in the "Preferences: Open Settings" file (get by typing after pressing key <kbd>cmd+,</kbd>).
<img width="551" alt="image" src="https://user-images.githubusercontent.com/16472948/160159728-4ea3a39f-e0d1-4ac5-8d02-199ff82df64e.png">

##### settings JSON
```json
    "C_Cpp.workspaceSymbols": "All",
    "c-cpp-flylint.flawfinder.enable": false,
    "c-cpp-flylint.flexelint.enable": false,
    "c-cpp-flylint.lizard.enable": false,
    "cmake.configureOnOpen": true,
    "C_Cpp.errorSquiggles": "Disabled",
    "C_Cpp.default.cppStandard": "c++17",
    "C_Cpp.default.includePath": [
        "${workspaceFolder}/**",
        "/Library/Developer/CommandLineTools/usr/include",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/libc",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/libcxx",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/capi",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/contracts",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/core",
        "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/native"
    ],
    // "c-cpp-flylint.includePaths": [
    //     "${workspaceFolder}/**",
    //     "/Library/Developer/CommandLineTools/usr/include",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/libc",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/libcxx",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/capi",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/contracts",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/core",
    //     "/usr/local/Cellar/eosio.cdt/1.8.1/opt/eosio.cdt/include/eosiolib/native"
    // ],
    "include-autocomplete.extensions": [
        "",
        ".h",
        ".hpp",
        ".hxx",
        ".cpp"
    ],
```

Commented "c-cpp-flylint.includePaths" because it is not linting the imp. ones.

#### Compiler
* Use this compiler based on OS:
  - Mac: `clang`
  - Linux (using WSL): `g++`
* In Mac, `clang` uses this directory for compiling: "/Library/Developer/CommandLineTools/usr/include/".
* In order to put some custom lib or folder like `boost`, download the folder from [here](https://www.boost.org/users/download/) & paste into this directory: "/Library/Developer/CommandLineTools/usr/include/"

#### Lib
- [Boost](https://www.boost.org/users/download/)

#### Output
* TODO also looks in good color like this
<img width="705" alt="image" src="https://user-images.githubusercontent.com/16472948/160118920-6db571d9-20a5-4cb8-9122-768a8406ea87.png">

#### Others
* More config commands: https://code.visualstudio.com/docs/cpp/customize-default-settings-cpp

### Rust
* Add the static analyzer package above.

### TypeScript
#### Package
* Look at the packages to be installed above.

#### Linting
* ESLint package automatically ensures linting on typescript in vscode
  - @pre
    - First install the compiler as per [this](https://github.com/abhi3700/My_Learning-Typescript/blob/main/README.md#macos)

#### Compiler
* [Installation](https://github.com/abhi3700/My_Learning-Typescript/blob/main/README.md#macos)

#### Lib

### Python
* Add the packages above.

### TypeScript
#### Package
* Look at the packages to be installed above.

#### Linting
* Python (by Microsoft) provides linting, suggestion

#### Compiler
* [Installation](https://www.anaconda.com/)

#### Lib

### JSON
#### Package
* Look at the packages to be installed above.
