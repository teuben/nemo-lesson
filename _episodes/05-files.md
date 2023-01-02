---
title: "Files and Pipes"
teaching: 5
exercises: 5
questions:
- "What kind of files does NEMO use"
objectives:
- "Files"
- "Unix Pipes"
keypoints:
- "Files"
- "Unix pipes"
---


NEMO stores most of its data in binary format.  We have already see that the **tsf** program can
display such data

~~~
$ mkplummer out=p10.dat nbody=10 seed=123
$ tsf in=p10.dat
~~~
{: .language-bash}

but since the first two keywords are in order, it's much easier to skip the *keyword=* portion for
those. The seed= keyword is much further down the list, so we explicitly pass it with the keyword
name:

~~~
$ mkplummer p10.dat 10 seed=123
$ tsf p10.dat
~~~
{: .language-bash}


~~~
char Headline[28] "init_xrandom: seed used 123"
char History[43] "mkplummer p10.dat 10 seed=123 VERSION=3.0b"
set SnapShot
  set Parameters
    int Nobj 10 
    double Time 0.00000 
  tes
  set Particles
    int CoordSystem 66306 
    double Mass[10] 0.100000 0.100000 0.100000 0.100000 0.100000 
      0.100000 0.100000 0.100000 0.100000 0.100000 
    double PhaseSpace[10][2][3] -0.609486 -0.221687 -0.450963 
      -0.0766784 -0.209397 0.396561 4.80925 -0.486182 -1.52575 
      0.418474 0.117766 0.230193 0.545314 0.0795464 0.0632245 
      0.0867019 -0.109128 -0.282036 0.377209 -0.213318 -0.0118330 
      . . .
  tes
tes
~~~
{: .output}

but we can also use this in a Unix pipe 

~~~
$ mkplummer - 10 seed=123 | tsf -
~~~
{: .language-bash}

and it should give exactly the same output, since the same **seed=123** was used.



{% include links.md %}

