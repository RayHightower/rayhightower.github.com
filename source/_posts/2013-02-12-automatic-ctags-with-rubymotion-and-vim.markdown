---
layout: post
title: "Automatic ctags with RubyMotion and Vim"
date: 2013-02-12 19:35
comments: true
categories: 
---
[Ctags](http://ctags.sourceforge.net/whatis.html) is a plugin for Vim that helps developers to write code faster and with fewer errors. For example, when creating a new class called `HomeViewController` that inherits from `UIViewController`, typing the first view characters of the superclass will produces the drop-down shown below.


RubyMotion includes a `rake` task that generates tags for a project. To generate tags, run the following in the root directory of a RubyMotion project.

``` bash
$ rake ctags
```



I like the efficiency that ctags brings to the table. But I don't want to type `rake ctags` every time I create a new RubyMotion app. Clearly there must be a way to save time! 

Every time I create a new RubyMotion app, I want ctags to be operational as soon as I jump into the code with Vim. So… I created an alias in my `~/.bash_profile` to do this for me. Here's what it looks like.

alias rm = 'motion create ARG[0]

Hopefully this will save you time too.

If you notice any potential problems with this approach, feel free to send me a "heads up" via the contact form on this site, in the blog comments below, or via a pull request. 

After the bash script ends, it lands in the directory from which it was originally run, regardless of where the script may have cd'd while running. So after the script is complete, do $ cd new_app_directory_name to get to your app.


If you're learning Ruby or RubyMotion or any language for that matter, the best thing you can do is create a whole bunch of apps, over and over again. Create and destroy. Create and destroy. It's part of the power behind Corey Haines' code retreats. What's the possessive case of Corey Haines? is it Haineses? Whatever. That guy's code retreats. At code retreats, devs get together to create and destroy apps over and over again. The more you can create and destroy in a given unit of time, the more you can learn. The more you can commit mundane tasks to muscle memory so that your higher order brain can focus on the real work, which is turning business requirements into working software.

So… Use ctags. Even better, use some sort of script that sets up your RubyMotion app with ctags for you so all you have to do is create the app, hop into your editor, and go!

****** Out Takes ************************
Tell RubyMotion to run '$ rake ctags' immediately after creating the new RubyMotion app
