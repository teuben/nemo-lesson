---
title: "Installing NEMO"
teaching: 5
exercises: 10
questions:
- "How do I install NEMO (can be skipped)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---


## Installing from github

The simplest will be
~~~
$ git clone https://github.com/teuben/nemo
$ cd nemo
$ ./configure
~~~
{: .language-bash}

~~~
lots of output. This will take less than a minute.
~~~
{: .output}

followed by the unusual

~~~
$ make build
~~~
{: .language-bash}


~~~
lots of output. This will take a few minutes.
~~~
{: .output}


## Loading NEMO

NEMO is now ready to be loaded in the shell, as we discussed before:

~~~
$ source nemo_start.sh
~~~
{: .language-bash}





## Checking

A regression test is useful to see if some important tools are working correctly

~~~
$ make check
~~~
{: .language-bash}


~~~
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/image/fits
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/image/io
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/image/misc
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/image/rotcur
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/image/trans
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/image/wcs
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/kernel/fortran
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/kernel/io
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/kernel/misc
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/kernel/tab
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/cores
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/aarseth/nbody0
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/aarseth/tools
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/dehnen
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/directcode
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/flowcode
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/hackcode/hackcode1
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/hackcode/treecode1
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/scfm
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/evolve/sellwood/tools
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/image
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/init
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/io
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/io/starlab
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/io_nemo
TESTSUITE: FAIL /home/teuben/NEMO/nemo/src/nbody/reduc
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/trans
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/nbody/xyz
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/orbit/misc
TESTSUITE: OK   /home/teuben/NEMO/nemo/src/orbit/potential
TESTSUITE: OK   /home/teuben/NEMO/nemo/usr/wolfire
Results in /home/teuben/NEMO/nemo/tmp/test23706/testsuite.log
A copy in /home/teuben/NEMO/nemo/testsuite.log is kept as well as the latest.
BSF regression results that failed:
BSF: FAIL   0 0 0 0 0 bench.dat
BSF: EXPECT 0.00196205 0.391904 -1.22753 2 10469 bench.dat
BSF regressions that are not OK: 1

~~~
{: .output}

in this example there was a failure.. The file **testsuite.log** will
need to be consulted to see what the failure was.

## Benchmark

To get an idea how fast your computing platform is, we have devices the **NEMOBENCH5** benchmark

~~~
$ make bench5
~~~
{: .language-bash}


~~~
CPU_USAGE  directcode  :  4.66  4.65  0.00  0.00  0.00  1718721840
CPU_USAGE  gyrfalcON   :  4.91  4.91  0.00  0.00  0.00  1718722307
CPU_USAGE  hackcode1   :  4.93  4.92  0.00  0.00  0.00  1718722799
CPU_USAGE  orbint      :  4.74  4.74  0.00  0.00  0.00  1718723292
CPU_USAGE  potcode     :  4.67  4.65  0.01  0.00  0.00  1718723767
CPU_USAGE  treecode1   :  4.61  4.61  0.00  0.00  0.00  1718724234
NEMOBENCH5 score:   1051.89
{: .output}

On this particular machine a score of **1052** was obtained. Larger values
are better. This **NEMOBENCH5** was modeled after the idea of
**geekbench5**, in our case each of the codes was tuned such that it
would take 5sec CPU on a i5-1135G7 intel CPU, to which the NEMOBENCH5 value
was normalized to 1000.

{% include links.md %}

