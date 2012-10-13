---
layout: post
title: "Using RubyMotion With Xcode's Interface Builder"
date: 2012-10-13 18:34
comments: true
categories: 
---

####Executive Summary
RubyMotion is a Mac application that lets developers write iOS apps in
Ruby. Third party libraries, like [Teacup](), accelerate the process of
creating a user interface for an application. But what if you're a
veteran Objective-C developer and you want to use Interface Builder?

This article whill show how to use Interface Builder to create a UI for
a bare-bones RubyMotion application.

####The App: FizzBuzz
For this example we will build an iOS app that calculates and displays
the fizzbuzz function. As a refresher, here's how fizzbuzz works:

* Count integers starting with 1 and incrementing as high as the user
  wants to go.
* If the integer to be displayed is a multiple of 3, display "fizz"
  instead.
* If the integer to be displayed is a multiple of 5, display "buzz"
  instead.
* If the integer to be displayed is a multiple of both 3 and 5 (i.e. a
  multiple of 15) display "fizzbuzz".




####Create the UI in Interface Builder
Xcode's Interface Builder is an intutive GUI for creating GUI's 
