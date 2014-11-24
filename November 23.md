# Design notebook for week ending November 23, 2014

## Description

This week we mostly did development work. We mostly froze our design and just
focused on getting a first pass working so that we can user test it
tomorrow, Monday. We did make at least one change. We changed our syntax to look like:

`#aaa This is a task @ start datetime - end datetime % repetition expression`

`start datetime`, `end datetime`, and `repetition expression` are all optional.
We are actually really happy with this syntax. It seems like a really clean and
efficient expression for what is necessary to define events. One small tweak we will
need to make is related to the `-` control character. In particular, it can be
ambiguous or at least very difficult to parse at the moment (consider `2014-3-5-2014-6-7`). 
We have been trying to decide how to fix this. We have considered requiring 
spaces around the dash (like `2014-3-5 - 2014-5-6`) or requiring a double dash
(like `2014-3-5--2014-6-7`). What do you think? Do you have other ideas?

In terms of what we have accomplished, our UI is looking pretty good, or 
at least I think so. (Full disclosure: it has been my job this past week,
to I may be a touch biased.) I've been impressed with what one can do with 
Sublime. I have also been surprised by how hard it is to do certain things, 
but overall my experience with plug-in development has been positive thus far.

[Here is an image of where we are so far.](https://www.dropbox.com/s/d0pa0novbfeqpkc/prototype.png?dl=0)

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation? What questions do you 
have for your critique partners? How can they best help
you?**

What do you think of the input bar at the bottom versus some more free-form text
entry method? The system currently supports a user directly editing the file in
the top window, but I am not sure which entry method to encourage. There is the ease 
of entry when entering via the prompt, and this method makes it easier to process
the text on entry (such as converting relative expressions to exact expressions.)
However, there are some cool things one can do with text with a Sublime plugin when
editing a file directly. In particular, one can provider auto-complete help and
syntax help in a file buffer window. As far as I know, this is not possible using 
the prompt. What do you think of this? Which should we go for, or should we continue 
using both?

What are the top features you would like to see next in the UI? We have a lot of ideas 
about where we would like to go with this, but we don't really have any idea
about how to rank their importance. Some ideas are:
* auto-complete help (esp. for hashes if you are referencing some other task)
* snippets that would allow you to tab through fields to fill out a new task
* automatic inserting of hashes for new tasks
* automatic conversion of relative expressions to unambiguous expressions
* syntax error identification and help (I don't know what would be useful to support for this. Suggestions welcome.)
* Integration/syntax support for some other task markup language like Todo.txt (this is already supported in a sense -- one can mark up the task in that language and our parser will only pay attention to what is after the `@` symbol, but we could make this more useful through syntax highlighting and being careful that the file we output is validly formatted as Todo.txt.)

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

11/18 3 hours. Worked on Sublime UI framework

11/18 1 hours. Worked on Critique for Phil

11/20 2.5 hours. Working on Sublime UI, specifically on getting a syntax definition

11/21 0.5 hours. Continuing refinement of UI.

11/22 3.0 hours. Continuing to work on UI. Fixed some bugs!

11/23 2.5 hours. Group meeting, worked on hooking things together for demo. Wrote basic main object for interpreter.

11/23 1 hours. Worked on journal.

## Post-critique summary

## Post-critique reflection
