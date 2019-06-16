[DEPRECATED] -- I now use **bobthefish** as shell prompt theme.
Have a look at `omf` framework for `fish`.

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

