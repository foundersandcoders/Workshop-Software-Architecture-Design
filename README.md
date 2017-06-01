# Introduction to Software Architecture Design

### Learning Outcomes
- To understand the general importance of software architecture design.
- To start developing the critical ability to identify distinct elements of your app and their relations.
- To apply this knowledge, and learn how you might begin architecting an app pre-build.

### What Is Software Architecture Design?

<iframe src="https://giphy.com/embed/85O5hFDD2xWeY" width="480" height="274" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/software-85O5hFDD2xWeY"></a></p>

##### Architecture is the high-level / overall structure of a software system.

It is like showing a route on a map. Both the route and the map display are abstractions. They don't exist in real life, but they allow us to find our way and conceptualise the landscape.

<iframe src="https://giphy.com/embed/kxhY6bj6JA7Qs" width="480" height="239" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/world-satisfying-map-kxhY6bj6JA7Qs"></a></p>


##### Architecture shows how all the parts of an app might interact with each other.

We can take the example of making an API call from the front end.

![](http://www.dnbpartner.com/wp-content/uploads/2015/02/an_api_call.jpg)

- Our user interacts with the graphic interface, maybe they click a button with an event listener attached to it.
- This triggers an instance of an API call.
- The API call sends a request to the database server, which returns a response.
- The response is a big object which needs to be filtered through.
- The desired results are sent to the DOM, updating the display.
- The user interacts with the updated graphic interface.

_The cycle continues..._

Let's draw how this might appear on the board.

## Types of Software Architecture

There are [many different ways to design a map](https://www.thoughtco.com/types-of-maps-1435689), depending on its purpose. You get road maps, political maps, climate maps, topographic maps... maps provide a very interesting insight into our ability to work with abstract information.

Similarly, there are many different approaches to architecting software, depending on the situation.

For a comprehensive overview of different Architectural Styles and Patterns, have a cheeky look at [this guide](https://msdn.microsoft.com/en-us/library/ee658117.aspx). But don't get overwhelmed; every organisation you work with will have a unique approach to architecture that you will learn on the go.

Let's look at some examples of common architectural styles.

We'll split into our project groups and tackle one style per group.

| Style        | Description           | Example Diagram  |
| ------------- |:-------------:| -----:|
| Client/Server      | Segregates the system into two applications, where the client makes requests to the server. In many cases, the server is a database with application logic represented as stored procedures. | ![](http://4.bp.blogspot.com/-U7IWBX8Od2E/UVQsx7PuVyI/AAAAAAAAABU/m5ckgXBLl-A/s1600/cc.jpg) |
| Layered or Multitiered Architecture      |    Partitions the concerns of the application into stacked groups (layers).   |   ![](https://upload.wikimedia.org/wikipedia/en/6/66/Overview_of_a_three-tier_application.png) |

When your group shares your findings with the rest of the cohort, consider the following:

- When might you use your architectural style?
- Are there advantages/disadvantages?
- What is the simplest way to draw it?

## Why is Architecture Important?

Scenario 1. You're in a rush to leave home and you can't find your keys. Your room is super messy and your keys could be in 1 of 57 places. You are late and miss the first part of your morning challenge at F&C. Doh!

Scenario 2. All of your belongings are arranged according to categories. There's only one place your keys could be. Life is a breeze.

##### Messy systems. On a micro or macro level, they're difficult to maintain, test, extend, scale, and reason about.

Messy systems are costly and they cause frustrating delays.

Clean and ordered systems mitigate complexity and make your life easier in the long run.  

<blockquote>
"The quality and longevity of a software system is determined by its architecture" -- Linda Northrop in ["The Importance of Software Architecture"](http://csse.usc.edu/GSAW/gsaw2003/s13/northrop.pdf), Carnegie Mellon University.</blockquote>

Be a Monica, not a Rachel.

<iframe src="https://giphy.com/embed/26FPxK7LVhEHammiY" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/friends-nick-at-nite-26FPxK7LVhEHammiY"></a></p>

<!-- ## Decisions, Decisions

There are some major decisions that you must make when you are planning a project. Making these decisions is a key part of iteratively developing your architecture design.

You need to:

- Determine the Application Type
- Determine the Deployment Strategy
  _"Your application may be deployed in a variety of environments, each with its own specific set of constraints such as physical separation of components across different servers, a limitation on networking protocols, firewall and router configurations, and more."_
- Determine the Appropriate Technologies
- Determine the Quality Attributes
  _e.g. run-time qualities, security, performance, usability, scalability_
- Determine the Crosscutting Concerns
  _Where can you use centralised solutions to problems that are specific to more than one layer of your application?_

-- "Key Design Considerations", from the [Microsoft Application Architecture Guide](https://msdn.microsoft.com/en-us/library/ee658124.aspx#DesignConsiderations) -->

## Key Principles To Keep in Mind

We're going to start designing the architecture for our own app in a bit.

When you are architecting an app, try to keep these key principles in mind:

- How can you separate your concerns? i.e. keep unrelated things in separate sections
- Which aspects of your app are generic, and which are specific to your requirements?
- How can you make it easy to test?
- How can you make it easy to change?
- Can you anticipate changes that are likely to occur?

Take a few minutes to look at your Week 2 project and come up with answers to these questions:

- Would you change the architecture of your app based on your answers to these questions?
- What would your new file structure look like?

If you finish early, [here](https://msdn.microsoft.com/en-us/library/ee658124.aspx#KeyDesignPrinciples) are some more detailed Key Principles.

## Group Exercise: Whiteboard Your Architecture

<iframe src="https://giphy.com/embed/l2SpKy09apbIwmXVS" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/southparkgifs-l2SpKy09apbIwmXVS"></a></p>

There are 2 main reasons why you should whiteboard your architecture:

- If you cannot whiteboard the architecture then it suggests that it is not well understood.
- If you can provide a clear and concise whiteboard diagram, others will understand it and you can communicate details to them more easily.

We have already drawn some architectural diagrams together.

Now it's time to get into  your project groups Again. We're going to architect a hypothetical app together.

This will be good practice for starting your projects tomorrow, and for all future projects for that matter.

##### Your Hypothetical App  

_Wherever The Weather_ gets a weather forecast for the area that the user is in, without the user having to input any information about their location.

1. When the user loads the page, a request is made to [SERVER A] to get their IP address.
2. The IP address is used to determine their device's location, by making a request to [SERVER B], the Google Maps Geolocation API.
3. The location is then passed to [SERVER C], a weather API which returns a response object for weather in that location. The relevant information is extracted from the response object and displayed in the DOM.

<iframe src="https://giphy.com/embed/3oriOaEFmDeLQPCFcQ" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/hr-fernsehen-weather-forecast-3oriOaEFmDeLQPCFcQ"></a></p>

##### Remember:

- There is no right way to show your architecture in a diagram. You need to decide as a group which approach(es) you will adopt, as long as you can justify your choice.
- The most important thing is to simplify without leaving out crucial processes.
- Avoid writing code at this point. You can talk about it in terms of pseudo-code if this helps.

## Summary

- Architecture is a conceptual representation of how an app is structured and how all the parts of it interact
- Good architecture mitigates complexity, so that code is easier to maintain, scale, test, and reason about
- There are many different ways of representing architecture, just like there are many different types of map
