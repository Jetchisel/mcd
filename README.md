# mcd - A bash function that prints the recently visited directories.

https://github.com/Jetchisel/mcd

Copyright 2015 Jetchisel

## Colored branch from Master.
* A more colored (bling-bling) version.

## Installation
* git clone https://github.com/Jetchisel/mcd
* cd mcd/
* git checkout -b fixnewline remotes/origin/fixnewline
* source ./mcd

## Usage: A simple test run once you have sourced mcd.
```shell
for f in /*/; do [[ -x $f ]] && cd "$f" >/dev/null; done
```

Now run mcd to see the lists of recently visited directories.
```shell
mcd
```
## Make permanent changes
mcd needs to be sourced during interactive session. Put something like this in ~/.bashrc
```shell
[[ -s /path/to/mcd ]] && source /path/to/mcd
```
Change the **/path/to** with the absolute path where mcd is located.

##
## Notes
This branch includes a cd function and an array of Directory stack which tries hard to work
around those nasty directories with embedded newlines.

