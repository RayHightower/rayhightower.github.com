---
layout: post
title: "Ruby on Raspberry Pi"
date: 2012-12-03 06:38
comments: true
categories: 
---

<img src="/assets/raspberry_pi_iphone.png" width="400" align="right">
Raspberry Pi is single-board computer roughly the size of a deck of cards. It's equipped with an ARM processor that runs Linux. USB ports let you attach a keyboard and mouse. Video is supported via HDMI and RCA. Storage comes in the form of SD cards. There's an Ethernet port. 

Even better: You can buy a Raspberry Pi for $35.00.

#### Why Raspberry Pi?
Raspberry Pi was created by a group of UK educators and engineers with a concern: Inexpensive hobbyist computers like the old Commodore 64 no longer exist. Game consoles continue to get better, but there is no replacement for the Commodore. As a result, young people who _might_ become developers get introduced to the profession as gamers or users of Word or Excel. They begin as consumers, not creators. Sad news, because it's creators who shape the world that we all enjoy. 

Creators get stronger when they have tools for learning, play, and growth. Enter Raspberry Pi. It's a tiny, inexpensive computer. It runs open source software so it is highly accessible to curious minds that are eager to learn.

#### Will it Run Ruby?
When my Raspberry Pi arrived, I was curious: Will it run Ruby? How about Rails?  This article describes my procedure for installing RVM, Ruby, and Rails on a Raspberry Pi, along with the "gotchas" I encountered along the way.
<!--more-->
#### Yes, It Will Run Ruby
Here's a screenshot from my Raspberry Pi with the Midori web browser, RVM, Ruby 1.9.3-p327, Rails 3.2.9, Vim 7.3, and other tools.

<img src="/assets/RaspberryPi-Desktop.png" width="800" align="middle">

#### Getting Started
Here's what you need to get Ruby running on your Raspberry Pi.

* 1 Raspberry Pi with 512MB RAM or more. I bought mine from [Newark/element14](http://newark.com).
* 1 Monitor that accepts HDMI or RCA video input.
* 1 HDMI or RCA cable, depending on your monitor.
* 1 USB keyboard
* 1 USB mouse
* 1 8GB (or larger) SD card. The instructions recommend 4GB, but I suggest at least 8GB if you expect to run Rails. You'll need room for gems, git, etc.
* 1 Ethernet cable w/RJ-45 ends. 
* 1 high-speed Internet connection.
* A separate computer capable of writing an SD card image, or an SD card pre-configured for Raspberry Pi.

The makers of the Pi have tested the device with SD cards as large as 32GB. I see no harm in using a larger card. More room for testing.

#### Prepping the SD Card
The Pi's operating system boots from the SD card. I found several methods for prepping the SD card with the Raspberry Pi system. The easiest: Buy a Pi with a pre-configured SD card. 

My Pi arrived before the kit containing the pre-configured SD card. I'm a little bit impatient when it comes to new gadgets, so I decided to prep an old SD card of my own.

_Note:_ If your'e reading this article, you already know the standard disclaimer about how technology changes rapidly therefore this procedure could be wrong by the time you read this. I've included links to references so you can check for updates on your own. You know the risks. Please backup everything that needs it.


References:

* [eLinux SD Card Setup](http://elinux.org/RPi_Easy_SD_Card_Setup). Methods for putting your preferred image on the SD card. I chose the "OS X mostly GUI" method.
* [Raspberry Pi Official Downloads](http://www.raspberrypi.org/downloads). Several SD card images, and a beginners wiki.

Prepping an SD card takes a _long_ time. In my case, it took 23 minutes from the time I executed the SD write command to the completion of the process. It was a little disconcerting because the system didn't do anything during that time. No feedback whatsoever. Sounds like an opportunity for a pull request!

#### Starting the System
To start your Raspberry Pi system:

* Plug the SD card, USB keyboard & mouse, Ethernet cable, and video cable (HDMI or RCA) into their corresponding sockets.
* Plug in the USB power adapter.

Linux will boot in text mode. When the system is done booting, you will be prompted for a username and password:

``` bash
raspberrypi login: pi
Password: raspberry
````

A few seconds later, you will be greeted with the $ prompt. You can continue to use the Pi in text mode, or you can start the X Window GUI with:

```
$ startx
```

#### Gotchas
The installation process was relatively smooth. Still, here are a few gotchas I encountered with the Pi:

* I already mentioned this, but it's worth repeating: It took 23 minutes to write the SD card, and there was no feedback along the way. This wasn't a big deal since I had been pre-warned by one of the wikis.
* apt-get needed an update before I could install git.
* The Pi will do absolutely nothing without a properly configured SD card. You know how a PC will partially boot (to CMOS) even without a hard drive? Not so with the Pi.
* The micro-USB power port requires 700mA or more of current. Most micro-USB power adapters don't deliver this month. I happened to have one on hand from another device.

#### For Screenshots, Try Scrot
To take screenshots of the Raspberry Pi desktop, I used Scrot (SCReenshOT). Here's how to install Scrot:

```
$ sudo apt-get install scrot
```

After you install Scrot, this command will take a shot of the entire desktop an drop it into a file called desktop.png in your home directory.

```
$ scrot ~/desktop.png
```

To pause for five seconds and then take the screenshot:

```
$ sleep 5; scrot ~/desktop.png
```




<img src="/assets/raspberry-pi-analog-TV.jpg" width="400" align="right">
#### Analog TV
Don't laugh: I still have an old analog TV in my living room. It's only twelve years old and it still works. Since every Raspberry Pi comes with an old-fashioned RCA video output, analog TVs are useful again.

Here's Raspberry Pi running with my old analog TV as a monitor. Reminds me of the Commodore 64 days!

#### Conclusion
Raspberry Pi will never replace my primary machine because it's too slow. But it is certainly fast enough for learning. More important: It's a very cool toy. Something tells me that it will continue to improve.

To the Raspberry Pi Foundation: Thank you for an impressive device. I wish you much success. 
