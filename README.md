# Abdel Config

This repository contains my personal local development environment configuration.

## Directory Structure

### `zsh/`

My shell of choice is **Zsh**, a highly customizable Bash-compatible shell that retains familiar Bash syntax while providing many additional features.

#### `zsh/functions/`

This directory contains custom Zsh functions that are automatically loaded when the shell starts.

For example, to create an `mkdcd` command that creates a directory and immediately changes into it, create a file named `mkdcd.zsh`:

```zsh
function mkdcd() {
  mkdir -p "$1" && cd "$1"
}
```

Once the file is added, the `mkdcd` command will be available in every new shell session.

#### `zsh/env.zsh`

Contains sensitive environment variables that should **not** be committed to Git.

To help others set up their environment, add placeholder values to `env.zsh.example` and keep your actual secrets in `env.zsh`.

#### `zsh/main.zsh`

The main entry point for the Zsh configuration. This file loads the rest of the configuration, including aliases, functions, plugins, and environment variables.