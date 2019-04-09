# Chain 

An init-like tool displaying system info for your shell prompt.

## Project goals

 - Wide compatibility (at least `bash`, `zsh` and `fish`)
 - Wide modularity with pluggable information modules (PIMs)
 - Atomic (and if possible, minimal) dependencies

## Basic principles

 1. When called, `prompt` will look for the standard `.config` directory.
	Inside the corresponding subdirectory, there should be a folder
	called `modules` containing echoing scripts.

 2. Each script is going to be executed as the prompt owner.

 3. In order to get it on your prompt, you just have to call `prompt`
	in the right rcfile (that is, `.bashrc` `.zshrc` and so on).

Easy, right ? You can even use the `color` script to prettify your infoline.

## Usage example

### Within Bash

```bash
export PS1="$(/path/to/prompt)" 		# For the current session
echo "PS1=$(/path/to/prompt)" >> $HOME/.bashrc	# For every session
```

### Within Zsh

```
# I don't know ZSH yet lulz
```

### Within Fish

```
# In-session or in .config/fish/config.fish
function fish_prompt ()
	sh /path/to/prompt
	echo ":suffix -> "
end
```

