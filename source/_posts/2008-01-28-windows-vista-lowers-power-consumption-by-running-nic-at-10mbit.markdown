---
layout: post
title: "Windows Vista lowers power consumption by running NIC at 10Mbit"
date: 2008-01-28 13:27:37Z
comments: true
categories: Windows
alias: /blog/archive/2008/01/28/windows-vista-lowers-power-consumption-by-running-nic-at-10mbit.aspx/index.html
---

I recently ran out of ports in my network switch, so I moved my computer over to my router as shown below (which is now also full).
I noticed about a week ago that the light for my computer (port 4 of 4) was orange when my computer was off, according to my router's
manual an orange LAN light means it is running at 10Mbit instead of 100Mbit. My first thought was that my UPS had bugged my motherboard
because my UPS is faulty, but I didn't think that was right because I have [a pretty nice PSU][1] that is meant to prevent any power problems.

{% img center /files/2008/Router10MbitConnection.jpg %}

When I switched the network cable from one NIC in my motherboard to the other, the light went green, which made me nervous. Just to check
I plugged my computer into the wall socket for my laptop and it did the same thing which made me more nervous. After flicking the switch
on my power supply and waiting for my PSU to drain its capacitor, I turned it back on and the light on my router went green. That's when
I realised that Vista must be being too smart for itself and is running the NIC at 10Mbit when it turns off the computer to save power.

I am aware that Vista's support for [ACPI][2] (Advanced Configuration and Power Interface) is really good. It puts my computer to sleep
so the computer makes no noise and I can start using it again in only a second. I searched around for other people who have discovered
this and couldn't find any info that Vista does actually do this, so I can only assume that this is another nice feature of
['Green Vista'][3] and that I really don't have any hardware problems.

Has anyone else seen the same behaviour?

[1]: http://www.velocityreviews.com/reviews/Thermaltake_ToughPower_550_Power_Supply/1/
[2]: http://www.acpi.info/
[3]: http://www.zdnet.com.au/news/software/soa/Microsoft-goes-on-green-Vista-offensive/0,130061733,339274460,00.htm
