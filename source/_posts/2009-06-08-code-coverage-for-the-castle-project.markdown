---
layout: post
title: "Code Coverage for the Castle Project"
date: 2009-06-07 14:44:02Z
comments: true
categories: Castle
alias: /blog/archive/2009/06/08/castle-ncover-and-ndepend-nant-targets.aspx/index.html
---

{% img right /files/2009/ncover_logo.png %}

I'd like to start by thanking the guys from [NCover][1] for the free open source licence of NCover Complete for use at the Castle Project.

I have finally got around to changing the build scripts to have NCover running in our build so we can generate code coverage reports.

You can view the summary report in the artifacts of one of the <u>coverage builds</u> (no longer available), or with this direct link
to the <u>symbol module report for the last successful build</u> (no longer available).

As you can see for yourself Castle's sequence point code coverage is currently at 61.2%. As for individual projects here are just a few:

* ActiveRecord: 65.6%
* Core: 31.7%
* DynamicProxy: 86.4%
* MicroKernel: 67.3%
* MonoRail Framework: 49.6%
* Windsor: 79.5%

Interestingly, Castle Core has the lowest code coverage of any project coming in at 31.7%, while it is at the base of all Castle projects,
however it is very stable and solid.

As expected, NVelocity has the highest maximum cyclomatic complexity by far because of several very long and complex methods.

I am yet to set up the build to generate the full HTML coverage report which displays the source code with annotated coverage information.

[1]: http://www.ncover.com/
