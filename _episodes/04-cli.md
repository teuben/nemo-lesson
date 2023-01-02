---
title: "NEMO's command line interface (CLI)"
teaching: 5
exercises: 10
questions:
- "How do I use NEMO from the command line"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---


Any NEMO command can be run from the command line. Here is the **tsf** (*"type structured file"*) program,
which would display the contents of NEMO's binary files in some human readable way

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

but

~~~
$ tsf --help
~~~
{: .language-bash}

give

~~~
tsf in=??? maxprec=false maxline=4 allline=false indent=2 margin=72 item= xml=f octal=f VERSION=3.3c
~~~
{: .output}

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





{% include links.md %}

