---
layout: post
title: "Upgrading Ruby With RVM"
date: 2013-05-16 13:36
comments: true
categories: [Education, Rails, Ruby]
---
[Ruby Version Manager (RVM)](http://rvm.io) is one of my favorite tools in the Ruby ecosystem.  Reason: RVM lets me experiment with Ruby and Rails at will. If I blow something up, I can always wipe out the broken areas without damaging my system. There are other tools, such as [RBenv](), that perform a similar function. But since RVM has always worked well for me, I'm sticking with it.

The latest patch of Ruby 2.0.0, p195, was released yesterday. RVM lets
devs upgrade seamlessly. Here's how.
<!--more-->

```bash
~/Code/Ruby/apps$ rvm upgrade 2.0.0
Are you sure you wish to upgrade from ruby-2.0.0-p0 to ruby-2.0.0-p195? (Y/n): y
Installing new ruby ruby-2.0.0-p195
Searching for binary rubies, this might take some time.
No binary rubies available for: osx/10.8/x86_64/ruby-2.0.0-p195.
Continuing with compilation. Please read 'rvm mount' to get more information on binary rubies.
Installing requirements for osx, might require sudo password.
==> Upgrading 1 outdated package, with result:
pkg-config 0.28
==> Upgrading pkg-config
==> Downloading https://downloads.sf.net/project/machomebrew/Bottles/pkg-config-0.28.mountain_lion.bottle.tar.gz
######################################################################## 100.0%
==> Pouring pkg-config-0.28.mountain_lion.bottle.tar.gz
🍺  /usr/local/Cellar/pkg-config/0.28: 10 files, 636K
Updating certificates in '/usr/local/etc/openssl/cert.pem'.
Warning: found user selected compiler '/usr/local/bin/gcc-4.2', this will suppress RVM auto detection mechanisms.
Installing Ruby from source to: /Users/rth/.rvm/rubies/ruby-2.0.0-p195, this may take a while depending on your cpu(s)...
ruby-2.0.0-p195 - #downloading ruby-2.0.0-p195, this may take a while depending on your connection...
######################################################################## 100.0%
ruby-2.0.0-p195 - #extracting ruby-2.0.0-p195 to /Users/rth/.rvm/src/ruby-2.0.0-p195
ruby-2.0.0-p195 - #extracted to /Users/rth/.rvm/src/ruby-2.0.0-p195
ruby-2.0.0-p195 - #configuring.....................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................
ruby-2.0.0-p195 - #compiling.......................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................
ruby-2.0.0-p195 - #installing ..................................................................................................................................
Retrieving rubygems-2.0.3
######################################################################## 100.0%
Extracting rubygems-2.0.3 ...
Removing old Rubygems files...
Installing rubygems-2.0.3 for ruby-2.0.0-p195...........................................................................................................................................................................................................................................................................................................................................................................................................
Installation of rubygems completed successfully.
Saving wrappers to '/Users/rth/.rvm/wrappers/ruby-2.0.0-p195'........

ruby-2.0.0-p195 - #adjusting #shebangs for (gem irb erb ri rdoc testrb rake).
ruby-2.0.0-p195 - #importing default gemsets, this may take time.......................
Install of ruby-2.0.0-p195 - #complete
Migrating gems from ruby-2.0.0-p0 to ruby-2.0.0-p195
Are you sure you wish to MOVE gems from ruby-2.0.0-p0 to ruby-2.0.0-p195?
This will overwrite existing gems in ruby-2.0.0-p195 and remove them from ruby-2.0.0-p0 (Y/n): y
Moving gemsets...
Moving ruby-2.0.0-p0 to ruby-2.0.0-p195
Making gemset ruby-2.0.0-p195 pristine....
Moving ruby-2.0.0-p0@firstruby20 to ruby-2.0.0-p195@firstruby20
Making gemset ruby-2.0.0-p195@firstruby20 pristine....
Moving ruby-2.0.0-p0@global to ruby-2.0.0-p195@global
Making gemset ruby-2.0.0-p195@global pristine....
Moving ruby-2.0.0-p0@rails40 to ruby-2.0.0-p195@rails40
Making gemset ruby-2.0.0-p195@rails40 pristine....
Moving ruby-2.0.0-p0@ruby-library to ruby-2.0.0-p195@ruby-library
Making gemset ruby-2.0.0-p195@ruby-library pristine....
Moving ruby-2.0.0-p0@store_engine to ruby-2.0.0-p195@store_engine
Making gemset ruby-2.0.0-p195@store_engine pristine....
Do you wish to move over aliases? (Y/n): y
Do you wish to move over wrappers? (Y/n): y
Do you also wish to completely remove ruby-2.0.0-p0 (inc. archive)? (Y/n): y
Removing ruby-2.0.0-p0........
Successfully migrated ruby-2.0.0-p0 to ruby-2.0.0-p195
Upgrade complete!

~/Code/Ruby/apps$
```
