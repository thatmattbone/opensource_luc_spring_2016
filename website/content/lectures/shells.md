---
layout: page
title: Shells and the command line
---

# Shells and the command line

Before we start, it's important to note the [difference between a shell and a terminal]( http://unix.stackexchange.com/questions/4126/what-is-the-exact-difference-between-a-terminal-a-shell-a-tty-and-a-con).
* Terminals in detail: http://www.linusakesson.net/programming/tty/


## A Shell is Just a Program

It's easy to confuse a shell with the operating system, but the shell is really just a program like any other. Keep in mind that every process in a unix environment has been `fork()`ed from another process. An init process runs as `pid` 1 and all other processes descrend from it. You can see this using the `pstree` command.

So what does a shell do? It sits there, waiting for user input, and lets us control programs in an interative fashion.

It is even fairly straightforward to [implement your own shell](http://www.gnu.org/software/libc/manual/html_node/Implementing-a-Shell.html#Implementing-a-Shell).

## Job Control

[Job control](http://www.tldp.org/LDP/abs/html/x9644.html) is an important aspect of any shell. In our modern world filled with enumurable virtual terminals, it might feel like job control commands are superfluous, but this is not the case (especially when dealing with remote systems).

Let's use this simple python program...

```
import time

i = 0
while True:
    print("sleeping... {}".format(i))
    time.sleep(5)
    i += 1
```
To show how we can suspend jobs, inspect jobs, run them in the background, bring them back to the foreground, and disown them.


## Builtins vs Programs

One common bit of confusion is the idea of a [shell builtin vs an external command](http://unix.stackexchange.com/questions/11454/what-is-the-difference-between-a-builtin-command-and-one-that-is-not).  One trick to test out whether or not something is a builtin in your shell is to use the `which command`. For example, on my linux system `which ls` prints out `/bin/ls` while `which cd` prints out nothing. This tells us that `cd` is interpretted directly by the shell and does not result in it forking off a new process. It is a builtin.

Consult [this page of the bourne shell manual](http://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html#Bourne-Shell-Builtins) for a complete list of builtins in bash.

## Environment Variables

Much like command line flags environment variables are a way to configure and influence how a program runs. For example if we want to use emacs to edit our crontab:

```
EDITOR=emacs contab -l
```

By default, variables in bash are 'local' to the currently running shell and not passed down to any subprocesses. The `export` built-in changes that behavior:

```
export EDITOR=emacs
crontab -l
```

## Pipelines & Redirection

[pipelines](https://en.wikipedia.org/wiki/Pipeline_%28Unix%29) are an incredibly handy feature implemented in almost all unix shells.

Here we use `cat` to output the contents of a file and pipe that through `grep`.
```
cat /proc/meminfo | grep MemTotal
```

[Redirection](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-3.html#ss3.1) is another capability of almost all shells. It's easy to redirect the output of some command to a file:

```
ls > ls_out
```

Redircting stderr is also easy:
```
ls /thisfiledoesnotexist 2> ls_errs
```

## Overviews of Popular Shells

The [variety of shells](http://www.in-ulm.de/~mascheck/various/shells/) in the world is mindblowing. We'll take a look at a few big ones.

### Bash

[bash](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/) is the shell you are probably most familiar with. These days it is the de facto standard on linux desktops, servers, and mac os machines. 

### c shell

c shell was invented to more closely match c-style syntax in shell programming. Though it seems to fall more out of use day by day, [tcsh](http://www.tcsh.org/Welcome) was the default shell in early versions of mac os X.

### zsh & fish shell

[zsh](http://www.zsh.org/) and [fish shell](https://fishshell.com/) offers some modern conveniences both in terms of interactivity and programming. Both are probably most lauded for their ability to add autocomplete to programs (like git, etc), making life easier on the command line.

### ash

[ash](https://en.wikipedia.org/wiki/Almquist_shell) is a slimmed down version of bash found on many embedded devices and android devices, too.

# Shell Programming

In addition to working interactively, most shells are also their own programming langauge, allowing us to write scripts that to all sorts of things. Languages like bash have the things we might expect from fully featured languages like [conditionals](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-6.html), [loops](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-7.html), and [functions](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO-8.html).

Bash can be tricky to get your head around and so something like fish shell tries to [emulate the appearance of modern languages](http://fishshell.com/docs/current/tutorial.html#tut_conditionals).
