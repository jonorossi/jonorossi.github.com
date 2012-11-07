---
layout: post
title: "Calling Control.Invoke() with anonymous methods"
date: 2008-03-02 12:20:52Z
comments: true
categories: .NET
alias: /blog/archive/2008/03/02/calling-control.invoke-with-anonymous-methods.aspx/index.html
---

With the help of a [blog post][1] by [Jeremy D. Miller][2] and a comment from Geert Baeyaert, I am now using anonymous methods
with Control.Invoke(). This code sure beats writing delegates for every control you want to make changes to.

The basic code is as follows, which can be improved to check `Control.InvokeRequired` to improve performance:

    Invoke((MethodInvoker)delegate {
        // Code to access WinForms controls here
    });

[1]: http://codebetter.com/blogs/jeremy.miller/archive/2006/11/05/Using-Anonymous-Methods-with-Control.Invoke_28002900_.aspx
[2]: http://codebetter.com/blogs/jeremy.miller/default.aspx
