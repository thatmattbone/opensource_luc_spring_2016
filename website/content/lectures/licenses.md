---
layout: page
title: Licenses
---

# Licenses

Licenses are a very important part of open source software, and they are nearly as varied as the software itself. Checkout the [Open Source Initiative](https://opensource.org), their summary of licenses, and their FAQs to get a feel for the territory. Also, for another (slightly competing) view checkout ["What is free software?"](http://www.gnu.org/philosophy/free-sw.html) from the Free Software Foundation.

When picking a license, our textbook offers some good advice to choose a license that ["many potential users and contributors will already be familiar with it"](http://producingoss.com/en/license-quickstart.html). Also, please read and understand [chapter 9](http://producingoss.com/en/legal.html).


## Public Domain

Public domain software is software (code or binaries) that claim to be free of copyright. That might sound simple enough, but as the free software foundation notes:

> Under the Berne Convention, which most countries have signed, anything written down is automatically copyrighted. This includes programs. Therefore, if you want a program you have written to be in the public domain, you must take some legal steps to disclaim the copyright on it; otherwise, the program is copyrighted.
(see: [Public Domain Software](http://www.gnu.org/philosophy/categories.en.html#PublicDomainSoftware))

Checkout these other resources around public domain software.

* https://opensource.org/faq#public-domain
* http://unlicense.org/

SQLite is an example of a major piece of software that's been placed in the public domain.

## MIT, BSD-Style, & Permissive Licenses

Let's take a look at the (very short) MIT License:

>    Copyright (c) 2016, Matt Bone
>
>
>    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
>
>    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
>
>    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

And the similar (3 clause) BSD License:

> Copyright (c) 2016, Matt Bone
> All rights reserved.
> 
> Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
> 
> 1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
>
> 2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
>
> 3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
>
> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

The popular [Apache License](https://opensource.org/licenses/Apache-2.0) takes things a step further by including mention of software patents.

### Do No Evil

Douglas Crockford has been causing trouble (good trouble) for years, and it stil stirring it up with his ['do no evil' license for JSMin](https://github.com/douglascrockford/JSMin/blob/master/jsmin.c).

## GPL & Other Copyleft Licenses

The GPL is perhaps one of the most popular licenses in the open source community. Today there are two versions in use, [version 2](http://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html) and [version 3](http://www.gnu.org/licenses/gpl-3.0.en.html). The linux kernel is licensed under version 2 of the GPL. The most interesting contrast with licenses like the BSD license is the idea of "copyleft". That is, derivative works must be licensed under the same license. The license is "viral".

In a certain sense, GPL and copyleft licenses are more restrictive than other licenses. So while creating a derivative GPL'd work is fairly simple,  [incorporating a more permissive license](https://www.softwarefreedom.org/resources/2007/gpl-non-gpl-collaboration.html) can get tricky.

* GPL 2 v 3: http://www.groklaw.net/article.php?story=20060118155841115

### Linking & the GPL

While the [FSF's position is quite clear](http://www.gnu.org/licenses/old-licenses/gpl-2.0-faq.html#LinkingWithGPL), there is [some controversy](https://en.wikipedia.org/wiki/GNU_General_Public_License#Linking_and_derived_works) regarding linking (static or dynamic) and whether or not that constitutes a derivative work. The [LGPL](http://www.gnu.org/licenses/lgpl-3.0.en.html) was written to handle this case specifically.

### Afferro

It is permissible to modify GPL code, run it on a server, and allow others to use that service WITHOUT distributing your modified code. The Affero GPL [addresses these concerns](http://www.gnu.org/licenses/why-affero-gpl.en.html).

mongoDB is licensed under the AGPL v3: https://www.mongodb.org/licensing

### Contributor Agreements

Many projects ask for contributor agreements. In this case, the person contributing their code signs away (reassigns) their copyright to an organization or company. This organization or company is then (theoretically) able to license that code however they wish.

* See: http://en.wikipedia.org/wiki/SCO-Linux_controversies


# Creative Commons

[Creative Commons](https://creativecommons.org/) is worth a mention here. Instead of dealing with code, creative commons offers customizeable licenses for things like your songs, photographs, artwork, documention, course materials, etc, etc.

As with all things, it's important to think about your license carefully, while they were complying with creative commons license, [flickr caused some controversy](http://www.forbes.com/sites/paulmonckton/2014/12/23/flickr-apologises-over-wall-art/#4d6e71ef6294) by offering prints of other peoples work (work that had been published with a creative commons license allowing commercial use) for sale as wall art prints online.




