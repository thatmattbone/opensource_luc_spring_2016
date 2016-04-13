---
layout: page
title: Testing
---

# Testing

Testing is just as important in open source projects as enterprise and commercial software, though its implementation tends to be more varied. Some open source projects [such as sqllite](https://www.sqlite.org/testing.html) have all types of testing: complete coverage, fuzz testing, memory testing, etc, etc. Other projects, particularly small or new projects, might have no testing at all. Even something as important as the linux kernel had no real automated tests for a long time (though [the linux test project](https://github.com/linux-test-project/ltp) now exists. Instead the kernel has historically relied on the community to expose bugs quickly.

## Writing Tests

You've probably encountered unit testing frameworks like [pytest](http://pytest.org) or [junit](http://junit.org/junit4/) in other courses. Many open source projects rely on these technologies, too. As we've already seen with sqllite, some projects implement their testing system from scratch. This is the case with [redis, too](http://oldblog.antirez.com/post/redis-new-test-engine.html).

Some testing projects themselves are open source even though they're almost exclusively used in corporate projects. [selenium](http://www.aosabook.org/en/selenium.html) (and now webdriver) is a great example of this. Like we've discussed beofore, plenty of open source tools are simply examples of professional developers releasing things that help other developers out.

## Coverage

While not a panacea, [code coverage](https://en.wikipedia.org/wiki/Code_coverage) is a common metric that can hint at the quality of project. In python, [coverage.py](https://coverage.readthedocs.org) (which makes use of a python [trace function](https://docs.python.org/3.5/library/trace.html))is the gold standard for code coverage tools.

## Continuous Integration

Conceptually, continuous integration is a simple idea: a script polls version control and, when changes are detected, runs the automated test suite. [travis ci](https://travis-ci.org/) is currently a very popular hosted CI solution. It offers free CI services for open source projects. [jenkins](https://jenkins.io/) and [buildbot](http://buildbot.net/) are two other popular open source CI platforms.

### Performance

Continuous integration is not limited to testing the correctness of software. Some CI projects like [speed.python.org](https://speed.python.org/) track how changes to software 
 
