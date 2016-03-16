---
layout: page
title: Virtualization
---

# Virtualization

Virtualization is a broad topic that becomes more relevant to open source computing every day. While cloud providers like amazon webservices offer the ability to spin up servers running proprietary operating systems, more often than not users choose to run an open source operating system such as Linux or FreeBSD. With desktop virtualization software like VirtualBox it's simple to run a free OS on your personal workstation, too. By making the deployment of open source operating systems almost trivial, these virtualization techniques bring more users into the open source family everyday.

## Emulators vs Virtualization

First, let's talk a little bit about emulators [which are a slightly different beast than virtualization software.](http://www.computerworld.com/article/2551154/virtualization/emulation-or-virtualization-.html)

* [bochs](http://bochs.sourceforge.net/) is an older project that emulates x86 cpus. It's interesting to [read about the internals](http://bochs.sourceforge.net/How%20the%20Bochs%20works%20under%20the%20hood%202nd%20edition.pdf) and discover how the hardware is emulated with software.
* http://www.hercules-390.eu/
* [qemu](http://wiki.qemu.org/Main_Page) is a particularly interesting project that dances on the border between virtualization and emulation. While it's able to [strictly emulate a wide variety of systems in several modes](http://qemu.weilnetz.de/qemu-doc.html#intro_005ffeatures), qemu is also capable of [using kvm](http://wiki.qemu.org/KVM) to provide virtualization and improve performance.


## ec2, DigitalOcean, etc

## webdev, networking stuff

docker, vagrant, openstack

# Virtual Machines
Java virtual machine and bytecode example. Java runtime bytecode manipulation.

Python virtual machine and bytecode example. py.test examples of runtime bytecode manipulation.
