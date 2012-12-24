---
layout: post
title: "Unix for Ruby Developers"
date: 2012-12-24 16:50
comments: true
categories: 
published: true
---
<a href="http://workingwithunixprocesses.com/"><img src="/images/working-w-unix-processes.jpg" align="right" width="350" height="266"></a>
It is gratifying to know that learning something tangentially related to Ruby will, in fact, teach me more about Ruby. 

[_Working With Unix Processes_](http://workingwithunixprocesses.com/), by Jesse Storimer, is ostensibly about Unix internals. However, in reading this book, I have become more aware of how executables run on my favorite family of operating systems, which in turn gives me more insight into Ruby.

### Passing Arguments
For example, what happens when we pass arguments to a process, Ruby or otherwise? How do the arguments get there? Storimer offers a 1-line Ruby program called `argv.rb` that we can use to play with the ARGV array:

``` bash
~/Code/Ruby/apps/sandbox$ echo 'p ARGV' > argv.rb

~/Code/Ruby/apps/sandbox$ ruby argv.rb what results can we expect here
["what", "results", "can", "we", "expect", "here"]

~/Code/Ruby/apps/sandbox$ 

```
<!--more-->
Once we have our hands on the ARGV array, we can parse it and manipulate it at will.

### Grokking Forks
The section on forks contains a lot of mind-bending fun. The author offers some code to explain how forks work. I had write my own in order to grok forks for myself.

Here's what the code does:
* In the parent process, fork returns the pid of the child process.
* In the child process, fork returns nil.
* Therefore, the *if* block should be executed by the parent process, 
* and the *else* block should be executed by the child process.

``` ruby
puts "Parent process pid (before fork) is #{Process.pid}.\n"

if fork
  current_process = Process.pid
  parent_process = Process.ppid
  printf "Entered the *if* block while running Process #{current_process}."
  printf "\nThe parent of this process is #{Process.ppid}, which should be bash.\n\n"
else
  current_process = Process.pid
  parent_process = Process.ppid
  printf "Entered the *else* block while running Process #{current_process}."
  printf "\nThe parent of this process is #{parent_process}, which should be the original of this process.\n\n"
end
```

Running the above Ruby code produces the following results:

``` bash

```

### Errata Handling
The book is new so you can expect a few typos. If you run into problems with sample code, a quick Google search will lead you to the corrected text. For example, early in the book I had problems with a command that returns the maximum number of processes allowed on a system. Turns out there was a typo, and <a href="http://forums.pragprog.com/forums/261/topics/11191">the correction</a> was posted by the author himself on the publisher's errata page.

### Conclusion
I enjoyed reading _Working With Unix Processes_ because it replaces a belief in "magic" with a sound understanding of Unix. The book is clear and brief with plenty of examples. The author assumes that readers have at least a basic understanding of Ruby. After that, you only need a command line, IRB, and the willingness to explore.
