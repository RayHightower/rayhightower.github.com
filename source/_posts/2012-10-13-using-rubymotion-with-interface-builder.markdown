---
layout: post
title: "Using RubyMotion With Xcode's Interface Builder"
date: 2012-10-13 18:34
comments: true
categories: 
---

####Executive Summary
[RubyMotion](http://www.rubymotion.com/) is a Mac application that lets developers write iOS apps in
Ruby. It's possible to create the user interface for the IOS app entirely
within RubyMotion or with a gem like [Teacup](https://github.com/rubymotion/teacup). But what about devs who prefer Interface Builder?

This article will show how to use Xcode's Interface Builder to create a UI for
a basic RubyMotion application.

####Our Sample App: FizzBuzz
For this example we will build an iOS app that calculates and displays
the fizzbuzz function. As a refresher, here's the fizzbuzz algorithm:

1. Count integers starting with 1 and incrementing as high as the user wants to go.
2. If the integer to be displayed is a multiple of 3, display "fizz" instead.
3. If the integer to be displayed is a multiple of 5, display "buzz" instead.
4. If the integer to be displayed is a multiple of both 3 and 5 (i.e. a multiple of 15) display "fizzbuzz".

Here's a video of our fizzbuzz app running in the iOS simulator.



####First, Build the RubyMotion App
We start by building the fizzbuzz app in RubyMotion. You'll find a copy
of the finished app at [github.com/rayhightower/fizzbuzzrm](github.com/rayhightower/fizzbuzzrm).

####Build the UI in Interface Builder
Start by building the UI in Interface Builder. In our example, we only
have four objects on our single-view interface: A label and three
buttons.

Next, click on the label, and scroll down to... Assign tag number 1 to
the label. Assign tags 2, 3, and 4 to the plus button, minus button, and
reset button, respectively.

Save the interface builder file in the <code>/resources<code> directory
of your RubyMotion app. In this example, the file is called
<code>fbib.xib</code>.

At this point, we're done with IB. Back to RubyMotion.

####Connecting the .xib file to the RubyMotion App




####Create the UI in Interface Builder
Xcode's Interface Builder is an intutive GUI for creating GUI's 
