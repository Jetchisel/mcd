# mcd - A bash function that prints the recently visited directories.

https://github.com/Jetchisel/mcd

Copyright 2015 Jetchisel

A bash shell function that  lists  a  menu  of  the  previously visited directories.
Duplicate directories are discarded in the menu (directories visited more than once).
When sourced, it has it's own "cd" and it's own directory stack. (overriding the bui-
ltins.). It tries to work around those directories with embedded newlines  which  the
builtin "dirs" can't handle. If the "git" utility is installed, the status of the git
repo is printed once inside the directory.

## Installation
* git clone https://github.com/Jetchisel/mcd
* cd mcd/
* source ./mcd

## Usage: A simple test run once you have sourced mcd.
```shell
for f in /*/; do [[ -x $f ]] && cd "$f"; done
```

Now run mcd to see the lists of recently visited directories.
```shell
mcd
```
Add the --help option for more info.
```shell
mcd --help
```
## Make permanent changes
mcd needs to be sourced during interactive session. Put something like this in ~/.bashrc
```shell
[[ -s /path/to/mcd ]] && source /path/to/mcd
```
Change the **/path/to** with the absolute path where mcd is located.
