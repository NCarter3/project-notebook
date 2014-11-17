# Design notebook for week ending November 9, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

We are currently working on really pinning down what this language is going
to look and feel like. My job has been creating a first pass of the IR. You
should find it on the [wiki](https://github.com/mculhane/project/wiki). 
I did mostly worked on how due dates would be
calculated, but Michael and I met this morning and we realized that we also
wanted to consider start dates, which adds more complexity to the language.

We are also trying to address the trade-off between more expressiveness and
more syntax. The lighter the better, but too light and we will not be
able to do the date calculations that we want to.

We think that Sublime will be a good platform for a demo of our language.
We should be able to use it to automate a lot of whatever input syntax we choose,
do live computations, and substitute out relative terms for exact. This last
part is going to be important as we will want to be able to say things like
"tomorrow" and we need our program to be parsed and calculated, and tomorrow
substituted for a real date, before the date changes and we think that tomorrow
is the wrong day.

We also thought more about recurrences and decided that the best way to store
them will be something like a hashtable. We will identify tasks by a name or
hash and let users reference them by the hash. Then, in a parse tree, when
we find recursive relationship, we can follow it in the hash table.

Clearly, we will have to deal with cycles, but I think we can do this 
computationally. If that proves difficult, it also seems reasonable to
simply consider this a invalid input and handle it fairly gracefully.



## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

We need to make a list of the things we plan to implement from the get-go
and the things that will be stretch goals. This will allow us, in continuing
to refine the IR and syntax, to make choices that are efficient in the short
term and also will scale well in the long term.

**What questions do you have for your critique partners? How can they best help
you?**

Take a look at the beginnings of the IR that I am putting in the wiki. It
is not complete yet and has some contradictions in it (I keep changing things
around), but it should give you a sense of where I think we might be going.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

This week I worked on the IR, Michael worked on exploring the feasibility of a Sublime
plugin as a platform, and Christine worked on a syntax. We will be seeing how
each of our tasks went and what needs to change in the next week to bring 
how everyone is conceptualizing the language in line.

I probably spent 5 hours outside of class this week.

## Post-critique summary and reflection

Michael highlighted some key issues in his critique of our project last week. At that point, 
as I said before, had been struggling heavily on how to appropriately represent the syntax and IR
while taking into account both easy of use and feature completeness. In the last week, as Micheal 
mentions in the feedback and as I mention in this week's notebook, I think we have made significant
progress on this.

In response to Phil's comments, I think he makes a good point about performance -- that we shouldn't
really need to care -- but I am not sure if I agree with his assessment of the syntax and IR. He 
does raise a good point that at the IR level we sould have already converted everything to one unit.
However, there could actually be some functional challenges with this as we may want to treat, for example, a daily
task differntly from one that has a specific due time. However, their are likely ways around this. 

Regarding his comment about flexibility, the power of the language comes about when considering how to 
specify relational times. That is what we are trying to accomplish. If we can get the required syntax 
to indicate where the task stops and the time starts down to one character, we will. However, this character
is necessary to disabiguate the task from the date statement. 

Phil is also correct in noticing that currently the syntax and the IR are closely related. We have not spent 
a long time thinking about how to specify the syntax briefly, so it makes sense that the "logical" representation
of the language currently closely mirrors the syntax. This may or may not change as we go.


