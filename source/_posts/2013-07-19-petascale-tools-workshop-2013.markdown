---
layout: post
title: "Petascale Tools Workshop 2013"
date: 2013-07-19 02:12
comments: true
categories: [ Education ]
published: true
---
The [Petascale Tools Workshop](http://www.paradyn.org/CSCADS2013/index.html) is for computer scientists who design, build, and test the fastest supercomputers on the planet. Supercomputer performance is measured in petaflops: 10<sup><sup>15</sup></sup> floating point operations per second. That's blazing speed, thousands of times faster than the fastest MacBook Pro. 
<!--more-->
[WisdomGroup](http://WisdomGroup.com) was invited to attend the workshop because our client, [Texas A & M University](http://www.wisdomgroup.com/case-studies/texas-am-university/), operates in the high performance computing (HPC) space. As the only non-PhD in the room, I was given a chance to exercixe Pat Metheny's [be-the-worst](/blog/2013/07/17/pat-metheny-be-the-worst/) philosophy in the extreme! The result: I learned things that will help WisdomGroup to deliver better solutions for our clients, especially the TAMU team. 

###One Megawatt = $1,000,000.00
As with other disciplines of engineering, supercomputer design is all about managing trade-offs. If you increase the clock speed, how will that affect your electrical bill? If you increase the size of the cache, how much more will you spend on hardware?

Every Petascale Workshop presenter highlighted the toughest constraint: The cost of electrical power. High performance computers gulp electricity. The wattage numbers were all very abstract to me until one presenter layed out a direct one-to-one correspondence between electricity and money. _One megawatt of power used over the course of a year costs one million dollars._

Express a constraint in terms of money, and the abstractions melt away.

The debate between the scientists was vigorous yet respectful. After hearing the 1-to-1 rule of thumb, one audience member remarked, "I know how to genererate a megawatt for only $865,000." He then outlined his solution, a combination of coal, fossil fuels, and natural gas that would achieve the reduction. The more important point: Electricity is expensive.

###Re-Framing the Power Problem
There is another way to look at the power problem. Consider it from the perspective of performance, not power. Here's how one presenter put it: No matter where we build a supercomputer, we will only have a limited amount of power. Let's look at the maximum available power as a constraint and go from there.

Today's most powerful supercomputing facilities can deliver a maximum of 20 megawatts, which translates into a $20 million per year electrical bill. This constraint is real; we have yet to build a more powerful facility.

Rubyists are familiar with the saying ["constraints are liberating"](http://gettingreal.37signals.com/ch03_Embrace_Constraints.php), popularized by 37signals. Since the 20 megawatt constraint is real, our next step is to figure out how to extract the best results that the constraint will allow.   

###Digging Deeper
Some of the biggest performance gains can be realized through more efficient software. The fastest supercomputers run some distribution of Linux. An entire community of PhDs focuses on ways to optimize the Linux kernel for supercomputing. Optimization is not a one-size-fits all process. The scientists need to consder the type of application being run, percentage of time spent on I/O, efficiency of algorithms... you get the idea. Each potential point for optimization is like a node on an ever expanding tree.

In the Ruby world, we might use tools like [New Relic](http://newrelic.com) or [Code Climate](http://codeclimate.com) to identify hot spots in our code, places where re-factoring can reduce CPU utilization or I/O. HPC tools, tend to be highly customizable because the users are scientists themselves.







As we say in the Ruby community, [constraints are liberating]().

I was blown away by the presenter's Kaviot graph:

<img src="" width="" height="" alt="" title="" aligh="center"> 

In one image, we can see the relationship between petaflops, cache hits...


###Measuring and Accepting Trade-Offs

Kaviat graph (radar graph)

###Optimization Methods




###Top 500
The top 500 HPC in the world:
http://top500.org/lists/2013/06/


###Sample Optimization
Say you have an application that performs matrix multiplication. Can there be a difference in app performance depending on the order of the loops?

```ruby

```

###Auto Tuning



