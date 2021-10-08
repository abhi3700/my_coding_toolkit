## About
This is a editor cum IDE used for any format of file.

**Website** - https://www.sublimetext.com/

**System (described here):** Windows 10

## Documentation
link - http://docs.sublimetext.info/en/latest/index.html

## Installation
1. ### Sublime Text 3
I prefer using Win 10. So, install on Win 10 & then connect WSL by creating shortcut to the ubuntu repo "/usr/local/bin/subl"

Follow the steps:
* Install from the link - https://www.sublimetext.com/3
* make the shortcut link on ubuntu using `ln -s "/mnt/f/Softwares/Sublime Text 3/subl.exe" /usr/local/bin/subl`
* use `subl` on bash-cmd

2. ### Sublime Merge
A Git Client
* Install from [here](https://www.sublimemerge.com/download)

### Context Menu
> NOTE: DON'T Forget to tick the option.

If missed, follow this workaround below:
* Create a .bat file with ST3.
* Copy and Paste this code:
```console
@echo off
SET st3Path=C:\Program Files\Sublime Text 3\sublime_text.exe
 
rem add it for all file types
@reg add "HKEY_CLASSES_ROOT\*\shell\Open with Sublime Text 3"         /t REG_SZ /v "" /d "Open with Sublime Text 3"   /f
@reg add "HKEY_CLASSES_ROOT\*\shell\Open with Sublime Text 3"         /t REG_EXPAND_SZ /v "Icon" /d "%st3Path%,0" /f
@reg add "HKEY_CLASSES_ROOT\*\shell\Open with Sublime Text 3\command" /t REG_SZ /v "" /d "%st3Path% \"%%1\"" /f
 
rem add it for folders
@reg add "HKEY_CLASSES_ROOT\Folder\shell\Open with Sublime Text 3"         /t REG_SZ /v "" /d "Open with Sublime Text 3"   /f
@reg add "HKEY_CLASSES_ROOT\Folder\shell\Open with Sublime Text 3"         /t REG_EXPAND_SZ /v "Icon" /d "%st3Path%,0" /f
@reg add "HKEY_CLASSES_ROOT\Folder\shell\Open with Sublime Text 3\command" /t REG_SZ /v "" /d "%st3Path% \"%%1\"" /f
pause
```
* Now, "Run as Administrator"
* DONE!

## Uninstallation
* All the extra packages are installed in "click Browse Packages".
* So, during uninstall, make a copy of the Sublime Text3 in other drives (E/ F/ G). Location - "C:\Users\abhijit\AppData\Roaming\Sublime Text 3".
* After re-install, copy the folder into the location of the 'Browse Packages'

### Shortcuts
* CMD: <br/>
	In cmd, bash-cmd, use `subl -h` to show the docs.
	- `subl -n hello.cpp`: opens a file in new ST3 window.
	
* <kbd>ctrl + p</kbd> - find anything within the workspace.
  * `eosio.hpp:5` - this takes to line 5 of "eosio.hpp" file.
* <kbd>alt + shift + 2</kbd> -  split the view into 2
* <kbd>ctrl + shift + p</kbd> - command palette i.e. manually install packages, Project:Save, Project:close, set:java, set:javascript, so on and so forth.
* 'Double click' will open the file (among the open side bar) and show in the "OPEN FILES". <br/>
  'Single click' will just open the file.

### Preferences
* `Preferences -> Settings - Default/User`: for all files
* `Preferences -> Settings - Syntax Specific`: for that language. `E.g. - Python.sublime-settings`
* Convert tabs to spaces: set this
```json
    "tab_size": 4,
    "translate_tabs_to_spaces": false,
```
* "Settings": set 
```json
{
  "line_padding_top": 1,
  "line_padding_bottom": 1
}
```
* `ctrl+P` - Type 
  - `@` to jump to symbols, 
  - `#` to search within the file, and 
  - `:` to go to a line number

### Packages
Just <kbd>ctrl + shift + p</kbd> and type the package name and enter. It will install thereafter. 
If not found, then manually download the .zip file into the directory "Preferences >> Browse packages". Then restart the sublime App.

* [x] A File Icon - https://github.com/ihodev/a-file-icon
* [x] Anaconda
* [x] [AppendSemiColon](https://packagecontrol.io/packages/AppendSemiColon): On windows, <kbd>ctrl + ;</kbd> for inserting semicolon and <kbd>ctrl + shift + ;</kbd> to insert both semicolon and newline.
* [x] Auto Refresh
* [x] AutoFileName
* [x] [C++ Snippets](https://packagecontrol.io/packages/C%2B%2B%20Snippets)
* [x] [CMake](https://packagecontrol.io/packages/CMake)
* [x] [CMakeEditor](https://packagecontrol.io/packages/CMakeEditor)
* [x] [CMakeSnippets](https://packagecontrol.io/packages/CMakeSnippets)
* [x] Color Schemes & Themes
	- __Dark__
		+ Color scheme: `Monokai` (installed by default)
		+ Theme: `Default`
	- __Light__ (adjust the brightness of the screen to 50 (contrast, brightness))
		+ [x] Color scheme:
			+ [x] `one-light`
				1. Download zip from [here](https://github.com/abhi3700/one)
				2. Select "Preferences" >> "Browse Packages..." >> "extract the zip folder here as 'one-master'"
				3. In ST, "Preferences" >> "Select Color Scheme" >> "Select One Light"
				4. Done!
			+ [ ]`sixteen` light 
			+ [ ]`ayu`-light (Install `ayu`)
		+ Theme: `Adaptive`
* [x] Comment-Snippets
* [x] Conda
* [ ] [CppFastOlympicCoding](https://packagecontrol.io/packages/CppFastOlympicCoding) - 
	compile in a unique way (in the sidebar on right side using unique test cases). Demo on the package link. Use <kbd>ctrl + alt + b</kbd> to debug, compile, test.
	> NOTE: It will work only if the g++ installation is done.
* [x] DoxyDoc: C++ description about any method, class, template. [Usages](https://packagecontrol.io/packages/DoxyDoc) in animation form.
* [x] EasyWorkspace - [link](https://packagecontrol.io/packages/EasyWorkspace)
  ```
  Save Workspace    | ctrl+alt+s       | Save open files and folders as an easy workspace
  Save As Workspace | ctrl+alt+shift+s | Save easy workspace to specified file
  Open Workspace    | ctrl+alt+o       | Open an existing workspace
  ```
* [x] [Ethereum](https://packagecontrol.io/packages/Ethereum)
	- Enable by using "View >> Syntax >> Ethereum >> Solidity" on `.sol` file.
* [x] FuzzyFileNav
* [x] FuzzyFilePath
* [x] [Git Savvy](https://packagecontrol.io/packages/GitSavvy) - Full git and GitHub integration with ST3.
* [x] [Include Autocomplete](https://packagecontrol.io/packages/Include%20Autocomplete) - for C++ files (in particular) to find out files inside folders. e.g. inside `#include " "`, use `../` to search for files and also other files inside different folders.
	NOTE: It has to be applied in workspace i.e. open a folder and import any files within a sub-folder using the above technique.
* [x] Javascript Completions
* [x] Kite: [Download](https://kite.com/download/), [kite for sublime](https://kite.com/integrations/sublime-text/), [Configuring the Sublime Text plugin](https://help.kite.com/article/72-configuring-the-sublime-text-plugin), [Using the Sublime Text plugin](https://help.kite.com/article/76-using-the-sublime-text-plugin), [Disable Anaconda & then activate Kite](https://help.kite.com/article/81-kite-and-anaconda)
	- To disable Anaconda's autocompletions and signatures, click on Preferences → Package Settings → Anaconda → Settings - User. In the opened settings file, add the following configurations:
```
{
  "disable_anaconda_completion": true,
  "display_signatures": false
} 
```
* [ ] MarkdownLivePreview: In the command palette, type "markdownlivepreview" and go to markdownlivepreview.preferences and toggle "keep on preview" as true.
* [x] [MarkdownPreview](https://packagecontrol.io/packages/MarkdownPreview). After install, for `key binding` i.e shortcut key, `Preferences >> Key Bindings`, add this line `{ "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} },` on `Win` or `{ "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} },` on `MacOS`. Now, press `alt+m` (Win) or `option+m` (Mac) to preview in browser.
* [x] [MarkdownTOC](https://github.com/naokazuterada/MarkdownTOC)
* [x] MarkdownWriter
* [x] PlainTasks
* [x] RTagsComplete
* [x] SideBarEnhancements
* [x] [Solidity Docstring Generator](https://packagecontrol.io/packages/Solidity%20Docstring%20Generator)
	- Enable via "<kbd>ctrl+shift+p</kbd> >> type "Generate..." >> Click on it"
* [x] Stackoverflow Snippets
* [x] Stackoverflow Debug Helper
* [x] SublimeLinter: [link](https://packagecontrol.io/packages/SublimeLinter) The code linting framework for Sublime Text 3 (for all languages)
* [x] SublimeLinter-gcc: [link](https://packagecontrol.io/packages/SublimeLinter-gcc) This linter plugin for SublimeLinter provides an interface to gcc or other gcc-like (cross-)compiler.
* [x] TabNine: A Deep learning based package for autocompletion of code. [More](https://tabnine.com/install)
* [x] Terminal: open terminal at the current folder of the opened file. Access by right clicking and choose the option "Open terminal here". By default it opens the Windows cmd. But to open the bash cmd, follow this: Preferences >> Package Settings >> Terminal >> Settings-Default. And then <br/>
  **Linux (Ubuntu):** add this `"terminal": "C:/Windows/System32/bash.exe",` i.e. bash executable location. <br/>
  **Windows:** Just add this `"terminal": "C:\\Windows\\System32\\cmd.exe",` i.e. cmd executable location.
* [x] Theme - Primer (A UI + syntax theme for @SublimeText inspired by GitHub's UI.): [Package control url](https://packagecontrol.io/packages/Theme%20-%20Primer)
* [x] Toggle Read-Only
* [x] Translate - downloaded from [here](https://github.com/desislavsd/translate) and extracted to (..Roaming\Sublime Text 3\Packages\) <br/>
	<kbd>ctrl+alt+g</kbd> - Select text and use this key shortcut.
* [x] Typescript Syntax
* [x] Vue Syntax Highlight
* [x] Vuejs Complete Package
* [x] WebAssembly Text Syntax
* Markdown Extended
* JSON Comma
* Ethereum
* EthereumSoliditySnippets
* Rainglow theme

### Shortcut keys
#### Windows
After the above packages are installed, use the following personalized shortcut keys:
* <kbd>ctrl + o</kbd> - open files, folders.
* <kbd>ctrl + s</kbd> - save the file.
* <kbd>ctrl + shift + s</kbd> - "save as" the file.
* <kbd>ctrl + tab</kbd> - switch b/w tabs in a panel.
* <kbd>alt + shift + 1</kbd> - view layout single. 
* <kbd>alt + shift + 2</kbd> - view layout double. Like this, so on and so forth.
* <kbd>ctrl + 1</kbd> - switch to panel 1.
* <kbd>ctrl + 2</kbd> - switch to panel 2.
* <kbd>ctrl + alt + s</kbd> - save the workspace with opened folder.
* <kbd>ctrl + alt + o</kbd> - open the saved workspaces (all will appear in the palette).
* <kbd>ctrl + shift + p</kbd> - open the command palette.
* <kbd>ctrl + p</kbd> - open any files from the workspace (chosen folder).
* <kbd>ctrl + shift + p</kbd> >> "install package" --> install any package available.
* <kbd>ctrl + alt + b</kbd> - debug, compile, test C++ program. [NOTE: `cppfastcoding` package should be installed first.]
* <kbd>ctrl + shift + t</kbd> - open terminal in that directory location, provided all the above (ticked) packages are installed.
* <kbd>ctrl + g </kbd> - Go to a line number.
* <kbd>ctrl + shift + k</kbd> - Delete current line
* <kbd>ctrl + r</kbd> - lists all functions and classes within a file to make them easier to find. Simply start typing the one you want.

#### MacOS
After the above packages are installed, use the following personalized shortcut keys:
* Follow [this](https://sublime-text-unofficial-documentation.readthedocs.io/en/sublime-text-2/reference/keyboard_shortcuts_osx.html#editing)

For more, click [here](https://shortcutworld.com/Sublime-Text/win/Sublime-Text_Shortcuts)

## Custom
### Key Bindings
```key
[
	{ "keys": ["ctrl+t"], "command": "new_file" },
	{ "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} },
	{ "keys": ["ctrl+shift+o"], "command": "prompt_open_folder" },	
	{ "keys": ["ctrl+alt+e"], "command": "open_dir", "args": {"dir": "$file_path", "file": "$file_name"} }
]
```

### Snippet
Anytime, a custom snippet might be needed in order to automate a lot of code.

Follow these steps:
* Open a new snippet - `Tools >> Developer >> New Snippet`
* For meaning of each tag, refer [video](https://www.youtube.com/watch?v=zS_4yLizMBw), [article](https://medium.freecodecamp.org/a-guide-to-preserving-your-wrists-with-sublime-text-snippets-7541662a53f2), [examples](https://github.com/Rapptz/cpp-sublime-snippet).
* I created my own version. E.g.
```xml
<snippet>
	<description>eosc - CONTRACT</description>
	<content><![CDATA[
CONTRACT ${1:/*class_name*/} : public eosio::contract {
public:
	using contract::contract;
	${1}( name self ) : contract(self) {}

private:

};
]]></content>
	<!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
	<tabTrigger>eosc</tabTrigger>
	<!-- Optional: Set a scope to limit where the snippet will trigger -->
	<scope>source.c++</scope>
</snippet>
```
* This is how, one can create any snippet as per the need.

### Build System
Create your custom build file to compile any type of program files.

Follow these steps:
* `Tools >> Build System >> New Build System`
* <kbd>ctrl + s</kbd> to save the file in `"../Packages/User/"` location with a name (to be seen in **Build System** list).
* Now, it is visible in `Tools >> Build System` location.

>	NOTE: Remember, for any windows based build, the command has to be installed in Win environment. And the same is applied in case of Ubuntu & OSX machine.

* Cases:
	- **windows**: <br/>
	An object of options to use when the build system is being executed on a Windows machine.
	Example:
	{
			"cmd": ["my_command.exe", "/D", "$file"]
	}
	- **osx**: <br/>
	An object of options to use when the build system is being executed on a Mac machine.
	Example:
	{
			"cmd": ["/Applications/MyProgram.app/Contents/MacOS/my_command", "-d", "$file"]
	}
	- **linux**: <br/>
	An object of options to use when the build system is being executed on a Linux machine.
	Example:
	{
			"cmd": ["bash", "-c", "/usr/local/bin/my_command", "-d", "$file"]
	}

* __Example-1__: 
	- in c++ for implementing `g++ -std=c++14 -o hello.out hello.cpp`
	```
	{
	 "cmd":["bash", "-c", "g++ -std=c++14 -Wall '${file}' -o '${file_path}/${file_base_name}' && '${file_path}/${file_base_name}'"],
	 "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
	 "working_dir": "${file_path}",
	 "selector": "source.c, source.c++",
	 "variants":
	 [
		 {
			 "name": "Run",
			 "cmd":["bash", "-c", "g++ -std=c++14 '${file}' -o '${file_path}/${file_base_name}' && '${file_path}/${file_base_name}'"]
		 }
	 ]
	}
	```
	
* __Example-2__: <br/>
	- For C++: Create a new build system. File - "gcc-cpp.sublime-build"
	```
	{
		"shell_cmd": "g++ -std=c++17 ${file_path}/${file_name} -o ${file_path}/${file_base_name} && ${file_path}/${file_base_name}.exe"
	}
	```
	- For C: Create a new build system. File - "gcc-c.sublime-build"
	```
	{
		"shell_cmd": "gcc -std=c11 ${file_path}/${file_name} -o ${file_path}/${file_base_name} && ${file_path}/${file_base_name}.exe"
	}
	```

* save the file (into the directory shown). Remember to give just the name, no extension (it will automatically take).
* Now, choose the build system.
* References: For more, click [here](https://www.sublimetext.com/docs/3/build_systems.html)

### Open with
Open your files (any type) using your `.exe` file.

NOTE: Firstly install [`SideBarEnhancements`](https://packagecontrol.io/packages/SideBarEnhancements) package.

Follow these steps:
* Open the file in Sublime Text 3.
* "Right click" on file
* Click "Open with" option
* A file - "Side Bar.sublime-menu" opens.
* Now, set the commands for any file - Word, Excel, Image, etc.

Example 1: for Word 2013
```console
//application 3
{
	"caption": "MS Word 2013",
	"id": "side-bar-files-open-with-word",

	"command": "side_bar_files_open_with",
	"args": {
						"paths": [],
						"application": "C:\\Program Files (x86)\\Microsoft Office\\Office15\\winword.exe",
						"extensions":"docx", //any file with extension (starting with doc i.e. doc, docx, docm,..)
						"args":[]
			},
	"open_automatically" : true// will close the view/tab and launch the application
},
```
Example 2: for Excel 2013
```console
//application 4
{
	"caption": "MS Excel 2013",
	"id": "side-bar-files-open-with-excel",

	"command": "side_bar_files_open_with",
	"args": {
						"paths": [],
						"application": "C:\\Program Files (x86)\\Microsoft Office\\Office15\\excel.exe",
						"extensions":"xlsx", //any file with extension (starting with xls i.e. xls, xlsx, xlsm, xlsb,.)
						"args":[]
			},
	"open_automatically" : true// will close the view/tab and launch the application
},
```

> NOTE: It's use is in Git Merge, while opening any binary file. Attach it with this settings in your editor - Sublime Text 3.

## Troubleshooting
* __Disable <kbd>ESC</kbd> aping to COMMAND MODE__
	- Just add this to your "Preferences >> Settings" & then choose right screen i.e. "Settings-User"
	```json
	"ignored_packages": ["Vintage"]
	```
	
## NOTE
* Know spaces and tabs within code: <br/>
	When the code is selected-
	- all the tabs are marked with single dash line
	- all the spaces are marked with dotted lines
