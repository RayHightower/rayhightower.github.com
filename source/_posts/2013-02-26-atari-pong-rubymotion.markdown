---
layout: post
title: "Atari's Pong, Built With RubyMotion"
date: 2013-02-26 10:35
comments: true
categories: [Education, Objective-C, Ruby, RubyMotion, iOS]
published: true
---
<img src="/images/pong-oc.png" width="300" height="160" alt="Atari's Pong in RubyMotion and Objective-C" title="Atari's Pong in RubyMotion and Objective-C" align="right">
[Atari's Pong](http://en.wikipedia.org/wiki/Pong) is a classic video arcade game from the 1970s. Seeing Pong always gives me childhood flashbacks.

####Pong in Objective-C
I recently completed the iOS Accelerated course at the [Mobile Makers Academy](http://mobilemakers.co/). For one of our homework assignments, we were asked to build a version of Pong that runs on iOS. Our instructor, [Don Bora](http://twitter.com/dbora), started us off with some skeleton code in Objective-C. Each student had to take Don's code and:

* Add paddles.
* Make the ball bounce off the paddles.
* Keep score.
* Let one or two players control the paddles via touch.
<!-- more -->
####Questions to Consider
How do you determine whether the pixels of the ball have collided with the pixels of a paddle? What about wall collisions? When a collision occurs, where should the ball bounce next? Many details to consider. 

####Building Blocks
Of course, Don had already taught us the necessary skills in earlier lectures, labs, and homework. It was our job to put the pieces together. 

Members of the class paired with each other, sharing solutions and advice. In time we each ended up with a working version of Pong in Objective-C. It's exciting to see a favorite childhood game running in the iOS simulator on your own machine, especially if you built the game yourself.

####Pong in RubyMotion
Since my day job revolves around Ruby, I wondered what Pong might look like in [RubyMotion](http://rayhightower.dev/blog/2012/10/29/building-ios-apps-with-ruby-motion/). Here are video clips of my two solutions. The first was written in Objective-C during the Mobile Makers course. The second is my version, written in RubyMotion.

<video of  Objective-C version>

<video of RubyMotion version>

As expected, the two solutions look similar. Source code is on GitHub: 

* [Pong in Objective-C](http://github.com/rayhightower/pong-oc)
* [Pong in RubyMotion](http://github.com/rayhightower/pong-rm)

####Why Play Games?
Why should a serious developer spend time writing games? I can think of a few reasons:

* Writing a game challenges our skills on many levels. In the case of Pong, we have to dust off our old physics and geometry textbooks to ensure that the ball bounces like a real ball.
* Writing a game lets us break out of our constraints. Devs who write business apps are very familiar with constraints.
* Because writing a game is fun. Get over it :-)

Of course, the most important reason was given by a Captain of the USS Enterprise NCC-1701:
>The more advanced the mind, the greater the need for the simplicity of play.
><br/>~James T. Kirk

####Comments and Pull Requests
I lead a [software team](http://wisdomgroup.com) that builds business apps. My experience with games is limited. If you are a game developer, and if you see anything in my code that could be done better, don't be shy! Feel free to submit a [pull request via GitHub](http://github.com/rayhightower/pong-rm), or you can drop a note in the comments below. Thanks!
