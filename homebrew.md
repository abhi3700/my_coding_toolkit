# Homebrew

Package manager for macOS.

## Usage

### Install

```bash
brew install <package>
```

The download happens in `/opt/homebrew/Cellar` & the symlink/binary is created in `/opt/homebrew/bin/`.

### Uninstall

```bash
brew uninstall <package>
```

### Tap

Here, tap & then install

```bash
brew tap <user>/<repo>
brew install <package>
```

There is a repository that contains the formulae i.e. `*.rb` file.
There is a file `<formula-name>.rb` in the repo which is pulled when you install.

### Untap

To untap (remove) a tapped repository.

```bash
brew untap <user>/<repo>
```
