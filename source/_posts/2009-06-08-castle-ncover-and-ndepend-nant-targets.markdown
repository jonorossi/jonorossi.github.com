---
layout: post
title: "Castle NCover and NDepend NAnt targets"
date: 2009-06-08 11:01:44Z
comments: true
categories: Castle
alias: /blog/archive/2009/06/08/castle-ncover-and-ndepend-nant-targets.aspx
---

I forgot to mention the new targets in the previous posts. If you want to generate either the NCover or NDepend reports like the
ones available from TeamCity use these targets.

If you run `nant coverage` it will enable running `nunit-console` under NCover to produce the coverage XML log files, and run a build.
The target will also generate the summary coverage report.

Using `nant ndepend` will run a build and generate the report from the artifacts.
