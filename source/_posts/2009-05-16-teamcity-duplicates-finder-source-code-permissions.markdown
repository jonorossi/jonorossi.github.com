---
layout: post
title: "TeamCity Duplicates Finder Source Code Permissions"
date: 2009-05-16 08:18:07
comments: true
categories: TeamCity
alias: /blog/archive/2009/05/16/teamcity-duplicates-finder-source-code-permissions.aspx
---

[{% img right /files/2009/TeamCity_ViewVCSFileContentPermission.png 260 %}](/files/2009/TeamCity_ViewVCSFileContentPermission.png)

I set up the .NET Duplicates Finder feature of TeamCity yesterday for Castle, and was later told that a guest (set up as the project viewer role)
could not see the source code in the report. TeamCity was displaying "You do not have enough permissions to view this file content" instead of
the source code.

I remembered today that the roles in TeamCity were made configurable in 4.5 and adding the "View VCS file content" permission to the project
viewer role now allows everyone to see the source code in the report.

This report provides some interesting results and is well worth setting up. One caveat is the requirement of a Visual Studio solution file
which TeamCity uses to search for the source code.
