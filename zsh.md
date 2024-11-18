# Zsh

Used this instead of bash on macOS.

## Completions

Use `compinit` to load completions.

Procedure:

1. Suppose, you want to add completions for `mdbook`.
2. Create a file `_mdbook` in `~/.zshrc/completions/_mdbook` using `mdbook completions zsh > ~/.zshrc/completions/_mdbook`.
3. Add these lines to `~/.zshrc`:

    ```zsh
    fpath=(~/.zsh/completions $fpath)
    autoload -Uz compinit
    compinit
    ```

4. Load via `source ~/.zshrc`.
5. Restart your shell.

Done! 🎉.

Now, you can use `mdbook <TAB>` to get completions.
