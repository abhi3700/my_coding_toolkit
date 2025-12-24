# Coding

## Description

This is about my preferred coding style which I learnt over the years. And still learning.

## Variable naming style

- `camelCase`: JS, TS, Solidity.
- `snake_case`: Rust, C/C++.
- `SCREAMING_SNAKE_CASE`: used for defining constants in C/C++, Rust, Solidity, Python.

## Repositories

Use github for quick project kickstart.

There are many boilerplates I have in my account for easy project kickstart.

For any type of learning, I create a repo with name like "My_Learning_Blockchain". And for languages, I use "My_Learning-Rust".

## LoC

Q. How many lines of code you have written?
A.

Install `cloc` via `brew install cloc` on macOS.

```sh
cd PROJECT_DIR
cloc . --exclude-dir=target,node_modules,.git
```

<details><summary>Sample output</summary>

```
     448 text files.
     375 unique files.                                          
     155 files ignored.

github.com/AlDanial/cloc v 2.06  T=0.18 s (2120.0 files/s, 505206.5 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
Rust                           242           6460          10839          44478
JSON                            11              0              0           6332
JavaScript                      23            351            245           5667
CSS                             15           1329            313           5558
SVG                              9              5              3           2746
Markdown                        18            488              6           1168
HTML                             7            141             57            835
TOML                            26            106             54            612
Bourne Shell                    11            151            155            543
Text                             2             51              0            244
Lua                              5             25             40            110
TypeScript                       4              8             70             99
Dockerfile                       1             11             19             31
YAML                             1              1              0             13
-------------------------------------------------------------------------------
SUM:                           375           9127          11801          68436
-------------------------------------------------------------------------------
```

</details>
