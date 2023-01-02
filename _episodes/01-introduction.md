---
title: "Introducing NEMO"
teaching: 5
exercises: 0
questions:
- "What is NEMO and how would I use it"
objectives:
- "Introducing NEMO"
keypoints:
- "Stellar Dynamics"
- "the N-body problem"
- "NEMO"
---
### Background

As soon as computers became available to the research community in the 50s, astronomers
tackled the problem how to compute the orbits of stars and planets 
under their common force of gravity: the N-body problem.

The first programs were written in FORTRAN (von Hoerner, Aarseth, van Albada and many others),
and we have some of those available to experiment with in NEMO!

### NEMO

NEMO is a software environment to enable you to do Stellar Dynamics in general and the N-body problem
in particular. It has several hundred programs to initialize stellar N-body systems, integrate them
in time, study their orbits, convert them to images and compare them to observations etc.etc.

You will be writing scripts to orchestrate a simulation and their analysis. We have examples
in csh, bash and python.

NEMO has excellent programs to import data from other codes, as well as export data such that
other codes can process that data. We also employ tables in text or CSV format.

NEMO has a good infrastructure to write new programs.

Although NEMO is no acronym (it's antology is from an attempt to pun nbody to nobody, which
became NEMO in latin), a good friend could not help himself and dub it *Not Everyone Must Observe* !

{% include links.md %}

