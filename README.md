# with

Program prefixing for continuous workflow using a single tool.

## Why no updates?
This works just fine as is. No need to keep updating things for no reason. Although the completions could be better. 

### Usage

`with <program>`


Starts an interactive shell with where every command is prefixed using `<program>`.

For example:
```sh
$ with git
git> add .
git> commit -a -m "Commited"
git> push
```


Can also be used for compound commands.
```sh
$ with java Primes
java Primes> 1
2
java Primes> 4
7
```

And to repeat commands:
```sh
$ with gcc -o output input.c
gcc -o -output input.c>
<enter>
Compiling...
gcc -o -output input.c>
```


To execute a shell command proper prefix line with `:`.


`git> :ls`

You can also drop, add, and replace different commands.

```sh
git> +add
git add> <some file>
git add> !commit
git commit> <arguments and message>
git commit> -
git>
```

To exit use either `:q` or `:exit`.

### Installation

With [apt-get](https://wiki.debian.org/apt-get):

```sh
sudo add-apt-repository ppa:mchav/with && sudo apt-get update && sudo apt-get install with
```

With [bpkg](https://github.com/bpkg/bpkg):

```sh
bpkg install mchav/with -g
```

With FreeBSD [pkg](https://github.com/freebsd/pkg):

```sh
pkg install with
```

With FreeBSD [ports](https://www.freshports.org/misc/with/)

```sh
cd /usr/ports/misc/with && make install clean
```

With [rawgit](https://rawgit.com):

```sh
curl -sLo- https://cdn.rawgit.com/mchav/with/master/install | bash
```

or:

```
curl -s https://raw.githubusercontent.com/mchav/with/master/install | bash
```

Currently supports command history and limited completions.
