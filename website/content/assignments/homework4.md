+++
date = "2015-05-01T15:58:57-05:00"
draft = false
title = "Homework 4"
+++

# Homework 4
Homework 4 will touch on many topics we've discussed in class.

You will install a minimal version of minux in virtualbox, get a c compiler up and running, download the lua source code inside of minux, modify the makefiles to get lua to compile and install, and then write a simple lua script.

Below are some resources:

* [Installling clang](http://wiki.minix3.org/doku.php?id=usersguide:installingbinarypackages), etc.
* If you have problems getting the networking up [these](http://wiki.minix3.org/doku.php?id=usersguide:runningonvirtualbox) [resources](https://www.virtualbox.org/manual/ch09.html#nat-adv-dns) might be useful
* [Lua Release 5.1](http://www.lua.org/ftp/lua-5.1.5.tar.gz)

## Submission Guidelines

In minix to submit:

```
curl http://static.thatmattbone.com/submit.sh > submit.sh
chmod +x submit.sh
./submit.sh <location_to_lua> <your_name>
```

Pass the location to lua as the first parameter (i.e. /usr/local/bin/lua) and your name separated by underscores as the second (i.e. matt_bone).

