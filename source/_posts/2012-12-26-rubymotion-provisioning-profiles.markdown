---
layout: post
title: "RubyMotion Provisioning Profiles"
date: 2012-12-26 20:46
comments: true
categories: 
published: true
---
<img src="/images/provisioning-profile.png" align="right" width="96" height="117"></a>
_Note: This article on provisioning profiles was first posted in the <a href="https://groups.google.com/forum/?fromgroups=#!topic/rubymotion/Nvo8dH_8rkI">RubyMotion Google Group</a> on May 10, 2012. The response was also referenced by <a href="http://stackoverflow.com/questions/13539743/rubymotion-build-error-cant-find-a-provisioning-profile-named-mixios-tea">Stack Overflow</a>_

Everything with RubyMotion worked great until I tried to run the sample apps on a physical device. And then I had to spend a few hours wrestling with provisioning profiles. Hopefully this post will save time for somebody else. 

In order to successfully run a RubyMotion app on a non-jailbroken iPhone 3GS (via "rake device") I had to: 

* Delete all of the expired provisioning profiles in the Mac OS X Keychain Access app. Yeah, my past is littered with many random experiments :-) 
* Explicitly set the path to my provisioning profile in the rakefile for the app (the defaults didn't work for me). 
* Explicitly set the name of my codesign_certificate. 

The default "iOS Team Profile" didn't work for me. I had to set explicit values in my rakefile for the app. Here's my rakefile for the 'Tweets' sample app at https://github.com/HipByte/RubyMotionSamples: 

``` ruby
    $:.unshift("/Library/RubyMotion/lib") 
    require 'motion/project' 
    Motion::Project::App.setup do |app| 
      # Use `rake config' to see complete project settings. 
      app.name = 'Tweets' 
      app.provisioning_profile = '/Users/[username]/Library/ 
 MobileDevice/Provisioning Profiles/[string-of- 
 numbers].mobileprovision' 
      app.codesign_certificate = 'iPhone Developer: John Q Developer 
 (A5QZ9QF4Z1)' 
    end 
```

Of course, my name isn't "John Q Developer", but you get the idea. Hope this helps! 
