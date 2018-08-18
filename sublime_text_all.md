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

### Shortcuts
* `ctrl + P` - find anything within the workspace.
  * `eosio.hpp:5` - this takes to line 5 of "eosio.hpp" file.
* `alt + shift + 2` -  split the view into 2
* `ctrl + shift + P` - command palette i.e. manually install packages, Project:Save, Project:close, set:java, set:javascript, so on and so forth.

### Packages
Just `ctrl + shift + P` and type the package name and enter. It will install thereafter. 
If not found, then manually download the .zip file into the directory "Preferences >> Browse packages". Then restart the sublime App.

* File icon - https://github.com/ihodev/a-file-icon
* Markdown Extended
* JSON Comma
* Ethereum
* EthereumSoliditySnippets
