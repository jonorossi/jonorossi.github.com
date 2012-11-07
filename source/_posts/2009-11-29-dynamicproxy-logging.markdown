---
layout: post
title: "DynamicProxy Logging"
date: 2009-11-29 08:21:23Z
comments: true
categories: Castle
alias: /blog/archive/2009/11/29/dynamicproxy-logging.aspx/index.html
---

[{% img right /files/2009/DPLoggingDemo.png 244 %}](/files/2009/DPLoggingDemo.png)

I have just committed some logging (r6370) into the DynamicProxy codebase which will be in the soon to be released v2.2.

[Krzysztof Kozmic suggested][1] a few weeks back that we should add some logging mainly around type caching and anything else that may
help users diagnose common problems.

In the screenshot, you can see examples of the logging that you can enable. Note that the blue info messages were logged by the demo console
application not by DynamicProxy.

The logging is implemented using the Castle logging infrastructure so Windsor can provide an ILogger directly to a ProxyGenerator. If a
ProxyGenerator class is not instantiated by a container the default logger that DynamicProxy uses is a trace logger set to display messages
at the warning level. By default this means that any messages at warning or higher logged by DynamicProxy will be visible in the Visual
Studio output window.

If you have feedback on the DynamicProxy logging, or ideas for more logging then let us know on the [mailing lists][2].

[1]: http://issues.castleproject.org/issue/DYNPROXY-120
[2]: http://www.castleproject.org/community/mailinglists.html
