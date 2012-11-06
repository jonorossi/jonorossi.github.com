---
layout: post
title: "Domain names for every network device"
date: 2008-01-15 12:09:24Z
comments: true
categories: Networking
alias: /blog/archive/2008/01/15/domain-names-for-every-network-device.aspx
---

With IPv6 [around the corner][1] it will become mainstream some time in the near future for all computers to be assigned a routable
IPv6 address. A trend that I'm pretty sure will start in the near future is for network devices in everyone's homes will have a
subdomain of a personal domain name. One pretty big reason is because it will be difficult to remember and type an address like
`2001:0db8:0000:0000:0000:0000:1428:57ab`, compared to something like "john.johnsmithhome.com". I see this getting popular because
more people are starting to remotely access their home network with things like Windows Home Server.

According to [Wikipedia][2], IPv6 provides us with "more than a trillion addresses per square centimeter of surface on the planet".
As mentioned on Wikipedia, not all this address space will be used for allocation to devices, however it is very unlikely we will
ever run out again. We could start leasing IPv6 addresses to another planet ;).

With all its advantages, IPv6 will cause some problems, it will make it harder for network administrators because IPv6 addresses
are so much longer to type and compare. But by far the biggest problem I foresee by assigning a routable IP address to every network
device is that a direct inbound connection can be made by anyone to any network device anywhere. Currently, [NAT][3] protects many
insecure computers in home networks because it does not allow direct connections to network devices unless explicitly set up.
Therefore, home routers will need to be shipped with a firewall that blocks all incoming traffic by default and allows for rules
to be created to open specific ports. End users are going to have to be made more aware that protecting individual machines is more
important than it has been.

A little off topic, but I have asked myself the question before but could never work it out. Why are domain names right to left?
Does anyone know?

Wouldn't "http://com.example.mypc:8080/something/" make more sense compared to "http://mypc.example.com:8080/something/".

I can just imagine IntelliSense for domain names, it would be so sweet. Typing "com.google." would display a list with "www", "mail",
"maps", etc. It would also be useful for the "com.example." example above where you might not remember the full hostname and your
browser could help you out by asking the Domain Name System.

Since the domain name system is a tree of domain names where the subdomains are resolved from the top level domain name (TLD),
resolving left to right makes more sense.

The "com.example.mypc" example above reads like, use the HTTP protocol to connect to the host under the "com" TLD, the "example"
domain name and the "mypc" subdomain" on the application port "8080", then request the resource "/something/".

Most hierarchical representations like code namespaces, web site breadcrumbs and file systems work display left to right. I am
fully aware that this is not going to change, I just wondered why domain names were put in this format to start with.

So are you looking forward to the worldwide deployment of IPv6, or are you happy with IPv4? I know I am looking forward to IPv6,
being a computer geek that loves to play with networks. I can't wait until I will be able to set up a 'real' DNS server at home
and host things wherever I like without worrying about port forwarding and conflicting ports being used by other computers via UPnP.

[1]: http://arstechnica.com/news.ars/post/20080102-icann-to-add-ipv6-addresses-for-root-dns-servers.html
[2]: http://en.wikipedia.org/wiki/IPv6
[3]: http://en.wikipedia.org/wiki/Network_address_translation
