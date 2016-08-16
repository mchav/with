# With
Program prefixing for continuous workflow using a single tool.

### Usage

`with <program>`


Starts an interactive shell with where every command is prefixed using `<program>`.

For example:
```
$ with git
git> add
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

Currently supports command history and limited completions.
