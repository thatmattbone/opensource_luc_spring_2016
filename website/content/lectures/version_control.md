---
layout: page
title: Version Control and Collaboration Tools
---

# Version Control 

## A Short Example

```
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ git init
Initialized empty Git repository in /home/mbone/Developer/vc_test/repo1/.git/
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ emacs -nw foo
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        foo

nothing added to commit but untracked files present (use "git add" to track)
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ git add foo
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ git commit -m "adding the foo file"
[master (root-commit) 2d08ac5] adding the foo file
 1 file changed, 1 insertion(+)
 create mode 100644 foo
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ git status
On branch master
nothing to commit, working directory clean
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ git log
commit 2d08ac51f450de81b66e54456b061d28b6f225ae
Author: Matt Bone <thatmattbone@gmail.com>
Date:   Wed Jan 27 18:25:10 2016 -0600

    adding the foo file
mbone@mbone-UX303LB:~/Developer/vc_test/repo1$ 
```

## Version Control History

ESR offers a [very interesting summary of version control](http://www.catb.org/esr/writings/version-control/version-control.html) (if slightly unfinshed) that was useful in putting this lecture together. It is worth a read.


### Versioned File Systems

While quite different from source control systems, versioned files have been around for some time. There are similarities.
One example is the system found in [vms](https://en.wikipedia.org/wiki/Versioning_file_system#Files-11_.28RSX-11_and_OpenVMS.29) and another is that found in MVS and later os/390 and z/os.


### RCS (gen 1)

[RCS](https://www.gnu.org/software/rcs/) seems to be the grandfather of all our existing version control systems. It is described in this academic paper, [RCS-A System for Version Control](https://www.gnu.org/software/rcs/tichy-paper.pdf). RCS has no concept of networking, though it could have been used in a shared filesystem setting. It also has no concept of a 'project' or changes made to a group of files. Instead, each file is versioned individually.

### CVS and SVN (gen 2)

[CVS](https://en.wikipedia.org/wiki/Concurrent_Versions_System) began its life as a wrapper around RCS files. It allowed for the repo notion we've come to know and love. Eventually it supported a client/server model and allowed users to work offline (but not make commits offline).

[Subversion or SVN]() supplanted CVS quite thoroughly.

### Bitkeeper, the Linux Kernel, and DVCSs (gen 3)x

Moder version control systems such as [git](https://git-scm.com/) and [mercurial](https://www.mercurial-scm.org/) evolved out of an [open source controversy](https://en.wikipedia.org/wiki/BitKeeper#License_concerns). [Monotone](http://www.monotone.ca/) also provided inspiration.

The really interesting thing about these gen3 systems is the ability to make commits offline and shuffle change sets between repos without a string client/server model. Some have theorized that this allows for [better development](http://blog.red-bean.com/sussman/?p=20#comment-103). Other advantages in these more modern systems is the [improvement and wider adoption of merges](http://stackoverflow.com/questions/2471606/how-and-or-why-is-merging-in-git-better-than-in-svn). Though this pain has been alleviated somewhat in newer versions of SVN.

### Other Crazy Stuff

The world of version control is not stagnent. For example [darcs](http://darcs.net) and its [theory of patches](http://darcs.net/Theory) offers some alternative thoughts on version control. 

[Fossil](https://en.wikipedia.org/wiki/Fossil_%28software%29) contains an entire suite of collaboration tools inside the version control system.

# Collaboration Tools

## Sourceforge, Github, et. al.

Sourceforge and then google code, github, bitbucket and others offer us a model of collaboration we're probably all familiar with. These online tools provide things like issue tracking, wikis, visual diff viewers, mailing lists, etc.

## Linux Kernel Mailing List

Development of the linux kernel does things a bit differently...

* FAQ: http://www.tux.org/lkml/
* Right from the source: https://kernel.org/doc/Documentation/HOWTO
* Patchwork tool: http://jk.ozlabs.org/projects/patchwork/


## Security/Workflow Concerns

* https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work
* https://www.mercurial-scm.org/wiki/CommitSigningPlan
