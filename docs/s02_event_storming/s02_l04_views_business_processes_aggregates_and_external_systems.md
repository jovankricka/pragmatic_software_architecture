In this lecture, we'll focus on remaining four event storming elements:

* views,
* business processes (policies),
* aggregates and
* external systems.

We have a lot to cover, so let's dive back in our event storming session.

## Views

First we will focus on **views**.
Views provide different perspectives on the system's data and state.  
They represent how actors or users perceive and interact with the information to perform tasks in the system.  
By identifying and modeling views, we ensure that our software meets the diverse needs of different
stakeholders.

Let's look at what views we have in our prompt library.

* We know that users will be registering via the **signup view** and logging in via the **log in view**.
* Once they are in the app, they will be viewing the **main dashboard**. This is also a view.
* Finally, both **prompt** and **category** entities will have their own views.

Let's include this in our model.

## Policies

Business processes or policies define the rules and constraints governing the system's behavior.  
They represent the logic and decision-making processes that guide the execution of commands and handling of
events.  
Properly modeling business processes allows us to ensure compliance, enforce rules, and implement complex
workflows.

Our system already has some rules.  
For example:

* Only users can create prompts or leave reviews.
* Sorting of prompts in a category is also a form of a policy.

Let's include these policies as well.

## Aggregates

Aggregates are an important concept in event storming.  
They group together related entities or components into cohesive units.  
Aggregates encapsulate business logic, maintain consistency, and provide transactional boundaries within
the system.  
Proper identification and design of aggregates contribute to a well-structured and maintainable architecture.

Let's look at what aggregates our system might contain.

* We can see four potential candidates - user, prompt, review and a category. All these can be aggregates
in our domain model.

## External systems

And finally, external systems represent the dependencies or integrations our software interacts with.  

Let's imagine that we want to extend our system and allow users to also execute prompts against ChatGPT.  
In this case we would have one more command "Execute prompt" and that command would interact with an
external system - "OpenAI API".

## Summary

These seven concepts we covered so far allow us to design a domain model that effectively addresses
the needs of the users, enforces business rules, and integrates seamlessly with external components.

Now that we have these in our toolbox, let's look at some tips on how to effectively facilitate event
storming sessions.
