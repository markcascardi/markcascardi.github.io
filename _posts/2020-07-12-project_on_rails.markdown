---
layout: post
title:      "Project on Rails"
date:       2020-07-12 19:04:22 +0000
permalink:  project_on_rails
---


Something I have learned from my 42 years on Earth is that sometimes the most necessary and effective inventions, are not always the sexiest. For my third project, I played around with a few different ideas, but I always came back to one in particular. It is not sexy – but certainly useful. I have written about my past experience in the food & beverage industry a few times, so by now you should know that I have spent a good portion of my career within that industry at a ski resort. One major issue we faced was the disconnect between a few of the payroll systems that were put into place. The idea for this app was to bridge the gap that created a huge bottleneck situation. The mountain had 5 restaurants that food & beverage employees could work at on any given day of the week. Many employees worked at more than one. However, there was no process in place that efficiently funneled all tips into the payroll system in place…meaning, each manager had to manually email in all tips for each employee to the director, and the director would have to add each employee’s tips from every day up, to send to accounting. This created a huge bottleneck situation, so for my project, I aimed to attack that issue by creating a web app that automatically funnels each employee’s tips from every restaurant into one place that can be sent to payroll.
 
I began by devoting a good portion of my time to styling my views. Early on in the process, I opted to use materialize CSS since I liked their default stylings and their supporting documentation was extensive. 

Applying that styling was straightforward, the trickiest part were the forms. Since I hadn’t worked much with CSS prior to this project, I spent time reading up on it and was able to adjust my presentation to my liking. 

This project did not come without setbacks...the issue that lingered longest was the implementation of collection select drop downs. In order to get them to display properly, I found that I had to refresh the page. After spending a lot of time researching this issue, I ultimately opted to disable turbolinks. I’m not certain that was the best workaround, but it fixed the problem and didn’t seem to impact the rest of the project.

In order for this to be an effective payroll tool for users, date filters were added.  That took some time but what I really needed was for the tables to be both sortable AND filterable by date. Since common knowledge tells us that HTTP is ‘stateless’, I had to make sure that my filter dates were getting passed to controller via the helper methods so they could be passed back to the view upon sorting.  When summarizing the process into one sentence it certainly seems easy, and maybe it is, or will be easier the next time.  Either way, now I have a handle on passing additional parameters through a redirect, using hidden input fields in a form, and using an options hash.

I used a table to display and add to each employees tip data in my view.  Perhaps as I learn more JavaScript in the coming weeks I can change that view from a table to a form that I add rows to as needed.  The end result of my rails project did accomplish everything I set out to do, and there’s definitely room for improvement. 

Although this project was not sexy, it would have been darn useful during my time in food and beverage. Has_many tips, as it’s called, saves users time…and time is money!
