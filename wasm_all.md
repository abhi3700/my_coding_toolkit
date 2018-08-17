## About
Web Assembly is the subset of JS. It is being used in Web Apps for high performance like games using unconventional languages like C/C++ and many more.

## Links
* Documentation - https://kripken.github.io/emscripten-site/index.html

## Installation
I have installed on WSL linux (Ubuntu). [SOURCE](https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html)

Steps to be followed:
* `git clone https://github.com/juj/emsdk.git`
* `cd emsdk`
* `./emsdk update`
* `./emsdk install latest`
* `./emsdk activate latest`
* `sudo ln -s "/mnt/f/softwares/emsdk/emscripten/1.38.11/emcc" /usr/local/bin/emcc`
* `emcc` gives output as:
  
  ```
  ==============================================================================
  Welcome to Emscripten!

  This is the first time any of the Emscripten tools has been run.

  A settings file has been copied to ~/.emscripten, at absolute path: /home/abhijit/.emscripten
  It contains our best guesses for the important paths, which are:

    LLVM_ROOT       = /usr/bin
    NODE_JS         = node
    EMSCRIPTEN_ROOT = /mnt/f/softwares/emsdk/emscripten/1.38.11

  Please edit the file if any of those are incorrect.

  This command will now exit. When you are done editing those paths, re-run it.
  ==============================================================================
  ```

