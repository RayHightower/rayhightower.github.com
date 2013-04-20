---
layout: post
title: "Ack: Written Perl, Useful With Ruby"
date: 2013-04-20 17:12
comments: true
categories: 
---
<img src="/images/ack.png" align="right" height="237" width="230" alt="Ack Linux Mac OS X" title="Ack Linux Mac OS X">

[Ack](http://beyondgrep.com/) is a command line tool that lets developers search large trees of source code very quickly. If you are looking for a method definition in a haystack of files, Ack will find the needle for you. Many devs regard Ack as a replacement for [grep](http://en.wikipedia.org/wiki/Grep).

The Elmhurst [ChicagoRuby](http://chicagoruby.org) meetings are always a source of unexpected learning. Today we were joined by [Andy Lester](http://twitter.com/petdance), creator of Ack. Andy released Act v 2.0 two days before the meeting. He shared some of the latest features in an impromptu demo.

<!--more-->
####Installing Perl on Mac OS X
Ack requires the Perl programming language. Perl comes pre-installed on Mac OS X and most Linux distros. If you're running on a 'nix platform, you already have Perl.

Windows installations are beyond the scope of this article. If you're running Windows, you might consider a Linux VM for Ruby and Rails-related work.

####Installing Ack on Mac OS X
Installing Ack is so easy that it almost feels wrong: Grab Ack in a single Perl file and drop it in your `~/bin/` directory. That's it. 

Here's a more detailed version of the steps:

# If you don't have one already, create `~/bin/` as a subdirectory of your home directory.
# Grab a the single-file copy of Ack from [http://beyondgrep.com/ ](http://beyondgrep.com/)
# Drop the single-file copy of Ack into a file called `~/bin/ack`
# Make sure that `$HOME/bin` appears at the beginning of your `$PATH` environmental variable.

As of this writing, you should be running Ack v2.0. To verify:

```bash
~/bin$ ack --version
ack 2.02 (git commit f3c8827)
Running under Perl 5.12.4 at /usr/bin/perl

Copyright 2005-2013 Andy Lester.

This program is free software.  You may modify or distribute it
under the terms of the Artistic License v2.0.

~/bin$
```

Now, let's have some fun with Ack.

####Using Ack With Vim

####Using Ack at the Command Line




####Why Ack?
When you're working on a project, maintaining focus is priceless. Have
you every been working on a project, only to be interrupted when you
have to look for something? A minor distraction can 


####Ack.Vim
Ack.vim is a Vim plugin that lets you...



