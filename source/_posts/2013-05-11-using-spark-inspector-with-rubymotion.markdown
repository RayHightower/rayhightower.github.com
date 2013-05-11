---
layout: post
title: "Using Spark Inspector With RubyMotion"
date: 2013-05-11 23:15
comments: true
categories: 
published: true
---
Any tool that gives me more insight into apps I'm writing gets me excited. I was pumped when [Spark Inspector](http://sparkinspector.com) was released this week. My excitement grew when I learned that Spark Inspector could work with RubyMotion.
<!--more-->
This article is based on a [gist posted by Ben Gotow](https://gist.github.com/bengotow/5552322).

In the project's `Rakefile`, add the following lines.
```bash
Motion::Project::App.setup do |app|
  # Use `rake config' to see complete project settings.
  app.name = 'Pong-RM'

  # Next three lines added to support Spark Inspector
  app.vendor_project '/Applications/Spark Inspector.app/Contents/Resources/Frameworks/SparkInspector.framework', :static, :products => ['SparkInspector'], :force_load => true, :headers_dir => 'Headers'
  app.libs += ['/usr/lib/libz.dylib']
  app.frameworks += ['QuartzCore']
  
  ...

end
```

Add `SparkInspector.enableObservation` to the first line of the `application:didFinishLaunchingWithOptions:` method in
`app_delegate.rb`.

```bash
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    SparkInspector.enableObservation
    
    ...
  
    true
  end
```
