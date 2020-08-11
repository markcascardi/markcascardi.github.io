---
layout: post
title:      "Insert fetch pun here"
date:       2020-08-11 01:44:06 +0000
permalink:  insert_fetch_pun_here
---

For my Rails-backed JavaScript project, I revisited the world of sports with the goal of accomplishing functionality that will be useful for tracking your favorite athletes, but as a single page application.  One of the things that helped me get my head around JavaScript was thinking about the it in terms of the three main responsibilities: 1. Recognizing events, meaning adding event listeners that execute some function (or functions) when the criteria of a specified event takes place,  2. Manipulating the DOM, which is adding/editing/deleting HTML, and 3. Communicating with the server, ie sending data changed on the front end back and forth with the database. 

My expectation was that the third piece mentioned above, communication with the server, would be the most challenging, but that wasn’t really the case for me.  I spent the first chunk of time on this project putting together the Rails portion of the project so that there actually was a server to communicate with and corresponding data, and then moved to the front-end.  Making use of the fetch() method I was able to start building out the front end without any styling pretty quickly.  The majority of my time on this project was spent manipulating the DOM and styling with CSS.

Adding event listeners was also not as complicated as I might have imagined before implementing them in my studies, and of course, in this project.  The complicating factors I found were: how to deal with HTML collections, and finding the best way to pass along the id of the record in our database we are trying to create, view, update, or delete.  My most preferred tool to operate on the HTML collections data structure was using the Array.from() method.  This turns that collection into an array that allows me to get at the data inside.  Targeting the correct element and manipulating as desired requires adding some combination of ids, classes, and datasets to HTML elements.  This project provided me with no shortage of opportunities to hone this skill. 

As with my previous project, I used Materialze to style my html.  The default styling looks sharp, but required an a layer of custom css to get input fields on and other elements sized the way I wanted.  While I do like the look of the Materialize CSS, after using it on consecutive projects I can definitively say its biggest area for improvement is its supporting documentation.  On a related note, my biggest challenge was on this project was manipulating the CSS to my liking.  I learned a great deal about CSS on this project, and clearly have plenty of room for improvement on my next project.


