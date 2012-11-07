---
layout: post
title: "Migration to Octopress"
date: 2012-11-07 12:04:49Z
comments: true
categories: 
---

{% img right /files/2012/octopress_logo.png %}

I've been very quiet on this blog for quite some time now. I partly blame my limited use of my blog on the dread of having to use
the poor WYSIWYG editor that shiped as part of the version of the [Subtext][1] blog engine my blog was running.

I've finally taken the plunge like many others to move to a blogging platform where the server side is powered by just static files
generated from clean Markdown files reducing vender lock-in if I decide to move to another blogging platform in 5 years time.
I've chosen [Octopress][2] (which builds on [Jekyll][3]) as it provides all the goodies that a usual blog needs.

I'm not going to explain how easy it is to set up, as I'll let others do that, but I'll provide some resources that I found useful:

* [Official Documentation][4]
* [Octopress on Windows and GitHub][5]
* [Jekyll Alias Generator for Posts][6]

Octopress has built in support for [Disqus Comments][7], but since the value of the comments on my blog since I started have been so low
and the spam ratio so high, I've decided to not have any comments on my new blog, and have enabled the twitter integration if anyone
would like to discuss any of my posts.

Octopress's script to generate a new post (`rake new_post`) does not seem to handle time zones very well by default, everything will
work fine as long as you stay in the same time zone. This caused me problems when I was manually migrating the content from the Subtext
database. I made a [change][8] to the new post script to always store the UTC time in the post's "front matter" which you might fine useful.

That's all from me for now, but I hope to make more use of my blog, because reflecting over my blog posts of the last 5 years has shown
me that I've definitely come a long way and that I now more than ever have something to contribute back.

[1]: http://subtextproject.com/
[2]: http://octopress.org/
[3]: https://github.com/mojombo/jekyll
[4]: http://octopress.org/docs/setup/
[5]: http://blog.zerosharp.com/setting-up-octopress-on-windows/
[6]: https://github.com/tsmango/jekyll_alias_generator
[7]: http://disqus.com/
[8]: https://github.com/jonorossi/jonorossi.github.com/commit/3573bc962fe38004c9d511d79892889431c8b073
