---
layout: post
title:      "Command Line Fun Times"
date:       2020-05-10 21:37:03 +0000
permalink:  command_line_fun_times
---



The content of your blog post goes here.My latest (ok, my first) project was to build a CLI data gem.  Throughout the process of building this I ended up scraping quite a few websites, realizing some websites are much easier to scrape than others.  The good news is a got a lot of practice zeroing in on html elements for scraping.  Once I determined the most appropriate website to scrape in order to achieve the functionality I wanted to build, it was on to the next phase.

Starting the project, I expected the scraping to be the most challenging part.  But for me, as a three week old programmer, it really was putting together all the pieces from the curriculum to-date that took up the majority of my time.  Somewhere in my efforts to write concise object-oriented code I stumbled upon Sandi Metz’ five rules for object-oriented developers.  Of the 5 rules to write good code, the rule that was most applicable to me as a brand new coder was limiting methods to 5 lines.  It was a rule I broke several times, but I found it useful at least as a guideline for abstracting my code and making it as readable as possible.
 
In my command line class I had two loops I was using to get the user to their desired end points.  My first loop included scraping for a current list of the top 50 actors and actresses in the US.  Once the user selects an actor they want more info on, my second loop scraped for all movies in which that actor played role.  My first stab at getting this working resulted in two very long methods.  Using my 5 line per method rule a s a way to guide my thinking, I was able to abstract most of the clunky functionality into other methods, resulting in code that just looks and reads way better. 

Another issue I was having as I was scraping for data was the amount of time that process was taking.  My display_all methods for my Film and Actor classes were expensive because they were scraping the web with every call, and were giving me duplicate results every time the method was called.  So I learned a little bit about memoization!  I was able to utilize memoization in those methods to resolve both of those issues for me in a clear and concise way.

All things considered, my CLI data gem is somewhat simple, but a successful project.  I really learned a lot through the process of starting from scratch to achieving my desired output, and it was incredibly satisfying.  Fine I’ll say it…at this point I’m really just “scraping” the surface of journey to become a programmer, but I’m excited to be moving onward to project number 2!
