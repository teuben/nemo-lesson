---
title: "NEMO's command line interface (CLI)"
teaching: 5
exercises: 5
questions:
- "How do I use NEMO from the command line"
objectives:
- "Learning NEMO command line interface"
keypoints:
- "Run a NEMO command"
- "Get help from a NEMO command"
---


Any NEMO command can be run from the command line. Here is the **tsf** (*"type structured file"*) program,
which would display the contents of NEMO's binary files in some human readable way. So lets try issuing
the command

~~~
$ tsf 
~~~
{: .language-bash}

~~~
Insufficient parameters, try 'help=', 'help=?' or 'help=h' or 'man tsf',
Formatted man page might also be here: https://teuben.github.io/nemo/man_html/tsf.1.html
Usage: tsf in=??? ...
type contents of a (binary) structured file
~~~
{: .output}

so obviously it needs some arguments. And there some reminders on how and where to get more help:

~~~
$ tsf --help
~~~
{: .language-bash}

give

~~~
tsf in=??? maxprec=false maxline=4 allline=false indent=2 margin=72 item= xml=f octal=f VERSION=3.3c
~~~
{: .output}

Your output might be a little different from the version when this manual was written.

> ## Getting More Help
>
> More help can also be obtained via the **help=** option. Try for yourself the **help=h** and
> **help=M** options for the **tsf** program.
>
> The **help=?** gives help what help options exist. If your shell gets confused by the question
> mark, try **help=\?**
>
> > ## Solution
> > The **help=h** will give you a line by line summary of the keyword, some one-line help
> > and the default in square brackets:
> >
> >          margin           : righthand margin  [72]
> >          in               : input file name  [???]
> >          maxprec          : print nums with max precision  [false]
> >          maxline          : max lines per item  [4]
> >          allline          : print all lines (overrides maxline)  [false]
> >          indent           : indentation of compound items  [2]
> >          margin           : righthand margin  [72]
> >          item             : Select specific item []
> >          xml              : output data in XML format? (experimental) [f]
> >          octal            : Force integer output in octal again? [f]
> >          VERSION          : 3-feb-2014 PJT  [3.3c]
> >
> > The **help=M** will give you a classic unix *man page*
> >
> >         TSF(1NEMO)
> > 
> >         NAME
> >              tsf - type a structured file
> > 
> >         SYNOPSIS
> >              tsf in=file [parameter=value] ...
> > 
> >         DESCRIPTION
> >              tsf types  the contents of a structured binary file ...
> >
> {: .solution}
{: .challenge}

Such a *Unix manual page* - short of reading the source code - will have the most information,
including examples, and sometimes a TLDR section.

> ## Source Code?
>
>  Ultimately the best documentation can be the source code. In the remainder of this episode
>  you will discover how to easily find and look at the source code
>
{: .callout}


> ## mknemo
>
> The **mknemo** command will help in updating NEMO when new code is available
>
>       mknemo tsf
>
> will not only compile a new version of the **tsf** program, but also show where the
> source code lives. Have a look at the source code with your favorite Unix command or editor.
>
> > ## Solution
> >
> >       MKNEMO> Searching tsf.c: 
> >       found one: /home/teuben/NEMO/nemo/src/kernel/io/tsf.c
> >       gcc -g -O2 -D_FILE_OFFSET_BITS=64 -D_LARGEFILE_SOURCE -D_LARGEFILE64_SOURCE  -fpic -rdynamic  -Dlinux -DSYSV  -I/home/teuben/NEMO/nemo/inc -I/home/teuben/NEMO/nemo/lib -I/home/teuben/NEMO/nemo/opt/include -I/usr/include/hdf   -Wall -Wimplicit-function-declaration  -D_GNU_SOURCE -std=c99  -o tsf tsf.c -L/home/teuben/NEMO/nemo/lib -L/home/teuben/NEMO/nemo/opt/lib          -lnemo -ldl  -lreadline -lhistory -lncurses `pkg-config --libs cfitsio` -lm   -L/usr/lib/gcc/x86_64-linux-gnu/11 -L/usr/lib/gcc/x86_64-linux-gnu/11/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/11/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/11/../../.. -lgfortran -lm -lquadmath 
> >
> >
> > On the 2nd line you will see the filename, so in my case I can do
> > 
> >        more /home/teuben/NEMO/nemo/src/kernel/io/tsf.c
> >
> {: .solution}
{: .challenge}





{% include links.md %}

