---
layout: page
title: Weird Operating Systems
---

# Weird Operating Systems

## Unix and Friends

Today we tend to take Linux for granted. From servers to phones to routers, the linux kernel is nearly ubiquitous. But starting from the humble [original linux announcement](https://groups.google.com/forum/#!msg/comp.os.minix/dlNtH7RRrGA/SwRavCzVE7gJ) and even earlier, we can see a family of open source operating system. Their evolution and continued development today can teach us a lot about open source software, too.

The [slightly less humble initial announcement](http://www.gnu.org/gnu/initial-announcement.html) of the GNU project predates the linux announcement by a number of years, but when linux was announced there was no free kernel widely available. [minix was not available under a free license until later](http://minix1.woodhull.com/faq/mxlicense.html) and existing BSDs were living under the chilling effect of [a lawsuit](https://en.wikipedia.org/wiki/UNIX_System_Laboratories,_Inc._v._Berkeley_Software_Design,_Inc.). Eventually linux matured and was released under the GPL version 2, with Torvalds later stating: ["Making Linux GPL'd was definitely the best thing I ever did."](http://www.tlug.jp/docs/linus.html)

### Hurd

Hurd is technically the official kernel of the GNU project though it has some [colorful](https://www.gnu.org/software/hurd/hurd.html) history. It's sort of unclear what would have happened had a usable kernel been produced before Linus came on the scene. Regardless, the hurd project is [still kicking](https://www.gnu.org/software/hurd/community/gsoc/project_ideas.html).


### BSDs

* [FreeBSD](https://www.freebsd.org/)
* [pcBSD](http://www.pcbsd.org/)
* [NetBSD](https://www.netbsd.org/)
* [OpenBSD](http://www.openbsd.org/)

One interesting thing about the BSDs is that their development style remains more conservative. Thinking about the famous ["The Cathedral and the Bazaar](http://www.catb.org/~esr/writings/cathedral-bazaar/), the BSDs are developed in a much more cathedral-like fashion. Checkout [wikipedia](https://en.wikipedia.org/wiki/The_Cathedral_and_the_Bazaar) for more.

### Minix

Minix has been around as an educational tool for sometime now, but [minix 3](http://www.minix3.org/) aims to be more than just pedagogical. The [minix wikipedia page](https://en.wikipedia.org/wiki/MINIX) provides some history.

### Plan 9

[Plan 9](http://plan9.bell-labs.com/plan9/about.html) was written by many of the same people at bell labs that gave us unix. Plan 9 was intended to be a distributed operating system. We can see some of the ideas in Linux today with a more robust procfs.

### Redox

Look down [a list of open source operating](https://en.wikipedia.org/wiki/Comparison_of_open-source_operating_systems) and you'll see one common feature. They're all written in C!

[redox](http://www.redox-os.org/) aims to change that by taking on the brave goal of writing a new operating system in a new programming language.

### Clones of Proprietary Systems

* [wine](https://www.winehq.org/) -- not an operating system but a "compatibility layer" for windows
* [backwards wine](http://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx) just announced today! 3/30/2016
* [BeOS clone](https://en.wikipedia.org/wiki/Haiku_%28operating_system%29)
* [AROS](https://en.wikipedia.org/wiki/AROS_Research_Operating_System)

### Embedded Operating Systems
* [contiki](https://en.wikipedia.org/wiki/Contiki)
* [tinyos](https://github.com/tinyos/tinyos-main)
* [FreeRTOS](https://en.wikipedia.org/wiki/FreeRTOS)
