# fp-course-notebooks

A "reformulation" of the [Data61 FP Course](https://github.com/data61/fp-course)
as [Jupyter notebooks](https://github.com/jupyter/jupyter), using the
[IHaskell kernel/backend](https://github.com/gibiansky/IHaskell).

I wrote these when taking people through the course recently.

## Caveat Emptor

Whether or not this delivery of the Data61 FP course is more effective for you,
please be aware that the [original course](https://github.com/data61/fp-course)
is maintained by:

- *More* people
- People who are *more* familiar with delivering the course
- People who have delivered the course to a *larger* more diverse sample of sample of people

In other words:

- Your mileage may vary, and they have taken this trip with a wider variety of people.
- Their version will be kept more up-to-date. I doubt I will have the time to keep this
  version in sync with theirs.

Also:

- This is an experiment and a Work In Progress, the coverage of the FP course may not be
  complete.

## Motivation

The Data61 FP course has been around for along time now, with experienced
code authors and teachers continually refining the course and iterating on the
experience.

There's a wealth of testimony that the course and its delivery is really effective on a
really large demographic, so the intention here is not to interfere with their work.

The notebooks here are an attempt to repackage the content for the small samples
of people that I was taking through this course recently.

The feedback that I got back while going through the course, and observations
I made that were providing distractions or noise to the people going through the
course included:

- Too much noise in the project, there are Nix, vagrant and cabal build files
  in the project, and this was a little too distracting in terms of focussing
  on the initial things like "I want to write a function that adds two things
  together, where can I play around?".
    - The differences in syntax between the REPL and what you write in code
      were different enough to cause confusion (`let x = foo`, and `x <- foo`
      being top-level things in the REPL while not so in code was too
      much in the initial bombardment of things).
- Editor/IDE issues.
    - Some people really needed an environment in which they were comfortable
      setup, with a minimal set of features, but it was hard finding one
      everybody was fluent in (`vim` definitely didn't work),
      and asking people to set it up themselves is a bridge too far.
- The "try and verify" iterative loop wasn't tight enough.
    - There's a lot of context
      switching between the coding environment and the repl/test window to run code through
    - When they did run the tests, there's too much noise from other tests for exercises
      they aren't focussing on. There are instructions in the course repo to at least
      limit these to a group of tests concerning a specific module, but people
      wanted to just look at a particular exercise.
    - It would have been better if the exercise, the tests for the exercise,
      and the result of running the tests for the exercise were more localised.

## Requirements

- Docker

## Getting Started

### (Optional) Try Haskell

Running through the interactive tutorial [here](https://www.tryhaskell.org)
can't really hurt much, it will give you more exposure to the syntax, which is
probably always good, but is not strictly required.

### Running the server

The following instructions will start the jupyter server running
on port `8888`.

#### Mac OS X and Linux

``` shell
# From the root of the project
bin/start-server
```

#### Windows

From the root of the project:

``` shell
start-server.bat
```

### Point your browser to it

[Here](http://localhost:8888).
