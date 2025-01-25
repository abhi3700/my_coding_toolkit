# Vim

## Installation

It comes installed by default in each CLI even if it is as tiny as Alpine linux (only `66 MB`).

## Commands

- `$ vi -n hello.cpp` - Create & open a new file, if doesn't exist
- `$ vi hello.cpp` - open an existing file, & create if doesn't exist unless save command is used.
- `<kbd>esc</kbd>` - Escape writing i.e. going to **normal** mode.
- `Esc` >> `i` - **Insert** mode (write mode)
- `:w` - save a file
- `:wq` - save & close a file.
- `:q!` - close a file without saving.
- `u` - undo
- `b` - move 1 word left
- `w` - move 1 word right
- `:q!` - Quit Vim without saving the data file (all unsaved changes are discarded).
- `:dw`: delete a word from end of a line the start of a line.
- `diw`: In normal mode, delete the word only.
- `daw`: In normal mode, delete the word and spaces around. 
- `:dd`: delete a line (current cursor) only
- `:d3`: delete 3 lines
- `yy`: copy current line
- `p`: paste below/above the current line based on current cursor position.

### Forward movement

- `w`: Move the cursor to the beginning of the next word.
- `e`: Move the cursor to the end of the current or next word.
- `ge`: Move the cursor to the end of the previous word.

### Backward movement

- `b`: Move the cursor to the beginning of the current or previous word.
