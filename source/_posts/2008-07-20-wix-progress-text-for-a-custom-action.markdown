---
layout: post
title: "WiX Progress Text for a Custom Action"
date: 2008-07-20 11:09:56Z
comments: true
categories: Wix
alias: /blog/archive/2008/07/20/wix-progress-text-for-a-custom-action.aspx
---

The MSI installer for Castle Visual Studio Integration runs both VS2005 and VS2008 with the `/setup` switch to configure the new
Visual Studio package. Because this process can take a while, I tried to work out how to display custom status text while the
custom action was running, but had no luck in finding any documentation about how to do this until just recently.

If you have a custom action like:

    <CustomAction Id="CA_DevEnv2008Setup" Property="DEVENV2008_EXE_PATH" ExeCommand="/setup" Impersonate="no" Execute="deferred" />

Then a `ProgressText` element like the following will set the status text while it is running:

    <UI>
      <ProgressText Action="CA_DevEnv2008Setup">Configuring Visual Studio 2008... (this may take a few minutes</ProgressText>
    </UI>

I found the details of how to do this in a [forum post][1] on the WiX sourceforge mailing list.

[1]: http://sourceforge.net/mailarchive/message.php?msg_id=028001c836c1%24fb70a270%24f251e750%24%25langley%40seconag.com
