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

In the open source world, and on linux in particular there's a wide range of approaches to packaging. [apt](https://wiki.debian.org/Apt), used by debian, ubunto and others,  is one of the more popular formats. We can [browse source packages](https://packages.debian.org/sid/source/) and checkout the [intro to debian packaging](https://wiki.debian.org/IntroDebianPackaging) to get a feel for what's involved. Also checkout this [brief tour of what's in a debian directory](https://feeding.cloud.geek.nz/posts/whats-in-a-debian-directory/).

Other systems such as [nix](https://nixos.org/nix/) and [guix](https://www.gnu.org/software/guix/) take their cues from functional programming. These systems try to isolate packages, making upgrades transactional, and trying to prevent packaging "side-effects" (i.e. breaking all of the things when upgrading libc, for example).

[rpm](http://www.rpm.org/) is another very popular package management system.


### Linux Packaging and Open Source Projects

Managing packages is almost as much of a social problem as a technical problem. The [Ubuntu Masters of the Universe](https://wiki.ubuntu.com/MOTU) keep things in order in the ubuntu packaging world.

[ppa](https://launchpad.net/ubuntu/+ppas)'s let users build their own packages and contribute them to the package ecosystem.


### Downstream Patches

Consider a piece of open source software that has only been tested on one architecture (let's say x86) but a distribution might be interested in enabling this package on a difference architecture it supports (let's say arm). Perhaps the project is ANSI C and only requires a few configuration or compilation changes to get working on the new architecture. A package maintainer might be able to create a small patch to the project that enables it to be built and run on this new architecture. Many packaging systems allow for the management and application of these 'downstream patches'. However, package maintainers and linux distributions [go to great lengths](https://fedoraproject.org/wiki/Staying_close_to_upstream_projects) to push any changes back upstream.

## BSD Packaging

The FreeBSD [ports](https://www.freebsd.org/ports/) system offers a glimpse into how packaging is handled in most BSDs. The [porter's handbook](https://www.freebsd.org/doc/en/books/porters-handbook/) also goes over the technical and social aspects of getting code in the ports system. [pkg](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/pkgng-intro.html) is FreeBSD's binary package manager.

Last week we used [pkgin](http://pkgin.net/) to install binary packages on minux. These are based off of [pkgsrc](https://www.pkgsrc.org/) source packages and available on a few platforms.


## Packaging on Mac OS

While package managers of one sort or another are usually the primary way of installing applications on free operating systems, something like mac os offers a wide range. You can download apps from websites or the app store. You can download and compile sourcecode. But since mac os has unix roots, there are package managers, too. [homebrew](http://brew.sh/) seems to be one of the more popular package managers these days. [macports](https://www.macports.org/) is another.


## Packaging for Programming Language Dependencies

We discussed [maven](https://maven.apache.org/) when we talked about build systems. Maven's strength is that it also provides for package management. Software built with maven can specify dependencies and these dependencies will be fetched from various repositories.

In the python world pip and pypi are often used to manage source and runtime dependencies. [This article](http://www.aosabook.org/en/packaging.html) offers a nice overview of some of the challenges.
