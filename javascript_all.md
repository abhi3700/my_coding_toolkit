## Online compiler
- https://jsfiddle.net/

### Editor
- Sublime text

### Compiler
- Setup within ST3 
  + Tools >> Build system >> New Build system 
    Copy and Paste the code:
    ```json
    {
      "cmd": ["F:/Softwares/nodejs/node.exe", "$file"],
      "selector": "source.js"
    }
    ```
  And then, save as JSON file. 
  Finally, use this as build system for Javascript.
