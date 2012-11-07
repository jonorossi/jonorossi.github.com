---
layout: post
title: "Compiling for .NET 2.0 with Csc 3.5 under NAnt"
date: 2009-07-06 12:52:35Z
comments: true
categories: Castle
alias: /blog/archive/2009/07/06/compiling-for-.net-2.0-with-csc-3.5-under-nant.aspx/index.html
---

The Castle Project dropped support for .NET 2.0 on the trunk last year, however as project leader of DynamicProxy I decided we would
continue to support DynamicProxy on .NET 2.0 until downstream projects (e.g. NHibernate) no longer support it.

Castle Core has had a reference to System.Core for quite some time, however it is conditionally compiled with support for .NET 2.0,
Silverlight and Mono.

Up until recently we had been making sure we didn't use any C# 3.0 features in DynamicProxy so we could still build for .NET 2.0 with
the .NET 2.0 compiler, however this has always been a little annoying.

I worked out that changing the frameworkdirectory attribute on the net-2.0 framework element in NAnt.exe.config will make NAnt use
Csc 3.5. You just need to change 'v2.0.50727' to 'v3.5'.

With this change we can now use the var keyword, lambda expressions, object initializers and anonymous types.
