+++
date = "2015-05-01T15:58:57-05:00"
draft = false
title = "Packaging"
+++

# Packaging
Package management is a necessity (and oftentimes a hassle) on most desktop operating systems, free or not. Last week when we looked at minix briefly, we used `pkgin` to install a few packages. You might also be familiar with `apt-get` on Ubunut or Debian machines or even `brew` on mac os.

A simple `apt-get` session might look like:

```
sudo apt-get update  # as a superuser, update a the package index
sudo apt-get install redis-server
# you are generally told how much disk space will be used during
# installation and prompted for confirmation
#
# any dependencies are installed, too
```

## Linux Packaging

* https://www.gnu.org/software/guix/
* https://nixos.org/nix/
* https://wiki.debian.org/Apt
* http://www.rpm.org/

### Linux Packaging and Open Source Projects

* (ppa)[https://launchpad.net/ubuntu/+ppas]
* (Ubuntu Masters of the Universe)[https://wiki.ubuntu.com/MOTU]

### Downstream Patches

Consider a piece of open source software that has only been tested on one architecture (let's say x86) but a distribution might be interested in enabling this package on a difference architecture it supports (let's say arm). Perhaps the project is ANSI C and only requires a few configuration or compilation changes to get working on the new architecture. A package maintainer might be able to create a small patch to the project that enables it to be built and run on this new architecture. Many packaging systems allow for the management and application of these 'downstream patches'. However, package maintainers and linux distributions (go to great lengths)[https://fedoraproject.org/wiki/Staying_close_to_upstream_projects] to push any changes back upstream.

## BSD Packaging

* https://www.freebsd.org/ports/
* https://www.pkgsrc.org/
* http://pkgin.net/


## Packaging on Mac OS

* http://brew.sh/
* https://www.macports.org/


## Packaging for Programming Language Dependencies

* Maven
* pip and pypi
