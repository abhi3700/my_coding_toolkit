## About
This is a editor cum IDE used for any format of file.
link - https://www.sublimetext.com/

## Documentation
link - http://docs.sublimetext.info/en/latest/index.html

## Installation
I prefer using Win 10. So, install on Win 10 & then connect WSL by creating shortcut to the ubuntu repo "/usr/local/bin/subl"

Follow the steps:
* Install from the link - https://www.sublimetext.com/3
* make the shortcut link on ubuntu using `ln -s "/mnt/f/Softwares/Sublime Text 3/subl.exe" /usr/local/bin/subl`
* use `subl` on bash-cmd

## Uninstallation
* All the extra packages are installed in "click Browse Packages".
* So, during uninstall, make a copy of the Sublime Text3 in other drives (E/ F/ G). Location - "C:\Users\abhijit\AppData\Roaming\Sublime Text 3".
* After re-install, copy the folder into the location of the 'Browse Packages'

### Shortcuts
* `ctrl + P` - find anything within the workspace.
  * `eosio.hpp:5` - this takes to line 5 of "eosio.hpp" file.
* `alt + shift + 2` -  split the view into 2
* `ctrl + shift + P` - command palette i.e. manually install packages, Project:Save, Project:close, set:java, set:javascript, so on and so forth.
* 'Double click' will open the file (among the open side bar) and show in the "OPEN FILES". <br/>
  'Single click' will just open the file.

### Preferences
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
* Creating a new build system:
	- Tools >> Build system >> New build system...
	- paste your settings. E.g.- in c++ for implementing `g++ -std=c++14 -o hello.out hello.cpp`
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
	- save the file (into the directory shown). Remember to give just the name, no extension (it will automatically take).
	- Now, choose the build system.

### Packages
Just `ctrl + shift + P` and type the package name and enter. It will install thereafter. 
If not found, then manually download the .zip file into the directory "Preferences >> Browse packages". Then restart the sublime App.

* [x] A File Icon - https://github.com/ihodev/a-file-icon
* [x] Auto Refresh
* [x] AutoFileName
* [x] Color Scheme - Pastels UI
* [x] Comment-Snippets
* [x] [CppFastOlympicCoding](https://packagecontrol.io/packages/CppFastOlympicCoding) - 
	compile in a unique way (in the sidebar on right side using unique test cases). Demo on the package link. Use `ctrl + alt + b` to debug, compile, test.
* [x] EasyWorkspace - [link](https://packagecontrol.io/packages/EasyWorkspace)
  ```
  Save Workspace    | ctrl+alt+s       | Save open files and folders as an easy workspace
  Save As Workspace | ctrl+alt+shift+s | Save easy workspace to specified file
  Open Workspace    | ctrl+alt+o       | Open an existing workspace
  ```
* [x] EasyWorkspace-workspaces
* [x] FuzzyFilePath
* [x] [Git Savvy](https://packagecontrol.io/packages/GitSavvy) - Full git and GitHub integration with ST3.
* [x] [Include Autocomplete](https://packagecontrol.io/packages/Include%20Autocomplete) - for C++ files (in particular) to find out files inside folders. e.g. inside `#include " "`, use `../` to search for files and also other files inside different folders.
	NOTE: It has to be applied in workspace i.e. open a folder and import any files within a sub-folder using the above technique.
* [x] Inline Google translate
* [x] MarkdownLivePreview: In the command palette, type "markdownlivepreview" and go to markdownlivepreview.preferences and toggle "keep on preview" as true.
* [x] [MarkdownTOC](https://github.com/naokazuterada/MarkdownTOC)
* [x] MarkdownWriter
* [x] PlainTasks
* [x] RTagsComplete
* [x] SideBarEnhancements
* [x] Stackoverflow Snippets
* [x] Stackoverflow Debug Helper
* [x] Toggle Read-Only 
* [x] Vue Syntax Highlight
* [x] Vuejs Complete Package
* [x] WebAssembly Text Syntax
* [x] zzz A File Icon zzz
* Markdown Extended
* JSON Comma
* Ethereum
* EthereumSoliditySnippets
* Rainglow theme



### Shortcut keys
After the above packages are installed, use the following personalized shortcut keys:
* `ctrl + o` - open files, folders.
* `ctrl + s` - save the file.
* `ctrl + shift + s` - "save as" the file.
* `ctrl + tab` - switch b/w tabs in a panel.
* `alt + shift + 1` - view layout single. 
* `alt + shift + 2` - view layout double. Like this, so on and so forth.
* `ctrl + 1` - switch to panel 1.
* `ctrl + 2` - switch to panel 2.
* `ctrl + alt + s` - save the workspace with opened folder.
* `ctrl + alt + o` - open the saved workspaces (all will appear in the palette).
* `ctrl + shift + p` - open the command palette.
* `ctrl + p` - open any files from the workspace (chosen folder).
* `ctrl + shift + p` >> "install package" --> install any package available.
* `ctrl + alt + b` - debug, compile, test C++ program. [NOTE: `cppfastcoding` package should be installed first.]

For more, click [here](https://shortcutworld.com/Sublime-Text/win/Sublime-Text_Shortcuts)


