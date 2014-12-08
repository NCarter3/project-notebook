# Design notebook for week ending December 7, 2014

## Description

This week I worked on getting human readable dates to work as inputs. I
used a python package to convert the dates. Currently, the program
reformats the dates to be absolute and unambiguous when the user
saves the file. This is not necessarily ideal, but it seems like 
a good first pass. If you have better ideas, let me know!

I also added a snippet syntax for entering new tasks. The system
now supports typing `alt+a` to add a task. The task is added in the 
form of a snippet with a hashtag already generated and the ability to
tab through fields. 

I though about how I am going to add done support too. I did some 
experimentation about how to implement it but didn't get very far
yet.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation? What questions do you have 
for your critique partners? How can they best help
you?**

We need to think about how to surface error, when, where, and how aggressively. 
Obviously, this type of tool needs to be trusted. So, we need to make sure
that when an error happens that it is recognized. However, as we are working
with human inputs, there may be times that things do get misinterpreted or
fail. Where and how should this information be surfaced?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

6 hours, 11:30 - 1:30 and 2:30 - 6:30 12/6, adding features

2 hours, 12/7, thinking about how to add done support, notebook, team interfacing


## Post-critique summary and reflection
I think we won't be changing our syntax to be more verbose. It's also good advice
not to put that much time into fluffing out the rough edges in the parser anymore.
Regarding done tasks, the concern with marking them in the input file is what if
the task repeats? Then how would you know which instance of the task is done?
I think for the moment we will handle done tasks in the output file, but we may
redo this at some point in the future if we come up with a better way.



## Post-critique summary and reflection for some past week that I unwittingly put in the wrong file
As a result of this critique and discussions last Wednesday, we decided that it would be best to combine
teams and work on this project together. So, Michael, Christine, and I are now one team. This critique 
also made us reevaluate what would work well for the language base. After further reflection, we decided not 
to use Todo.txt as a base and instead to start from scratch.

We are also looking at elucidating what an IR will look like for this language. There are definitely complexities
here that we did not fully understand when proposing the language. We are working on how to address these.
