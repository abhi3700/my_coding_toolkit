# Bash

## Usage

- `find . -type f -name '*.rs' -exec rename 's/\.rs$/.txt/' {} +`: Find all .rs files in the current directory and subdirectories and rename them to .txt files

> `brew install rename` has to be installed on macOS.

- `find . -name ".DS_Store" -exec rm -f {} +`: remove all `.DS_Store` files from the current directory and all nested directories
- `find . -type d -name "target" -exec rm -rf {} +`: remove all `target` directories from the current directory and all nested directories
