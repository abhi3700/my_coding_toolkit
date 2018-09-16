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

* File icon - https://github.com/ihodev/a-file-icon
* Markdown Extended
* JSON Comma
* Ethereum
* EthereumSoliditySnippets
* SideBarEnhancements 
* MarkdownWriter 
* MarkdownLivePreview: In the command palette, type "markdownlivepreview" and go to markdownlivepreview.preferences and toggle "keep on preview" as true.
* Vue Syntax Highlight
* Color Scheme - Pastels UI 
* Stackoverflow Debug Helper
* Stackoverflow Snippets
* EasyWorkspace - [link](https://packagecontrol.io/packages/EasyWorkspace)
  ```
  Save Workspace    | ctrl+alt+s       | Save open files and folders as an easy workspace
  Save As Workspace | ctrl+alt+shift+s | Save easy workspace to specified file
  Open Workspace    | ctrl+alt+o       | Open an existing workspace
  ```
* Rainglow theme
* Auto refresh
* WebAssembly Text Syntax
* Vue Syntax Highlight
* Vuejs Complete Package
* FuzzyFilePath
* [Include Autocomplete](https://packagecontrol.io/packages/Include%20Autocomplete) - for C++ files (in particular) to find out files inside folders. e.g. Use `../` to search for files and also other files inside different folders.
* #### [CppFastOlympicCoding](https://packagecontrol.io/packages/CppFastOlympicCoding) - 
	compile in a unique way (in the sidebar on right side using unique test cases). Demo on the package link. Use `ctrl + alt + b` to debug, compile, test.

