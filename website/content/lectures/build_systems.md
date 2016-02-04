---
layout: page
title: Build Systems
---

# Build Systems

Even with open source software, most of the time we download binary packages when we need them. But these binaries were built somehow! Perhaps [more](https://www.netbsd.org/) than proprietary software, open source tools must run on a wide range of operating sytems and hardware. It's a tricky task.

Build systems, from simple to complex, can automate some of these tasks. Today we'll limit ourselves to looking at systems we run interactively, but in the future we'll look at how some of these tools are utilized by automatic systems.

[Here is a nice, terse comparison of a variety of build systems.](http://hyperpolyglot.org/build)

## A Simple Compilation

```
$ wget https://www.sqlite.org/2016/sqlite-autoconf-3100200.tar.gz
$ tar -xzf sqlite-autoconf-3100200.tar.gz
$ cd sqlite-autoconf-3100200
```

## Make 

[make](https://www.gnu.org/software/make/) and it's [family of tools](https://en.wikipedia.org/wiki/GNU_build_system) remains quite prevalent in the open source world. We'll take a look at a simple example of make and see how things can get more complicate with autotools.

The GNU project even provides some [guidelines for releasing projects](http://www.gnu.org/prep/standards/html_node/Releases.html#Releases).

## Friends of Make

* [cmake](https://cmake.org/) is 
* [rake](http://docs.seattlerb.org/rake/) offers a ruby-based solution that feels very similar to make
* [scons](http://scons.org/) which offers a python-based approach. It's [own comparison](https://bitbucket.org/scons/scons/wiki/SconsVsOtherBuildTools) to other tools is interesting.

## Java Tools: Ant, Maven

* [ant](https://ant.apache.org/) was (is?) a popular build system in the java community. [Here](https://ant.apache.org/manual/using.html) is a simple example
* [maven](https://maven.apache.org/) is a build system and more for java that seems to have largely supplanted ant (which it actually extends).

## Javascript Tools: Gulp, Grunt

The newer javascript build tools are worth mentioning because they pull tasks themselves from a repo.

 * [grunt example](http://gruntjs.com/sample-gruntfile)
 * [gulp example](https://github.com/gulpjs/gulp/blob/master/docs/recipes/browserify-transforms.md)


## Remote Stuff: Fabric, Capistrano

Tools like [fabric](http://www.fabfile.org/) and [capistrano](http://capistranorb.com/) blend the line between remote system management and build tools. 


Fabric:
```
from fabric.api import run, cd, hosts, local, get

prod_hosts = (
    'prod1.example.com',
    'prod2.example.com',
)

@hosts(prod_hosts)
def deploy_prod():
    with cd('/home/myuser/'):
        run("git pull origin master")
        run("../env/bin/pip install -r requirements.txt")
        run("""find . -name "*.pyc" -exec rm -rf {} \;""")
        run("kill -HUP `cat /home/myuser/gunicorn.pid`")
```

From the capistrano docs:
```
role :demo, %w{example.com example.org example.net}
task :uptime do
  on roles(:demo), in: :parallel do |host|
    uptime = capture(:uptime)
    puts "#{host.hostname} reports: #{uptime}"
  end
end
```
