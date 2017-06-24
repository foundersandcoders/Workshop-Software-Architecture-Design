# Introduction to Software Architecture Design

### Schedule
- Set Up and Learning Outcomes \ Individually \ 5 mins
- Read "What Is Software Architecture Design?" \ Individually \ 5 mins   
- Discuss ^ all together \ 5 mins
- Exercise 1 \ All together \ 5 mins
- Read "Why Is Architecture Important?" \ Individually \ 5 mins
- Discuss ^ all together \ 5 mins
- Exercise 2 \ Project groups \ 20 mins
- Presenting findings from Exercise 2 \ All together \ 10 mins
- Go through Key Principles \ As a group \ 5 mins
- Exercise 3 \ Pairs \ Restructure a file system \ 10 mins
- Exercise 4 \ Project groups \ 25 mins
- Wrap up and present ideas \ 20 mins

Total: 2 hours


### Learning Outcomes
- To understand the general importance of software architecture design.
- To start developing the critical ability to identify distinct elements of your app and their relations.
- To apply this knowledge, and learn how you might begin architecting an app pre-build.

### Getting Started

Clone this repo: `git clone https://github.com/lucyrose93/Workshop-Software-Architecture-Design.git`

### What Is Software Architecture Design?

![pixelated building](https://static.pexels.com/photos/10643/photo-1442406964439-e46ab8eff7c4.jpg)

- ##### Architecture is a *general* term for the overall structure of a software system. Fundamentally, it's about managing complexity.

It is like showing a route on a map. Both the route and the map are abstractions of a more complicated reality, allowing us to find our way and conceptualise the landscape.

![maps manage complexity](/maps-manage-complexity.png)

- ##### Software architecture shows how all the parts of an app might interact with each other.

- ##### Architectural concerns also affect our file structure and _how we write code_ in a macro way.

Organising your files is a way to manage complexity.

![file structure](http://www.talesfrompipeline.com/theme/images/file_structure.jpg)

In addition to filing, you can also formulate your code in a way that is readable, testable, scalable, etc.

Don't worry too much about this now; this workshop is not about writing code.

If you are interested in finding out more, [this article](https://toddmotto.com/mastering-the-module-pattern/) gives a lucid explanation.


### Exercise 1: Read the steps below. We will map out an API call on the board taking into account the relationship between the [client](https://techterms.com/definition/client) and [server](https://techterms.com/definition/server).

The diagram below represents a complex reality (an API call) in an abstract way. That's a kind of architecture.

- Our user interacts with the graphic interface, e.g. they click a button with an event listener attached to it.
- This triggers an instance of an API call.
- The API call sends a request to the database server, which returns a response.
- The response is a big object which needs to be filtered through.
- The desired results are sent to the DOM, updating the display.
- The user interacts with the updated graphic interface.

_The cycle continues..._

![](http://www.dnbpartner.com/wp-content/uploads/2015/02/an_api_call.jpg)


## Why is Architecture Important?

Scenario 1. You're in a rush to leave home and you can't find your keys. Your room is super messy and your keys could be in 1 of 57 places. You are late and miss the first part of your morning challenge at F&C. Doh!

Scenario 2. All of your belongings are arranged according to categories. There's only one place your keys could be. Life is a breeze.

##### Messy systems. On a micro or macro level, they're difficult to maintain, test, extend, scale, and reason about.

Messy systems are costly and they cause frustrating delays.

Clean and ordered systems mitigate complexity and make your life easier in the long run.  

<blockquote>
"The quality and longevity of a software system is determined by its architecture" -- Linda Northrop in ["The Importance of Software Architecture"](http://csse.usc.edu/GSAW/gsaw2003/s13/northrop.pdf), Carnegie Mellon University.</blockquote>

## Types of Software Architecture

There are many different ways to design a map, depending on its purpose. You get road maps, political maps, climate maps, topographic maps... maps provide a very interesting insight into our ability to work with abstract information.

Similarly, there are many different approaches to architecting software, depending on the situation.

For a comprehensive overview of different Architectural Styles and Patterns, have a look at [this guide](https://msdn.microsoft.com/en-us/library/ee658117.aspx). But don't get overwhelmed; every application/product you work on will require a unique approach to architecture that you will learn on the go. Similarly, every organisation has its own in-house way of doing things.  

## Key Principles To Keep in Mind :key:

We're going to start designing the architecture for our own app in a bit.

When you are architecting an app, try to keep these **key principles** in mind:

- How can you **separate your concerns**? i.e. keep unrelated things in separate sections
- Which aspects of your app are **generic**, and which are **specific** to your requirements?
- How can you make it **easy to test**?
- How can you make it **easy to change**?
- Can you **anticipate changes** that are likely to occur?

## Exercise 3: Restructuring A File System

Your file structure is an architectural structure in its own right. Again, it is an _attempt to manage complexity_.

Keeping the Key Principles above in mind, how would you reorganise the files of this repository? (They are intentionally empty files, by the way.)

_**Tip**: you can run `apm install file-icons` so that all your atom icons have icons, making them easier to distinguish_

If you finish early, [here](https://msdn.microsoft.com/en-us/library/ee658124.aspx#KeyDesignPrinciples) are some more detailed Key Principles.

## Exercise 4: Whiteboard Your Architecture

![](http://mindmappingsoftwareblog.com/wp-content/uploads/2017/03/large-whiteboard.jpg)

##### Why should you whiteboard your architecture?

- If you cannot whiteboard the architecture then it suggests that it is not well understood.
- If you can provide a clear and concise whiteboard diagram, others will understand it and you can communicate details to them more easily.

We have already drawn some architectural diagrams together.

Now it's time to get into  your project groups again. We're going to architect a hypothetical app together. See below for your brief.

This will be good practice for starting your projects tomorrow, and for all future projects for that matter.

As a follow-on exercise, write up a proposed file structure plan to suit the architecture that you've drawn out.

For example:

```js
root/
  index.html
  assets/
    css/
      index.css
    scripts/
      index.js
      location_request.js
      forecast_request.js

```

##### Your Hypothetical App  

<!-- _Wherever The Weather_ gets a weather forecast for the area that the user is in, without the user having to input any information about their location.

1. When the user loads the page, a request is made to get their IP address.
2. The IP address is used to determine their device's location, by making a request to the Google Maps Geolocation API.
3. The location is then passed to a weather API which returns a response object for weather in that location. The relevant information is extracted from the response object and displayed in the DOM. -->


##### Remember:

- There is no right way to show your architecture in a diagram. You need to decide as a group which approach(es) you will adopt, as long as you can justify your choice.
- You can think of it as drawing out a flow diagram, showing how all parts of the app interact with each other.
- The most important thing is to simplify without leaving out crucial processes.
- Avoid writing code at this point. You _can_ talk about it in terms of pseudo-code if this helps.

##### Remaining Time?   

Now's the perfect time to go back to your past projects on GitHub and neaten up the file structure.

## Summary

- Architecture is a conceptual representation of how an app is structured and how all the parts of it interact
- Good architecture mitigates complexity, so that code is easier to maintain, scale, test, and reason about
- There are many different ways of representing architecture, just like there are many different types of map
