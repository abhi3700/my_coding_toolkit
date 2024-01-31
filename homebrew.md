# Homebrew

Package manager for macOS.

## Usage

### Install

```bash
brew install <package>
```

Directories created:

```
Download: ~/Library/Caches/Homebrew/downloads
Package Installation (for different versions of same pkg): `/opt/homebrew/Cellar`
Binary: /opt/homebrew/bin/
```

When you install a package, it is first downloaded followed by building the package i.e. installation & then symlinks the packages's binaries to `/opt/homebrew/bin/`.

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

When tapped, the repository is cloned to `/opt/homebrew/Library/Taps/<user>/homebrew-<repo>`.

Example:

```bash
❯ brew tap subspace/homebrew-pulsar

==> Tapping subspace/pulsar
Cloning into '/opt/homebrew/Library/Taps/subspace/homebrew-pulsar'...
remote: Enumerating objects: 24, done.
remote: Counting objects: 100% (24/24), done.
remote: Compressing objects: 100% (20/20), done.
remote: Total 24 (delta 6), reused 17 (delta 3), pack-reused 0
Receiving objects: 100% (24/24), 4.64 KiB | 4.64 MiB/s, done.
Resolving deltas: 100% (6/6), done.
Tapped 1 formula (14 files, 11.5KB).
```

And then install:

```bash
❯ brew install pulsar 
Warning: Treating pulsar as a formula. For the cask, use homebrew/cask/pulsar
==> Fetching subspace/pulsar/pulsar
==> Downloading https://github.com/subspace/pulsar/releases/download/v0.7.4-alph
Already downloaded: /Users/abhi3700/Library/Caches/Homebrew/downloads/d72a4cd25aeb90a5dbb02cad6484e54569073c4beddf33d2f7816fc85ae32812--pulsar-macos-aarch64-v0.7.4-alpha.zip
==> Installing pulsar from subspace/pulsar
🍺  /opt/homebrew/Cellar/pulsar/0.7.4-alpha: 3 files, 56.9MB, built in 3 seconds
==> Running `brew cleanup pulsar`...
```

There is a repository that contains the formulae i.e. `*.rb` file.
There is a file `<formula-name>.rb` in the repo which is pulled when you install.

### Untap

To untap (remove) a tapped repository.

```bash
brew untap <user>/<repo>
```

### Cask (GUI)

Install a GUI app with `--cask` flag.

> Only GUI, not CLI.

```bash
brew install --cask <package>
```
