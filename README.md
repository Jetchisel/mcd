# mcd - A bash function that prints the recently visited directories.

https://github.com/Jetchisel/mcd

Copyright 2015 Jetchisel

## Colored branch from Master.
* A more colored (bling-bling) version.

## Installation
* git clone https://github.com/Jetchisel/mcd
* cd mcd/
* git checkout -b Colored remotes/origin/Colored
* source mcd

## Usage: A simple test run once you have sourced mcd.
```shell
for f in /*/; do [[ -x $f ]] && builtin pushd "$f" >/dev/null; done
```

Now run mcd to see the lists of recently visited directories.
```shell
mcd
```
##
Dirstack must have some value/entry and pushd is the builtin utility that does that.
