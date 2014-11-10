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
should find it on the (wiki)[https://github.com/mculhane/project/wiki]. I did mostly worked on how due dates would be
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

## Post-critique summary

## Post-critique reflection
