# with

[![Join the chat at https://gitter.im/with-tool/Lobby](https://badges.gitter.im/with-tool/Lobby.svg)](https://gitter.im/with-tool/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
Program prefixing for continuous workflow using a single tool.
[PowerShell Implementation](https://github.com/Acader/withPS)

[Discuss a feature or stop by for some tea on gitter](https://gitter.im/with-tool/with)

### Installation

With [apt-get](https://wiki.debian.org/apt-get):

```sh
sudo add-apt-repository ppa:mchav/with && sudo apt-get update && sudo apt-get install with
```

With [bpkg](https://github.com/bpkg/bpkg):

```sh
bpkg install mchav/with -g
```

With [rawgit](https://rawgit.com):

```sh
curl -sLo- https://cdn.rawgit.com/mchav/with/master/install | bash
```

or:

```
curl -s https://raw.githubusercontent.com/mchav/with/master/install | bash
```

### Usage

`with <program>`


Starts an interactive shell with where every command is prefixed using `<program>`.

For example:
```
$ with git
git> add .
git> commit -a -m "Commited"
git> push
```


Can also be used for compound commands.
```
$ with java Primes
java Primes> 1
2
java Primes> 4
7
```

And to repeat commands:
```
$ with gcc -o output input.c
gcc -o -output input.c>
<enter>
Compiling...
gcc -o -output input.c>
```


To execute a shell command proper prefix line with `:`.


`git> :ls`

You can also drop and add different commands.

```
git> +add
git add> <some file>
git add> -
git>
```

To exit use either `:q` or `:exit`.

Currently supports command history and limited completions.
