# Layered architecture

Before going deeper into explaining hexagonal architecture let's take a bit of a step back.
In this lecture we will kick off by revisiting Layered architecture.

Chances are high that you have worked with this pattern before.
Most of the applications I worked with in my career were structured in multiple layers.

No wonder this is so, when you try to google “layered architecture” this is what you’ll get:

(image)

Even Google bolds the fact that the layered architecture is the leading pattern for structuring your applications.
There are a lot of articles out there that state it as the de facto standard in any application development.

When I was doing a talk on hexagonal architecture, I asked my audience to think about an application structured with a
very common 3-layer architecture (4 if you count frontend).
Application was supposed to make an HTTP call to another microservice.
I asked this simple question:

* Where does the HTTP client go?

(image)

Answers were quite interesting:

(image)

I will ignore the fact that most people chose FRONTEND most probably because I used the word CLIENT in the question,
and because frontend usually consumes API via HTTP.
The thing that interests me is that a room full of programmers was not able to strongly agree on where to put the HTTP
client in the layered architecture.

This was very interesting.

Perhaps it is good to repeat one more time the sentence emphasised by Google search:

* “The layered architectural style is one of the most common architectural styles.“.

Room full of experienced programmers, all of them having worked with this most common architectural style throughout
their careers, could not agree where to put HTTP client in it.
Not just that, but all available options were chosen.

To get a bit more insight I asked my fellow engineers to think about a use case when this application needs to listen
to a queue on some imaginary message broker.
I asked where would that queue listener go:

I was once again confused with results:

(image)

There were two things which surprised me with this one:

* one more time all options were chosen (there was not a single option that everyone agreed to exclude) and
* most of the programmers chose to put technology-specific queue listener directly into the domain layer.

At the time I did this presentation I had already worked with hexagonal architecture and was completely blown away by
tremendous increase in clarity on “what goes where“ that it brings.
Also, I found its ability to keep code clean and maintainable and prevent “big ball of mud” so much more powerful than
most of the other patterns for structuring code I used until then.

When I asked those two questions above, what developers actually did is:

* they did not agree on “what goes where” in layered architecture and
* they leaked technology details (HTTP, queue listener) into the domain.

This is exactly what hexagon can help you prevent.
Let's find out how in the next lecture.