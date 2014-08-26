---
layout: post
title: "Finding a New Home for the Web"
date: 2013-11-03 11:30
comments: false
categories:
published: true 

---
#The Goal

The main idea was to have a place where I can post personal thoughts and information.  Of course, there are quite a few options available that could do the job.  Wordpress is a popular blogging platform that has been around for a while.  I've tried  it a few years back and it struck me how bloated the service was for what I wanted to do with it.  

So lets have a look at the requirements I was looking for in a blogging platform:

* Open source
* Offered self-hosting
* Supported Mardown
* Fast and customizable
* Static
* Secure

#Solution
This list alone brought down the available options to a very small number.  At first I stumbled upon Jekyll, written in Ruby, which seemed to do pretty much everything I wanted.  After starting the process for setting it up, I quickly realised that it would take a very long time to get it running since theming would have needed to be done by myself and my time is limited (I'm no HTML/CSS/javascript guru).  This led me to [Octopress](https://github.com/imathis/octopress), which is a framework for Jekyll and takes care of all the "boring stuff".  In other words, you clone the Octopress repo into a directory, point your web server config to the proper file and presto, you're up-and-running - ready to start writing.  

The nice thing with Octopress is that it comes with a default theme, similar to the one used at [octopress.org](http://octopress.org), already installed, with the installation of a new theme (built by the community) only 3 commands away.  Visite the About page for information on how to use the theme of this site.

How does the typical workflow look like?  Very simple!
    rake new_post["New Post Name"]
    vim /path/to/new/post.md (to write the article)
    rake generate

And Octopress takes care of converting the markdown file to HTML, and updating the blog and archives with the new article.  

Since everyting is just a text file, it makes it convenient to use revision control such as git as well as edit the files in Vim over SSH.  This puts you in total control of your blog and its content.

#Conclusion
There are of course other alternatives out there, such as [Pelican](https://github.com/getpelican/pelican) which is written in Python or [Sculpin](https://sculpin.io) that is written in PHP, and they might better suite other specific needs.  Octopress will be my platform of choice for the time being however since I'm quite happy with it.
