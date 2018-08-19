## About
Web Assembly is the subset of JS. It is being used in Web Apps for high performance like games using unconventional languages like C/C++ and many more.

## Links
* Documentation - https://kripken.github.io/emscripten-site/index.html
* Codelab Google - https://codelabs.developers.google.com/codelabs/web-assembly-intro/#0

## Installation
I have installed on WSL linux (Ubuntu). [SOURCE](https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html)

Steps to be followed:
* `git clone https://github.com/juj/emsdk.git --recursive`
* `cd emsdk`
* `./emsdk install sdk-incoming-64bit binaryen-master-64bit`
* `./emsdk activate sdk-incoming-64bit binaryen-master-64bit`
* `source ./emsdk_env.sh` - Added to the PATH. <br/>
  #### NOTE: But whenever bash-cmd is loaded for wasm, follow these 2 steps:
   * `cd /mnt/f/Softwares/emsdk`
   * `source ./emsdk_env.sh`
* **Execution:**
  * `emcc hello.cpp` : creates 2 files - `a.out.js` , `a.out.wasm`
  * `node a.out.js` gives output as `"Welcome to the world of WASM!"`
  * `emcc hello.cpp -o hello.html` - creates the .html file.
  * In order to see the output on the browser, follow the steps below: 
    * `python -m SimpleHTTPServer 8080` gives output as -
    ```
    Serving HTTP on 0.0.0.0 port 8080 ...
    
    
    ```
    * Open the url - `http://localhost:8080/hello.html` on the browser. So, it shows the output.
    
      > Unfortunately several browsers (including Chrome, Safari, and Internet Explorer) do not support file:// XHR requests, and can’t load extra files needed by the HTML (like a .wasm file, or packaged file data as mentioned lower down). For these browsers you’ll need to serve the files using a webserver. The easiest way to do this is to use the python SimpleHTTPServer (in the current directory do python -m SimpleHTTPServer 8080 and then open http://localhost:8080/hello.html).
   
   [SOURCE](https://kripken.github.io/emscripten-site/docs/getting_started/Tutorial.html#generating-html)
    

DONE!!...
    
