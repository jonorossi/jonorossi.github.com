---
layout: post
title: "Sync TeamCity build configurations with Git branches"
date: 2011-11-27 15:18:00Z
comments: true
categories: TeamCity
alias: /blog/archive/2011/11/28/sync-teamcity-build-configurations-with-git-branches.aspx
---

A few months ago at work we moved from Subversion to Git, which has caused us to make many process changes within our development team.
By forcing everyone to work in a new Git branch for every task has added overhead to the build management process. Several of us have
slowly been getting tired of manually creating new TeamCity build configurations just to run a single build that we later have to manually
remove after our release managers have merged our changes.

To remove some of this burden we needed TeamCity to automatically create configurations for all our private development branches, so in
lieu of the excellent JetBrains team building this feature ([TW-16052][1]), I very quickly wrote an app that does just that for us.

I was asked by a few in the TeamCity issue above to provide the code we are using, so I have uploaded a slightly modified version of the
code to GitHub. The app is written in C# and uses the [libgit2sharp][2] library, but could easily be ported to another language or the
command line tools respectively.

So that a few things make sense when you read it, our private development branch convention is "private/username/anything", so with a single
TeamCity project for these branches it will name them "username-anything". You'll see that when it creates the build configuration it creates
it from our branch template and sets the BRANCH_NAME configuration variable, which we use as the Ref name in a VCS root (i.e. %BRANCH_NAME%).

[https://gist.github.com/1397643][3]

[1]: http://youtrack.jetbrains.net/issue/TW-16052
[2]: https://github.com/libgit2/libgit2sharp
[3]: https://gist.github.com/1397643
