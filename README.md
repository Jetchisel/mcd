# mcd - A bash function that prints the currently remembered directories.

https://github.com/Jetchisel/mcd

Copyright 2015-2016 Jetchisel

A bash shell function that allows user to navigate to the previous directories.
Duplicate directories are discarded in the menu (directories visited more than once).
When sourced, it has its own "cd" and its own directory stack. (overriding the bui-
ltins.). It tries to work around those directories with embedded newlines  which  the
builtin "dirs" can't handle in some cases. If the "git" utility is installed,
the status of the git repo is printed once inside the directory.

## Requirements
* Bash version 4 and newer is a must because of Associative arrays.
* Tput and git are optional.

## Installation
* git clone https://github.com/Jetchisel/mcd
* cd mcd/ && source ./mcd
* or just download the zip archive and unpack it.

## Usage: A simple test run once you have sourced mcd.
```shell
for f in /*/; do [[ -x $f ]] && cd "$f"; done
```

Now run mcd to see the lists of recently visited directories. Press the correct number in the menu.
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
Change the **/path/to** with the absolute path where the file mcd is located.
