---
layout: post
title: "Hardware Network Firewall"
date: 2008-04-26 16:32:22
comments: true
categories: Networking
alias: /blog/archive/2008/04/26/hardware-network-firewall.aspx
---

{% img right /files/2008/VIAITX.jpg %}

I have been planning to build a standalone hardware firewall for my home network for quite a long time. I brought a 1Ghz VIA ITX
17cm x 17cm motherboard towards the end of last year for the firewall but couldn't find a decent case to mount the board in.

I have been looking on eBay for months for a cheap old rackmount network switch or router that I can gut and mount the board inside,
but nothing has come up cheap. Yesterday I won an eBay auction for a brand new 1U rackmount case, a little flashy for a firewall,
but I got the case cheap and it has plenty of space for all the components compared to an old network switch.

I was always planning to install [IPCop][1], but after some research I found both [m0n0wall][2] and one of its children [pfSense][3]
seem more polished. I know from playing around with IPCop that it wasn't the easiest firewall to configure and with m0n0wall/pfSense
having a single configuration XML file that I can commit into Subversion it is shaping up nicely. pfSense is a fork of m0n0wall and
has more features but requires a slightly more powerful chip and more RAM. pfSense has several features I am interested in that m0n0wall
doesn't, including a traffic shaper and installable packages, which includes both [snort][4] and [squid][5]. I am now planning to install
pfSense because it seems a lot more polished than IPCop, but I haven't tried out pfSense myself.

Once I get all the hardware together I'll post further details of my experience. If you have done something similar yourself or just want
to voice your opinion then I am interested in hearing your comments.

[1]: http://www.ipcop.org/
[2]: http://m0n0.ch/wall/
[3]: http://www.pfsense.org/
[4]: http://www.snort.org/
[5]: http://www.squid-cache.org/
