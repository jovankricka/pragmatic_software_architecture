# Core concepts

All the ambiguity and confusion on how to structure code and where to put things comes from this idea that our mental
model of software should be a series of layers stacked on top of each other.
Let’s forget about that idea for a moment.

Instead of imagining multiple top-down layers, lets imagine a single, central core of the application.
This core is surrounded with plugs (which we call ports).
Ports are the only doors for the application to the outside world.
You can have any number of these plugs that communicate with the world.

This is a very important distinction from the traditional layered architecture, where you aim to model everything with a
limited set of layers.
With the hexagon there are no limits - there is one core and any number of I/O ports.

So the idea is to go from this:

(image)

, to something like this:

(image)

At first, the drawing might seem scary or more complex than the regular app you are used to working with.
However, the actual concept is not.
In fact, the core idea is quite trivial.

There is the “center” and there is an “outside”.
That's all.
That's your app.

“Center” contains your domain model.
This is the brain of your application and, as accurate as possible, code representation of your mental model of the
problem that you are solving.

No mappings, database nuances, juggling with HTTP, transactions, entity flushing, etc. goes here.
None of those things should ever go here.

(image)

“Out” is the bridge linking your domain model and the outside world.
This is where all the “techy” stuff goes.

Those are all the rules.
And they cover everything.
Essentially every application can be viewed as a simple machine able to receive inputs and produce outputs.
Thus, the only thing essentially necessary to structure any such application is the core and the I/O.

By using this simple structure:

* you should never be in doubt about “what goes where” and
* making sure your domain is not polluted with non-domain code will be more straightforward.

Alistair Cockburn is the one who coined the term hexagonal architecture and proposed it in 2005.
He is also one of the signees of the famous agile manifesto.
He is not in the agile manifesto photo, but the rumor is that he is the guy that actually took it.

Jeffrey Palermo proposed something similar with the concept of the onion architecture.
What he did is very similar to hexagonal architecture, only he went further with decomposing the core part in several
concentric rings (hence the 🧅).

Also, in his talks Robert C. Martin often emphasizes the importance of recognizing the I/O parts of your application and
the importance of differentiating your core application from its inputs and outputs from/to the outside world.
In 2012 Uncle Bob defined the concept of “clean architecture”, and this concept shares a lot of similarities with
Alister’s hexagon (or at least the things that distinct these two from the traditional layered architectures share a lot
of similarities).

Main reason why I am focusing this section only to the first one and not to the other two, is my take on the difference
in the value-add between them. 
Alistair was the first one who proposed to ditch the layers, to view your app as a core surrounded by I/O and to
segregate tech from your domain.
Jeffrey and Uncle Bob added further decompositions of the domain model on top of that.
The reason I like hexagon’s simplicity is exactly the fact that there is nothing telling you how to structure your
domain.

What matters is the shift in perspective from layers to the in & out.
This is where the bulk of the value lies in my view.

(image)

Join me in the next lecture where we will get our hands dirty and build our first hexagon.