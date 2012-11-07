---
layout: post
title: "Upgrading Castle Visual Studio Integration to VS2008"
date: 2008-06-29 08:41:32Z
comments: true
categories: Castle
alias: /blog/archive/2008/06/29/upgrading-castle-visual-studio-integration-to-vs2008.aspx/index.html
---

{% img right /files/2008/cvsi.png %}

Recently, I spent some time getting Castle Visual Studio Integration working on Visual Studio 2008.

James Curran got it working a while back (as mentioned in CONTRIB-57 of the Castle Project's issue tracker), however this was using the VS2005
compatibility mode. I decided that it would be a better idea to move to the 2008 binaries and conditional compile CVSI, so that I could continue
to support both Visual Studio releases without problems. JetBrains does this with ReSharper so I thought it must be a better solution.

After getting it mostly working I decided to consult Google, where these 2 blog posts by James Lau helped get everything work right:

* [Upgrading VS 2005 Packages to VS 2008: A Basic Guide][1]
* [Upgrading VS 2005 Packages to VS 2008: A more Advanced Guide][2]

If you are working on Visual Studio packages, James' blog contains heaps of useful information. Thanks James.

[1]: http://blogs.msdn.com/jameslau/archive/2008/01/21/upgrading-vs-2005-packages-to-vs-2008-a-practical-guide.aspx
[2]: http://blogs.msdn.com/jameslau/archive/2008/02/13/upgrading-vs-2005-packages-to-vs-2008-a-more-advanced-guide.aspx
