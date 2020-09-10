---
layout: post
title:      "Wrapped in Dispatch"
date:       2020-09-10 17:25:18 +0000
permalink:  wrapped_in_dispatch
---


I think I know a lot about beer. I certainly have a handle on what the current trends are and what the breweries in my area are producing.  However, in my travels I have learned that the craft beer industry is very much segmented regionally.  So when someone, like myself for example, that has tried all the best beers in New England travels to a different part of the country, it’s really difficult to get your head around where to start.  My idea for this project was to use a Rails-backed React app was to help people on the road discover new beers they might like.

Heading into the project I didn’t have a strong understanding of when to use the Redux store and when not to, and wasn’t completely sure of the difference between using state and props. 

Here is a concise-ish version of what I learned as I built out this application:  State is managed locally within a component in our application.  If you need to pass the state from one component to another, you can pass it to a child component via props.  What that means is if you need to communicate state to a sibling component, it has to be managed in the nearest ancestor component, and then passed down through props.  Redux uses the store to manage state which can be accessed by any component, meaning less passing of props down through component trees, and therefore not passing the props through components that don’t have any business knowing that info.  There are other pros and cons to each strategy, but thinking about state, props, and Redux in this way helped me to understand what made the most sense as I built out this React project.

Adding a beer to my application’s database on the front-end seemed like the perfect time to utilize Redux’s dispatch method, since I could add new data to the state without having to pass that new data through multiple components.  For smaller and more short-term changes to state, it made the most sense to manage state locally without adding to the Redux store.

So it seems that for smaller applications, in general, Redux isn’t quite as critical a tool than it is in a large-scale application.  Using both techniques I was able to put together this application that successfully gives me beer suggestions based on my selected style preference and location.  The feature I would like to implement next with this project is to make use of Geocoding to locate the user and nearby beer places of interest.
