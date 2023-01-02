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




{% include links.md %}

