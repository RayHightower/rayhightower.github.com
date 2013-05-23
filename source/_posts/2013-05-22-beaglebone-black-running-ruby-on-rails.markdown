---
layout: post
title: "BeagleBone Black, Up & Running"
date: 2013-05-22 22:13
comments: true
categories: [BeagleBone Black, Education, Rails, Ruby]
---
<img src="/images/BeagleBoneBlack.jpg" width="372" height="600" title="BeagleBone Black" alt="BeagleBone Black" align="right">
BeagleBone Black, like the [Raspberry Pi](/blog/2012/12/03/ruby-on-raspberry-pi/), is a small, inexpensive computer that runs Linux. It's smaller than a deck of cards and you can buy one for about forty-five dollars ($45.00). The device is made by [CircuitCo](http://circuitco.com) in Richardson, TX.

###It Just Works
BeagleBone Black runs Linux right out of the box. Steps required:

* Plug in the micro-HDMI cable for the monitor. See the "Gotchas"
  section about micro-HDMI below.
* Plug the keyboard & mouse via the USB port. You might need a USB hub because the board only has one USB port.
* Adding power via the mini-USB port or the 5v power connection. 

After a few minutes of boot time, we have a fully-functioning Linux computer with a GUI, Firefox browser, and other tools.
<!--more-->
Here's a screenshot after just a few minutes of ownership.

<center><img src="/images/BeagleBoneBlack-WindyCityRails.png" width="600" height="338" title="BeagleBone Black Firefox WindyCityRails" alt="BeagleBone Black Firefox WindyCityRails" align="center"></center>

<img src="/images/micro-HDMI-home-depot.jpg" width="400" height="300" title="Micro HDMI Home Depot" alt="Micro HDMI Home Depot" align="right">
###Gotchas
The manufacturer was thoughtful enough to include a mini-USB cable with the device, so you can power it up immediately after it arrives in the mail. However, you won't be able to see anything unless you already have a micro-HDMI cable for your monitor connection. 

<img src="/images/BeagleBoneBlack-USB.png" width="250" height="200" title="BeagleBone Black USB" alt="BeagleBone Black USB" align="right">
###Documentation
All of the paper documentation for the BeagleBone Black fits on a slip of paper roughly the size of two business cards. The meat of the documentation resides on the device itself. To reach the documentation:

1. Plug the BeagleBone Black into a USB port on your laptop.
2. The board will appear as a USB storage device. One of the files at the
root of the storage device, `START.htm`, contains the documentation. It
can be viewed in a web browser.

The documentation recommends against [MSIE](http://en.wikipedia.org/wiki/Internet_Explorer).

###Installing Rails
I will have to cover Ruby and Rails installation in a future blog post because my initial attempts have been unsuccessful. RVM, Ruby, and Rails installed easily with Raspberry Pi, even though the wait was long. With the BeagleBone Black, I got the following in response to the `curl` command:

```bash
sh-4.2# curl -L https://get.rvm.io | bash -s stable --ruby
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
curl: (77) Problem with the SSL CA cert (path? access rights?)
sh-4.2# 
```

Maybe it's time to try [RBEnv](https://github.com/sstephenson/rbenv)? I'll post a solution when I find it. Or... if a reader of this blog already has a solution for the BeagleBone Black Rails installation challenge, please post in the comments below and I'll credit you here.

