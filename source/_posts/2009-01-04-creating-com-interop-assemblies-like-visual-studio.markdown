---
layout: post
title: "Creating COM interop assemblies like Visual Studio"
date: 2009-01-03 15:33:53Z
comments: true
categories: .NET
alias: /blog/archive/2009/01/04/creating-com-interop-assemblies-like-visual-studio.aspx
---

Unfortunately, we still use COM to access a few of our own and 3rd party native libraries in our product from .NET code.

In my journey to improve our build system I needed to work out how to generate COM interop assemblies exactly like Visual Studio does
when you add a reference to a type library.

Just run the Type Library Importer (`tlbimp`) like following substituting {0} with your library's name. The key is the `/namespace` argument
which defaults to `Interop` if not specified.

`tlbimp.exe {0}.dll /strictref /namespace:{0} /out:Interop.{0}.dll`
