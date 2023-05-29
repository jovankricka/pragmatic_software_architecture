In this lecture, we'll expand our event storming knowledge to cover additional important elements:

* views,
* business processes (policies),
* aggregates and
* external systems.

We have a lot to cover, so let's dive back in our event storming.

Views provide different perspectives on the system's data and state.  
They represent how actors or users perceive and interact with the information to perform tasks in the system.  
By identifying and modeling views, we ensure that our software meets the diverse needs of different
stakeholders.

Let's look at what views we have in our prompt library.

Business processes or policies define the rules and constraints governing the system's behavior.  
They represent the logic and decision-making processes that guide the execution of commands and handling of
events.  
Properly modeling business processes allows us to ensure compliance, enforce rules, and implement complex
workflows.

Our system already has some rules.  
For example...

Aggregates are an important concept in event storming.  
They group together related entities or components into cohesive units.  
Aggregates encapsulate business logic, maintain consistency, and provide transactional boundaries within
the system.  
Proper identification and design of aggregates contribute to a well-structured and maintainable architecture.

Let's look at what aggregates our system might contain...

And finally, external systems represent the dependencies or integrations our software interacts with.  

Let's imagine that we want to allow users to execute prompts against ChatGPT.  
In this case we would have one more command "Execute prompt" and that command would interact with an
external system - "OpenAI API".

By comprehending and modeling views, business processes, aggregates, and external systems, we can create software architectures that effectively address the needs of the users, enforce business rules, and integrate seamlessly with external components.

Join me as we explore these essential components in event storming and learn how to incorporate them into our software architecture.