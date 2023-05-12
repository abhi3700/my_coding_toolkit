# Visual Studio Code

My favourite editors: ST, VSC

## Installation

> For Mac OS & Win OS

- Add to terminal [source](https://stackoverflow.com/a/36882426)

```
1. Open VSC & type `cmd+shift+p`
2. Type "Shell" & select 'Shell Command : Install code in PATH'
3. Use `$ code <project-folder-name>`
```

- For permanence, follow this:
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

## Extensions

In macOS, I can get the list of packages here: `~/.vscode/extensions` in local PC.

last updated on `17-06-2022`

For remote desktop, I just need to sync after login, then all the extensions would be synced, provided I have "Settings Sync" turned on in my source PC.

<details>
  <summary><b>Expand: </b></summary>
		
```
aaron-bond.better-comments-3.0.0
adpyke.codesnap-1.3.4
ajshort.include-autocomplete-0.0.4
akamud.vscode-theme-onedark-2.2.3
akamud.vscode-theme-onelight-2.2.3
appland.appmap-0.31.0
appland.appmap-0.31.1
azemoh.one-monokai-0.5.0
bierner.markdown-mermaid-1.14.2
bierner.markdown-preview-github-styles-1.0.1
bungcip.better-toml-0.3.2
chrisdias.vscode-opennewinstance-0.0.12
christian-kohler.npm-intellisense-1.4.2
christian-kohler.path-intellisense-2.8.1
christophwolff.sublime-oceanic-after-next-theme-0.0.2
chrisvltn.vs-code-semicolon-insertion-0.0.6
contractshark.solidity-lang-1.4.0
cschlosser.doxdocgen-1.4.0
cssho.vscode-svgviewer-2.0.0
dakshmiglani.hex-to-rgba-1.0.0
davidanson.vscode-markdownlint-0.47.0
dbaeumer.vscode-eslint-2.2.2
dendron.dendron-paste-image-1.1.0
dunstontc.vscode-rust-syntax-0.0.32
eamodio.gitlens-12.1.1
eg2.vscode-npm-script-0.3.25
ericadamski.carbon-now-sh-1.2.0
esbenp.prettier-vscode-9.5.0
fabiospampinato.vscode-markdown-todo-1.1.1
fabiospampinato.vscode-todo-plus-4.18.4
felipe-mendes.slack-theme-1.9.17
formulahendry.auto-close-tag-0.5.14
gimenete.github-linker-0.2.5
gordonlarrigan.vscode-kanbn-0.11.0
grapecity.gc-excelviewer-4.2.55
gruntfuggly.calendar-0.0.13
gruntfuggly.mermaid-export-0.0.8
haaleo.timing-2.7.1
hediet.vscode-drawio-1.6.4
izaxon.todo-0.1.0
jebbs.plantuml-2.17.3
jeff-hykin.better-cpp-syntax-1.15.18
jgclark.vscode-todo-highlight-2.0.4
jithurjacob.nbpreviewer-1.2.2
joaompinto.vscode-graphviz-0.0.6
josetr.cmake-language-support-vscode-0.0.4
jrtools.mariana-1.0.8
juanblanco.solidity-0.0.139
kelvin.vscode-sshfs-1.25.0
kevinrose.vsc-python-indent-1.17.0
llvm-vs-code-extensions.vscode-clangd-0.1.17
maximetinu.identical-sublime-monokai-csharp-theme-colorizer-1.1.0
mechatroner.rainbow-csv-2.4.0
mikestead.dotenv-1.0.1
mkloubert.vscode-kanban-1.33.0
ms-azuretools.vscode-docker-1.22.0
ms-dotnettools.vscode-dotnet-runtime-1.5.0
ms-python.python-2022.8.0
ms-python.vscode-pylance-2022.6.30
ms-toolsai.jupyter-2022.5.1001601848
ms-toolsai.jupyter-keymap-1.0.0
ms-toolsai.jupyter-renderers-1.0.8
ms-toolsai.vscode-jupyter-powertoys-0.0.3
ms-vscode-remote.remote-containers-0.238.2
ms-vscode-remote.remote-ssh-0.82.1
ms-vscode-remote.remote-ssh-0.82.1.vsix
ms-vscode-remote.remote-ssh-edit-0.80.0
ms-vscode-remote.remote-wsl-0.66.3
ms-vscode.cmake-tools-1.11.26
ms-vscode.cpptools-1.10.7-darwin-arm64
ms-vscode.cpptools-extension-pack-1.2.0
ms-vscode.cpptools-themes-1.0.0
ms-vscode.hexeditor-1.9.7
ms-vscode.js-debug-companion-1.0.18
ms-vscode.references-view-0.0.89
ms-vscode.sublime-keybindings-4.0.10
mythx.mythxvsc-0.7.21
naumovs.color-highlight-2.5.0
njpwerner.autodocstring-0.6.1
nomicfoundation.hardhat-solidity-0.4.3
perkovec.emoji-1.0.1
pkief.material-icon-theme-4.18.1
royaction.color-manager-0.7.5
rust-lang.rust-analyzer-0.3.1099-darwin-arm64
rust-lang.rust-analyzer-0.3.1107-darwin-arm64
ryu1kn.partial-diff-1.4.3
smh.eosio-0.0.1
softwaredotcom.swdc-vscode-2.6.31
softwaredotcom.swdc-vscode-2.6.32
streetsidesoftware.code-spell-checker-2.2.5
supperchong.pretty-json-0.0.4
tabnine.tabnine-vscode-3.5.58
tabnine.tabnine-vscode-3.5.59
tintinweb.ethereum-security-bundle-0.0.6
tintinweb.graphviz-interactive-preview-0.3.0
tintinweb.solidity-metrics-0.0.20
tintinweb.solidity-visual-auditor-0.1.2
tintinweb.vscode-ethover-0.0.7
tintinweb.vscode-inline-bookmarks-0.0.26
tintinweb.vscode-lll-0.0.7
tintinweb.vscode-solidity-flattener-0.0.11
tintinweb.vscode-solidity-language-0.0.6
tintinweb.vscode-vyper-0.0.13
tomoki1207.pdf-1.2.0
trailofbits.slither-vscode-0.0.7
twxs.cmake-0.0.17
tyriar.luna-paint-0.15.0
tyriar.vscode-terminal-here-0.2.4
visualstudioexptteam.vscodeintellicode-1.2.21
vitelabs.soliditypp-0.7.11
vitelabs.solppdebugger-0.2.5
wakatime.vscode-wakatime-18.1.6
yzhang.markdown-all-in-one-3.4.3
zainchen.json-2.0.2
```	
		
</details>

## Packages

> This is for MacOS. <kbd>**Not updated with Latest**</kbd>, refer to the list.

- [x] [Atom One Light theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onelight)
- [x] [Atom One Dark Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)
- [x] [autoDocstring - Python Docstring Generator](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring)
- [x] [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
- [x] [Better C++ Syntax](https://marketplace.visualstudio.com/items?itemName=jeff-hykin.better-cpp-syntax)
- [x] [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)
- [x] [Better TOML](https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml)
- [x] [C/C++ Advanced Lint](https://marketplace.visualstudio.com/items?itemName=jbenden.c-cpp-flylint)

  - pre-requisite: install `cppcheck` using `$ brew install cppcheck`. Try `$ cppcheck` command on terminal
  - open the global settings <kbd>cmd+,</kbd> >> "Extensions" >> "C/C++ Lint configuration" >> untick these:

  ```
  Flawfinder: Enable
  Flexelint: Enable
  Lizard: Enable
  ```

  which looks like this

  <img width="462" alt="image" src="https://user-images.githubusercontent.com/16472948/160075374-64b18202-5dbb-49e4-9cc1-e9fc799d8457.png">

- [x] [carbon-now-sh](https://marketplace.visualstudio.com/items?itemName=ericadamski.carbon-now-sh)
- [x] [CodeSnap](https://marketplace.visualstudio.com/items?itemName=adpyke.codesnap)
      <img width="1166" alt="image" src="https://user-images.githubusercontent.com/16472948/163014636-3988cce0-7219-43c4-ad3d-01800af25286.png">

- [x] [Code Time](https://marketplace.visualstudio.com/items?itemName=softwaredotcom.swdc-vscode)
- [x] [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
      <img width="253" alt="image" src="https://user-images.githubusercontent.com/16472948/163014762-b5a8fdce-7281-4249-a7b3-bdee8cf3c7a1.png">

- [x] [Color Manager](https://marketplace.visualstudio.com/items?itemName=RoyAction.color-manager)
      <img width="832" alt="image" src="https://user-images.githubusercontent.com/16472948/163014306-88928ad8-4ec2-4790-9f9b-381cfa27f764.png">

- [x] [Emoji](https://marketplace.visualstudio.com/items?itemName=Perkovec.emoji)
  - Refer to its usage section
- [x] [ES Lint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint): Linting for JS, TS
- [x] [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  - [Documentation](https://gitlens.amod.io/)
- [x] [Identical Sublime Text Monokai theme](https://marketplace.visualstudio.com/items?itemName=maximetinu.identical-sublime-monokai-csharp-theme-colorizer)
- [x] [Include Autocomplete](https://marketplace.visualstudio.com/items?itemName=ajshort.include-autocomplete)
  - For C/C++ include directive
- [x] [json](https://marketplace.visualstudio.com/items?itemName=ZainChen.json)
- [ ] [Kanban Board](https://marketplace.visualstudio.com/items?itemName=mkloubert.vscode-kanban)
- [x] [Kanbn Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=gordonlarrigan.vscode-kanbn)
- [x] [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
  - Activate this
- [x] [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [x] [Markdown Preview Mermaid Support](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)
- [x] [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
- [x] [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
- [x] [Markdown Todo](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-markdown-todo)
- [x] [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
- [x] [One Monokai Theme](https://marketplace.visualstudio.com/items?itemName=azemoh.one-monokai)
- [x] [Open Folder Context Menus for VS Code](https://marketplace.visualstudio.com/items?itemName=chrisdias.vscode-opennewinstance)
- [x] [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- [x] [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [x] [Pretty js/json](https://marketplace.visualstudio.com/items?itemName=supperchong.pretty-json)
  - Refer "Usage"
- [x] [Python Indent](https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent)
- [x] [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- [x] [Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv)
- [x] [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=matklad.rust-analyzer)
- [x] [Slither](https://marketplace.visualstudio.com/items?itemName=trailofbits.slither-vscode)
- [x] [solidity](https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity)
- [x] [Sublime Oceanic After Next Theme](https://marketplace.visualstudio.com/items?itemName=christophwolff.sublime-oceanic-after-next-theme)
- [x] [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
  - This would enable to work with keyboard shortcuts used in ST
- [x] [Semicolon Insertion Shortcut](https://marketplace.visualstudio.com/items?itemName=chrisvltn.vs-code-semicolon-insertion)

  - <kbd>cmd+shift+p</kbd> >> "Open Keyboard Shortcuts (Default)" >> Search for 'semicolon' >> Toggle the 2 shortcut keys from <kbd>cmd+/</kbd> & <kbd>cmd+shift+/</kbd> to <kbd>cmd+;</kbd> & <kbd>ctrl+shift+;</kbd>
  - There would be another duplicate usage of this keyboard shortcut <kbd>cmd+shift+;</kbd>. Change that to some other shortcut key.

- [x] [TabNine](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode)
- [x] [Terminal Here](https://marketplace.visualstudio.com/items?itemName=Tyriar.vscode-terminal-here)
  - <kbd>cmd+shift+p</kbd> >> "Open Keyboard Shortcuts (Default)" >> Search for 'terminal here' >> set <kbd>ctrl+shift+t</kbd> as shortcut key
- [x] [Time Converter](https://marketplace.visualstudio.com/items?itemName=HaaLeo.timing)
- [x] [todo](https://marketplace.visualstudio.com/items?itemName=izaxon.todo)
- [x] [Todo+](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-todo-plus)
- [x] [TODO Highlight v2](https://marketplace.visualstudio.com/items?itemName=jgclark.vscode-todo-highlight)
- [x] [WakaTime](https://marketplace.visualstudio.com/items?itemName=WakaTime.vscode-wakatime)
- [x] Work with WSL Ubuntu Server (Applicable for Win OS)

## Shortcut keys

### Mac OS

[keyboard-shortcuts-all-macos](./docs/keyboard-shortcuts-macos.pdf)

> First install the [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), then follow this shortcut keys along with [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/sublime_all.md#shortcut-keys):

- <kbd>cmd+,</kbd> - Open preferences (global)
- <kbd>cmd+k+t</kbd>, <kbd>ctrl+t</kbd> - change the color theme
- <kbd>cmd+shift+p</kbd> - open the command palette
- <kbd>cmd+shift+c</kbd> - open the terminal in the directory of root folder (opened)
- <kbd>ctrl+`</kbd> - toggle the terminal (integrated)
- <kbd>ctrl+l</kbd> - select multiple lines
- <kbd>ctrl+shift+l</kbd> - edit multiple lines at a time
- <kbd>cmd+k,f</kbd> - close the opened folder
- <kbd>cmd+k+b</kbd> - toggle the explorer
- <kbd>cmd+shift+k</kbd> - delete the line cursor is at
- press <kbd>cmd</kbd> & hold - Edit multiple lines at different line no. simultaneously.
- <kbd>cmd+opt+1</kbd> - Only one screen
- <kbd>cmd+opt+2</kbd> - 2 screens side by side. In order to have 3 screens, just select one file opened & then press this shortcut key.
- <kbd>ctrl+g</kbd> - Go to a line
- <kbd>cmd+shift+f</kbd> - Find all references of a function in entire project files.
- <kbd>opt+click</kbd> - Go to the file, function (definition), folder directly
- <kbd>fn+F12</kbd>: Go to the definition of the function or just use the above shortcut key.
- <kbd>ctrl+w</kbd> - Switch to workspace/window
- <kbd>cmd+shift+.</kbd> - View a navigation pane for a file
- <kbd>opt+ 🔼/🔽</kbd> - Keeping the cursor on a line, use this move the line up or down
- <kbd>cmd+f</kbd> - find in the current file
- <kbd>cmd+shift+f</kbd> - find in the current workspace
- <kbd>cmd+opt+f</kbd> - Replace in the current file
- <kbd>ctrl+spacebar</kbd> - give suggestions at any red color cursor point
- <kbd>cmd+shift+e</kbd> - show the active file in the explorer
- <kbd>cmd+k</kbd>, <kbd>s</kbd> - Here, save file without formatting. Normally, if the formatter is enabled for the file extension type in the VSCode Settings, then when doing <kbd>cmd+s</kbd>, the file is saved with formatting automatically.
- Open sub-folder in new window using this [package](https://marketplace.visualstudio.com/items?itemName=chrisdias.vscode-opennewinstance)
- <kbd>cmd+opt+=</kbd>: zoom-in
- <kbd>cmd+opt+-</kbd>: zoom-out

### Win OS

> First install the [Sublime Text Keymap and Settings Importer](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), then follow this shortcut keys along with [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/sublime_all.md#shortcut-keys):

- <kbd>ctrl+k+t</kbd>, <kbd>ctrl+t</kbd> - change the color theme
- <kbd>ctrl+shift+p</kbd> - open the command palette
- <kbd>ctrl+`</kbd> - toggle the terminal
- <kbd>ctrl+k,f</kbd - close the opened folder
- <kbd>ctrl+k+b</kbd - toggle the explorer
- <kbd>ctrl+shift+k</kbd - delete the line cursor is at
- press <kbd>ctrl</kbd> & hold - Edit multiple lines at different line no. simultaneously.

## Preferences

- In VSCode, 2 ways to be dependent on settings for a language:
  - global: <kbd>cmd+shift+p</kbd> >> "Preferences: Open Settings"
  - local: create a language properties for a repository like "c_cpp_properties.json" inside ".vscode/" folder.

> NOTE: By default, the local settings (if defined) supersedes global settings.

## Formatter

In VSCode, select the default formatter with this [package](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) for all files (sol, ts, js, md, py, java, cpp)

**Procedure**:

[YouTube](https://www.youtube.com/watch?v=PX6xb8sRlFc)

- Open Settings
- type 'save format' >> tick the "Editor: Format on Save"
- type 'formatter' >> set the "Editor: Default Formatter" to Prettier (by esbenp....)
- type 'solidity formatter' >> set the "Solidity: Formatter" from `none` to `prettier`
- Now, on saving any solidity (`*.sol`) file, it will automatically format.

## Languages

### C/C++

#### Package

- Look at the packages to be installed above.

#### Linting

- Maintain this settings in the "Preferences: Open Settings" file (get by typing after pressing key <kbd>cmd+,</kbd>).
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

- Use this compiler based on OS:
  - Mac: `clang`
  - Linux (using WSL): `g++`
- In Mac, `clang` uses this directory for compiling: "/Library/Developer/CommandLineTools/usr/include/".
- In order to put some custom lib or folder like `boost`, download the folder from [here](https://www.boost.org/users/download/) & paste into this directory: "/Library/Developer/CommandLineTools/usr/include/"

#### Lib

- [Boost](https://www.boost.org/users/download/)

#### Output

- TODO also looks in good color like this
  <img width="705" alt="image" src="https://user-images.githubusercontent.com/16472948/160118920-6db571d9-20a5-4cb8-9122-768a8406ea87.png">

#### Others

- More config commands: https://code.visualstudio.com/docs/cpp/customize-default-settings-cpp

### Rust

- Add the static analyzer package above.

### TypeScript

#### Package

- Look at the packages to be installed above.

#### Linting

- ESLint package automatically ensures linting on typescript in vscode
  - @pre
    - First install the compiler as per [this](https://github.com/abhi3700/My_Learning-Typescript/blob/main/README.md#macos)

#### Compiler

- [Installation](https://github.com/abhi3700/My_Learning-Typescript/blob/main/README.md#macos)

#### Lib

### Python

- Add the packages above.

### TypeScript

#### Package

- Look at the packages to be installed above.

#### Linting

- Python (by Microsoft) provides linting, suggestion

#### Compiler

- [Installation](https://www.anaconda.com/)

#### Lib

### JSON

#### Package

- Look at the packages to be installed above.

### TODO

How to manage todo inside VSC

#### key shortcuts

- <kbd>cmd+enter</kbd> / <kbd>opt+enter</kbd>: toggle TODO
- <kbd>opt+s</kbd>: toggle start of task
- <kbd>opt+d</kbd>: toggle end of task
- <kbd>cmd+shift+p</kbd>: open command palette & then:
  - "Todo: Toggle Cancelled" to cancel (the task on which the cursor was)
  - "TODO-highlight: List highlighted annotations" to show all the TODOs in the workspace.

#### Package

- Look at the packages to be installed above.

## Troubleshoot

In case where the terminal font style gets changed (during sync for multiple machines), then do this:

Go to `settings.json` file via <kbd>cmd+shift+p</kbd>/<kbd>ctrl+shift+p</kbd>: `Preferences: Open Settings (JSON)`

just change/**remove** this line:

```json
    "terminal.integrated.fontFamily": "Menlo, Monaco, 'Courier New', monospace",
```
