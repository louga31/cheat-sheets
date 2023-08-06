# direnv: Environment Switcher

direnv is a shell extension that dynamically adjusts your environment variables based on the current directory. By allowing project-specific environment setups, it ensures that tools and dependencies are correctly aligned and isolated per project.

Project Homepage: [direnv: Unclutter Your .profile](https://direnv.net/)
Documentation: [direnv Wiki](https://github.com/direnv/direnv/wiki)

---

## Installation

### Windows

https://direnv.net/docs/installation.html

### Linux

#### Ubuntu/Debian

```sh
sudo apt update && sudo apt install direnv
```

For direnv to work properly it needs to be hooked into the shell. Each shell has its own extension mechanism. Follow the [official direnv hook docs](https://direnv.net/docs/hook.html).

**Example on zsh**:
```zsh
eval "$(direnv hook zsh)"
```

---
## Getting started

Create a new `.envrc` file with your environment variables.

**Example `.envrc` file**:
```zsh
export ENVVAR="test"
export ENVVAR2="test2"
```

Allow the current directory in **direnv**.

```zsh
direnv allow .
```
