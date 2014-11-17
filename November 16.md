# Design notebook for week ending November 16, 2014

## Description

This week we formalized what we want to accomplish in our first week by defining what the
AST will look like for our first prototype. With this in hand, we are comfortable 
procdeeding to the next phase of the project -- writing a prototype. We recieved some excellent
feedback from the design consultants that came to class last week. They helped us sort out
some design questions we had been nagging at. In the week before, we had been trying to make
our IR as robust and flexible as possible. 

However, after talking with the designers, we realized
that we were really making it more flexible than necessary for our application. We had been thinking
as engineers. We were trying to imagine every possible use case for our language and every 
possible way it could be extended. However, the designers pointed out that our core use
case is recurrances similar to daily chores or homeworks. This realization allowed us to 
significantly scale back the first pass featureset of our language. The similifications
that this allowed will make it much easier for us to get a clean, quick prototype built.

Since we have made these decisions, we have begun the process of implementation. 
We are still planning on using a Sublime plugin as the IDE for our language. As a result,
we have been learning the tools that will enable us to do this. In particular, we have been
examining the Sublime API and various python packages for doing things related to parsing,
ASTs and semantics. We had hoped to use a library called [MacroPy](https://github.com/lihaoyi/macropy) in order 
write case classes in python, however after a lot of experimentation we realized that this library is 
both overkill and overly complicated for what we need to be able to do. At this point, we think we will
use a normal python class heirarchy to describe our IR, while keeping open to the possiblity of using
pre-written or our own function decorators to make things easier. For parsing, we are looking 
at the [PyParsing](http://pyparsing.wikispaces.com/) library which appears to be light weight but
powerful enough for our purposes.

[Here is a link to our IR for our prototype.](https://github.com/mculhane/project/blob/master/pete/intermediate_representation.py)

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Currently are most pressing issue is simply learning about the tools we have chosen and 
starting to use them. Our next week is going to be working on a prototype. So, I think
we are going to keep our design mostly as-is for this week and see how a prototype goes,
then look back on our decisions and see what we want to change.

**What questions do you have for your critique partners? How can they best help
you?**

We are still mostly getting started on this project. We think our AST spec is fairly solid now for 
a first pass. However, if you notice anything terrible we would love to hear it. In terms of future plans,
as I said, we are planning on using almost exclusively python for this project. However, we are also
early enough in the projct that if you convincingly argued that that is a bad decision, we would likely listen to you.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

* 3 hours -- 11/13 meeting with team starting design review document. Together we completed a first pass. 
* 2 hours -- 11/15 meeting with team continuing and finishing design review. I also started researching and learning about Sublime plugins and how to write them.  
* 2 hours -- 11/16 meeting with team working on getting started on code. Still trying to get a feel of the Sublime API. I also worked on finding some python libraries that might come in handy.
* 1 hour -- 11/16 working on this document.

Total: about 8 hours outside of class.

## Post-critique summary

## Post-critique reflection
