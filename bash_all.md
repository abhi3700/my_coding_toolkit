# Bash

## Usage

- `find . -type f -name '*.rs' -exec rename 's/\.rs$/.txt/' {} +`: Find all .rs files in the current directory and subdirectories and rename them to .txt files

> `brew install rename` has to be installed on macOS.
