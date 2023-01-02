---
title: Setup
---

There are no files to setup yet. NEMO has a few small datafiles in the directory **$NEMO/data**.

### Generate your own data

In general it is easy to generate data from NEMO, here is an example
to view a 10-body Plummer sphere using **tsf**

~~~
$ mkplummer - 10 seed=123 | tsf -
~~~
{: .language-bash}

~~~
char Headline[28] "init_xrandom: seed used 123"
char History[37] "mkplummer - 10 seed=123 VERSION=3.0b"
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


{% include links.md %}
