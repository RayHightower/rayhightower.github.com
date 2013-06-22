---
layout: post
title: "Preparing for Parallella's 64 Cores: Installing Go on Mac OS X"
date: 2013-06-22 12:58
comments: true
categories: [ Education, Linux-Unix-OSX ]
---
<img src="/images/parallella.jpg" width="600" height="342" alt="Parallella 64-core supercomputer" title="Parallella 64-core supercomputer" align="right">
The idea of owning a 64-core parallel system for two hundred dollars (yes, $200.00) is exciting. [Parallella](http://parallella.org) is working to make that happen, perhaps as early as August 2013. To prepare for that day, I've decided to introduce myself to the Go language. 
<!--more-->
I was inspired to explore Go by [Blake Smith's](https://twitter.com/blakesmith) presentation at [8th Light](http://www.meetup.com/ChicagoSC/events/120658422/) earlier this month.

####What is Go?
[Go](http://golang.org) is designed for parallel systems. Why does Go exist? A developer friend sums it up well:

>Go was created at Google, by Google, for Google-size problems.<br/>~Dave Aestels

Google writes software that runs on thousands of machines in parallel. As the number of concurrent operations increases, new challenges are encountered. Google addressed those challenges by creating Go.

####Why Does a Rubyist Learn Go?
The team at [WisdomGroup](http://wisdomgroup.com) specializes in Ruby apps. So why am I learning Go?

Because the best developers are polyglot. When we learn a new language, we cause ourselves to see old problems in new ways and we strengthen our ability to solve new problems. It's a similar to cross-training for  athletes. In the end, we become better developers.

####How to Install Go on Mac OS X

1. [Download the binary distribution of Go that matches your system](https://code.google.com/p/go/downloads/list), but don't install it until the other steps are done. For my 2010 i5-based MacBook Pro, I chose `go1.1.1 Mac OS X (x86 64-bit) PKG installer`. I was concerned about the reference to `amd64` in the package name, but this version worked fine for me.

2. If you are upgrading from a previous version of Go, you will need to remove the old Go directory.

```bash
$ rm -rf /usr/local/go
```
You can do this while the download is happening in the background.

3. Setup the `GOROOT` environmental variable. My system uses `~/.bash_profile` to define environmental variables, so I added the following lines to the end of that file:

```bash
export GOROOT=$HOME/go
export PATH=$PATH:$GOROOT/bin
```

4. Run the package installation program that was downloaded in Step 1.

5. Tell your terminal session to recognize the new Go installation. You can either restart terminal, or if your environmental variables are in `~/.bash_profile` like mine, you can do the following:

```bash
$ source ~/.bash_profile
```

Now, let's go for a test drive.


####Writing 'Hello World!' in Go

The official installation instructions include a simple 'Hello World' program for testing the installation. A slightly modified version appears below:

```go
package main

import "fmt"

func main() {
    fmt.Printf("Hey Parallella enthusiasts: Learn Go!\n")
}
```

We can run the Hello World program with the Go tool:

```bash
$ go run hello.go

Hey Parallella enthusiasts: Learn Go!
```

####Next Steps
Now it's time to explore the language. Of course, there's only so much we can do with a 4-core i5. The real adventure begins when the 64-core Parallella arrives. Can't wait!





