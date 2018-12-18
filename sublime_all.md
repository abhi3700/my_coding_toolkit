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
Just <kbd>ctrl + shift + p</kbd> and type the package name and enter. It will install thereafter. 
If not found, then manually download the .zip file into the directory "Preferences >> Browse packages". Then restart the sublime App.

* [x] A File Icon - https://github.com/ihodev/a-file-icon
* [x] Anaconda
* [x] [AppendSemiColon](https://packagecontrol.io/packages/AppendSemiColon): On windows, <kbd>ctrl + ;</kbd> for inserting semicolon and <kbd>ctrl + shift + ;</kbd> to insert both semicolon and newline.
* [x] Auto Refresh
* [x] AutoFileName
* [x] [C++ Snippets](https://packagecontrol.io/packages/C%2B%2B%20Snippets)
* [x] Color Scheme - Pastels UI
* [x] Comment-Snippets
* [x] Conda
* [x] [CppFastOlympicCoding](https://packagecontrol.io/packages/CppFastOlympicCoding) - 
	compile in a unique way (in the sidebar on right side using unique test cases). Demo on the package link. Use <kbd>ctrl + alt + b</kbd> to debug, compile, test.
* [x] DoxyDoc: C++ description about any method, class, template. [Usages](https://packagecontrol.io/packages/DoxyDoc) in animation form.
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
* [x] Javascript Completions
* [ ] MarkdownLivePreview: In the command palette, type "markdownlivepreview" and go to markdownlivepreview.preferences and toggle "keep on preview" as true.
* [x] [MarkdownPreview](https://packagecontrol.io/packages/MarkdownPreview). After install, for `key binding` i.e shortcut key, `Preferences >> Key Bindings`, add this line `{ "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} },`. Now, press `alt+m` to preview in browser.
* [x] [MarkdownTOC](https://github.com/naokazuterada/MarkdownTOC)
* [x] MarkdownWriter
* [x] PlainTasks
* [x] RTagsComplete
* [x] SideBarEnhancements
* [x] Stackoverflow Snippets
* [x] Stackoverflow Debug Helper
* [x] Terminal: open terminal at the current folder of the opened file. Access by right clicking and choose the option "Open terminal here". By default it opens the Windows cmd. But to open the bash cmd, follow this: Preferences >> Package Settings >> Terminal >> Settings-Default. And then add this `"terminal": "C:/Windows/System32/bash.exe",` i.e. bash executable location.
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
* <kbd>ctrl + shift + t</kbd> - open terminal in that directory location

For more, click [here](https://shortcutworld.com/Sublime-Text/win/Sublime-Text_Shortcuts)

## Custom
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

