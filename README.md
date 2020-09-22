# Software Engineering Challenge

The current state of our world has prompted online interaction to become the most important thing not only in our workplaces, but in our personal lives as well. In this challenge, we will work on a scenario that turns all of this into opportunity.

One of the things that saw a big insurgence was Livestreaming. As isolation took over the world, online broadcasts became the go to for human interaction for work, classes, socialization and entertainment.

# Scenario

For this challenge, let's consider the following scenario. A company wants to interact with its millions of customers. To do so, they will broadcast a live event that will attract hundreds of thousands of watchers. In order to make the event more interactive, the company wants to also use the chat for interactive polls. Your job is to write a solutions that allows for that interaction. The event will be broadcasted on the Science and Technology category of Twitch.tv, a livestreaming platform.

# Business Requirements

+ Your solution must allow a way of starting a poll. When the channel owner or a channel moderator writes `!poll <QUESTION>` commands, a message containing the question must be sent in chat, and the program must start listening for `!yes` and `!no` responses from the chat. Example: `!poll do you like polls?` should display `do you like polls?` on chat, and start listening for `!yes` and `!no` messages.
+ All questions will be yes or no questions.
+ Users may only vote once per question.
+ The command `!results` should display in chat the overall results of the last question in the format `yes: XX% | no: YY%`. Example `yes: 57% | no: 43%`.
+ Only one question may be asked at once, and the program must deal with this and other corner cases.

# Non-functional requirements

+ Assume the solution will be used by hundreds of thousands of people simultaneously. Your solutions must account for scalability, elasticity and performance.
+ Account for good coding practices and design a scalable architecture that would be easy to maintain.
+ Write all of your code and documentation in English.

# Assigment

You can use whatever tools, language and frameworks you desire. Please setup your project in a well organized and simple to understand structure, as if publishing it as a git repository. You can send your project back to the email you are currently in contact with.

## Code

Provide a zip file of your solution containing all the code and documentation. Please setup your project in a way that is simple to compile, run and build. Document the solution to the best of your ability, making it clear when taking decisions for the design and architecture.

## Architecture

As important as the code is its maintainability. Provide alongside your code a PDF file containing one or more diagrams describing your solution's architecture. Please account for the following requisites:

1. Where will your solution be hosted?
1. What tools will be used to guarantee performance and security?
1. How well does it scale if the number of users rises exponentially?
1. How would implement a data architecture for future analytics? For instance, if the company later asks to see a report with all questions made, their answers, and statistics about the users (how old is their Twitch account, are they followers of the channel, are they subscribers), how would you implement it?

A diagram for each item is not inherently necessary, but please make sure to answer each question.

## Hints

+ You can use the [TwitchIO](https://github.com/TwitchIO/TwitchIO), a Python wrapper to the TwitchBots API to fetch and send messages to Twitch chat. You'll need to create a Twitch account for your bot. To authenticate, you will need to generate an oauth code and register an application. More info [here](https://dev.twitch.tv/docs/irc#next-steps).
+ Wrapping your code in a Docker image makes it very easy to run and deploy.
+ To draw the diagrams, [draw.io](https://www.draw.io/) is an excellent tool.
+ You can take liberties in your design and solutions as long as you follow the requisites. If anything feels ambiguous, be sure to make it clear why you made each decision.
