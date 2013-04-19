---
layout: post
title: "New RVM Behavior"
date: 2013-04-18 20:33
comments: true
categories: [Rails, Ruby]
---
I trust RVM to manage my Ruby versions and my gems. So when I saw an unexpected change in RVM's behavior, I was concerned about a possible disruption in my workflow. Here's what I saw:

```bash
~/Code/Ruby/apps$ cd hartl/
You are using '.rvmrc', it requires trusting, it is slower and it is not compatible with other ruby managers,
you can switch to '.ruby-version' using 'rvm rvmrc to [.]ruby-version'
or ignore this warnings with 'rvm rvmrc warning ignore /Users/rth/Code/Ruby/apps/hartl/.rvmrc',
'.rvmrc' will continue to be the default project file in RVM 1 and RVM 2,
to ignore the warning for all files run 'rvm rvmrc warning ignore all.rvmrcs'.

Using /Users/rth/.rvm/gems/ruby-1.9.3-p385 with gemset hartl

~/Code/Ruby/apps/hartl[master]$ rvm --version

rvm 1.19.5 (master) by Wayne E. Seguin <wayneeseguin@gmail.com>, Michal Papis <mpapis@gmail.com> [https://rvm.io/]


~/Code/Ruby/apps/hartl[master]$
```

My decision: To move forward boldly. If things don't work out, I can always remove RVM completely and start from scratch.


