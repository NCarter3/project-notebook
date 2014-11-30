# Design notebook for week ending November 30, 2014

## Description

Due to break, not too much happened this week. We had our design review in class. Some time was
spent getting ready for that. We do now have something that does something, which is
kind of awesome. The other thing we worked on was our evaluation.

Our next steps will be to improve user interaction with the program. At the front end,
this means changing relative statements to exact statements (e.g. tomorrow -> Jan 5, 2014). 
On the back end, this means improving the flexibility of our parser and semantics, and
adding the recurrence and dependency calculation that is now lacking. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

We don't know at the moment what to do with completed tasks. We hadn't even
considered that we need to handle them until our design review. One idea 
I have is to add a `done.txt` file and (much like the language `Todo.txt`)
have completed tasks be prefaced by an `x` and be moved from the output of
our language to the `done.txt` file. This, however, adds a number of complications
as it requires us to do computations on the output of our interpreter and
to remember changes to the output in the future. Another option would be to have
some form of annotation to the input file. This might be more easily accomplished, 
but I don't know what it would look like. What do you think? Any other potential
ideas?

**What questions do you have for your critique partners? How can they best help
you?**

Other than the above question, also take a look at our evaluation document and 
see what you think about the feedback during the review day that we received.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

11/24 2.5 hours. Connecting the scala component to the python part. This took way to long.

11/30 1.5 hours. Working on evaluation document. Working on weekly journal.

## Post-critique summary and reflection


