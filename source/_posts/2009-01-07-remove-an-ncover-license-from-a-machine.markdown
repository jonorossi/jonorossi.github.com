---
layout: post
title: "Remove an NCover license from a machine"
date: 2009-01-07 11:46:18Z
comments: true
categories: NCover
alias: /blog/archive/2009/01/07/remove-an-ncover-license-from-a-machine.aspx/index.html
---

I needed to remove the license key for NCover on one of our build machines because the license was moved to another build machine.

I didn't find anything using Google, so by trial and no error deleting the value named `Key` from the key `HKLM\SOFTWARE\Gnoso\NCover`
did the trick with NCover v2.1.

I'm writing this down so I know how to do it if I need to do it again, and for anyone else's reference.
