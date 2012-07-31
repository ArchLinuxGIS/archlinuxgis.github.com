---
layout: post
title: Repos not available
author: Emiliano Vavassori
authref: http://syntaxerrormmm.zapto.org
category: blog
tags:
    - repo
    - network
    - ISP
---
Today [Huub Munstege](https://plus.google.com/110590337815162302339/posts)
reported in the `-dev` mailing list reporting that he had problems on two
installation with ArchLinuxGIS repository.

As I suspected, the problem was due to the fact that my IP address was not
updated by my Dynamic DNS Update client (which was
[ddclient](http://sourceforge.net/apps/trac/ddclient)). Recently it
discomforted me a little, since it was hanging strangely and did not report
anything in the syslog (even if it was instructed to do so).

I've started investigating in [inadyn](http://www.inatech.eu/inadyn/), which
is great since it is written in C/C++ so it is sleek and efficient. I
implemented it as my new Dynamic DNS Updater, just to find out that
[DynDNS](http://dyn.com/dns/) was not allowing me to update my IP address.
Dear DynDNS, this is the straw that broke the camel's back.

I've since jumped in [No-IP](http://www.no-ip.com/) and I'm happy with it.
I've already used them for ArchLinuxGIS with no problems. So here's why Huub
wasn't able to update his installations (hopefully `:)`).

Anyways, I refreshed the repositories and checked that they was accessible
from the outside, so the issue would be much more likely be solved.

Please run the following command if you experienced some issues with the repos
in the last few days:

    pacman -Syy

Happy hacking to all.
