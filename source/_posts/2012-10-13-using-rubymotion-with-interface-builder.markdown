---
layout: post
title: "Using RubyMotion With Xcode's Interface Builder"
date: 2012-10-15 18:34
comments: true
categories: 
---

####Executive Summary
[RubyMotion](http://www.rubymotion.com/) is a Mac application that lets developers write iOS apps in
Ruby. It's possible to create the user interface for the app entirely
within RubyMotion or with a Ruby gem like [Teacup](https://github.com/rubymotion/teacup). But what about devs who prefer Interface Builder?

This article will show how to use Xcode's Interface Builder to create a basic UI for
a RubyMotion application.
<!-- more -->

####Our Sample App: FizzBuzz
For this example we will build an iOS app that calculates and displays
the fizzbuzz function. As a refresher, here's the fizzbuzz algorithm:

1. Count integers starting with 1 and incrementing as high as the user wants to go.
2. If the integer to be displayed is a multiple of 3, display "fizz" instead.
3. If the integer to be displayed is a multiple of 5, display "buzz" instead.
4. If the integer to be displayed is a multiple of both 3 and 5 (i.e. a multiple of 15) display "fizzbuzz".

<img src="/assets/fizzbuzzrm.png" width = "200" align = "right">
The bare-bones UI appears at right. The plus sign increments the
counter, minius decrements it, and the label area shows "Begin" at
the beginning.


####First, Build the RubyMotion App
We start by building the fizzbuzz app in RubyMotion.

<code>
$ motion create fizzbuzzrm
</code>

You'll find the code for the finished app at [github.com/rayhightower/fizzbuzzrm](github.com/rayhightower/fizzbuzzrm).

####Build the UI in Interface Builder
Next, build the UI in Xcode's Interface Builder.

Once you've completed the interface, we will need to asign tags to each
element so that the UI knows how to communicate with RubyMotion. Scroll
down to View|Tag in the rightmost colum (screnshot attached). In my
example, I assigned the tags 1, 2, 3, and 4 to the label, plus button,
minus button, and reset, respectively.

Save the IB file in the <code>/resources</code> directory of your
RubyMotion project. In my example, I called the file
<code>fbib.xib</code>. RubyMotion will compile the .xib file next time
you use the rake command to build the ap.

####Connecting the .xib file to the RubyMotion App
Let's head back to the RubyMotion app so we can 




####Create the UI in Interface Builder
Xcode's Interface Builder is an intutive GUI for creating GUI's 
