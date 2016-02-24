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

## Pipelines & Redirection

## Overviews of Popular Shells

The [variety of shells](http://www.in-ulm.de/~mascheck/various/shells/) in the world is mindblowing. We'll take a look at a few big ones.

### Bash

[bash](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/) is the shell you are probably most familiar with. These days it is the de facto standard on linux desktops, servers, and mac os machines. 

### c shell

c shell was invented to more closely match c-style syntax in shell programming. Though it seems to fall more out of use day by day, [tcsh](http://www.tcsh.org/Welcome) was the default shell in early versions of mac os X.

### zsh & fish shell

### ash

[ash](https://en.wikipedia.org/wiki/Almquist_shell) is a slimmed down version of bash found on many embedded devices and android devices, too.

# Shell Programming

In additiona to working interactively, most shells are also their own programming langauge, allowing us to write scripts that to all sorts of things.
