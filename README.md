# mcd - A bash function that prints the recently visited directories.

https://github.com/Jetchisel/mcd

Copyright 2015 Jetchisel

## Installation
* git clone https://github.com/Jetchisel/mcd
* git checkout -b simple remotes/origin/simple
* cd mcd/
* source ./mcd

## Usage: A simple test run once you have sourced mcd.
```shell
for f in /*/; do [[ -x $f ]] && builtin pushd "$f" >/dev/null; done
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
Dirstack must have some value/entry and pushd is the builtin utility that does that.
The builtin dirs command holds the directory stack.
