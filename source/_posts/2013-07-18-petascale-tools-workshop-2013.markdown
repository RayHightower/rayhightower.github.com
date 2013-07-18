---
layout: post
title: "Petascale Tools Workshop 2013"
date: 2013-07-18 02:12
comments: true
categories: [ Education ]
published: false
---
The Petascale Tools Workshop is for computer scientists who design, build, and test the fastest computers on the planet. Their performance is measured I petaflops: 10<sup>15</sup> floating point operations per second. That's about [1,000 times faster](http://browser.primatelabs.com/geekbench2/1640254) than the fastest MacBook Pro, depending on the type of floating point operation performed. 
<!--more-->
[WisdomGroup](http://WisdomGroup.com) was invited to attend because our client, [Texas A & M University](http://www.wisdomgroup.com/case-studies/texas-am-university/), operates in the high performance computing space. I was the only non-PhD in the room, taking Pat Metheny's [be-the-worst](/blog/2013/07/17/pat-metheny-be-the-worst/) philosophy to the extreme! The more we understand about our clients, the better we can deliver for them. 

###One Megawatt = One million dollars
As with other disciplines of engineering, supercomputer design is all about managing trade-offs. If you increase the clock speed, how much more power will you pay for? If you increase the size of your cache, how much more money will you spend on hardware?

The biggest constraint seems to be electrical power. High performance computers gulp electrical power. To keep things in perspective, it helps to 

One Petascale Workshop attendee remarked, "I know how to genererate a megawatt for only $865,000." He then listed a combination of electrical generation sources, a combination of coal, fossil fuels, and natural gas that would achieve the reduction. The more important point: In the year 2013, it costs a lot of money to generate electrical energy.


###Re-Framing the Problem
One presenter's approach was to look at the problem in terms of performance, not power. His reasoning: No matter where we build high performance computers, we will only have a limited amount of power. The max for most installations is 20 megawatts. Since the constraint is real, lets figure out how to get the best performance we can get within e constraint.

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



