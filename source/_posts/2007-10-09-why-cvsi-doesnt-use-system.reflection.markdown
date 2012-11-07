---
layout: post
title: "Why CVSI doesn't use System.Reflection"
date: 2007-10-09 12:18:07Z
comments: true
categories: Castle
alias: /blog/archive/2007/10/09/why-cvsi-doesnt-use-system.reflection.aspx/index.html
---

When you use `System.Reflection.Assembly.Loadxxx` it loads the assembly into the current AppDomain unless you specifically load it
into another AppDomain. The problem with this is that there is no way to unload the assembly unless you unload the whole AppDomain.
Therefore, loading an assembly using `Assembly.Load` locks the assembly on the disk until you unload the AppDomain which prevents
you from being able to rebuild your project.

If you create another AppDomain and unload it every time you needed to reflect over assemblies the performance of the IntelliSense
would make it nearly useless. This is because it takes a second or so to create an AppDomain and another second to unload it. This
is why ASP.NET is slow at refreshing the page after you rebuild your project because it unloads the old AppDomain and creates a new
one with your new assemblies. ASP.NET does not have the problem of locked assemblies because it shadow copies them to a temporary
directory.

I considered using [PERWAPI][1] because I have used it before for another compiler, but I decided to use [Mono Cecil][2] because I
had never used it before and have seen it used for other projects at [Castle][3]. Both PERWAPI and Mono Cecil read the assembly off
the disk just like you would open a normal file. They then build up objects to represent the structure of the assembly. By using a
reader like these you do not have the problems of loading the types into the CLR that you do with `System.Reflection`. The main
limitation of these readers is obvious, you cannot create instances of classes or execute the code in the assembly.

Castle Visual Studio Integration reads the assemblies in your 'Bin' directory using Mono Cecil and finds all the helpers and view
components so that it can display them in the IntelliSense lists in Visual Studio as quickly as possible.

[1]: http://plas.fit.qut.edu.au/perwapi/
[2]: http://www.mono-project.com/Cecil
[3]: http://www.castleproject.org/
