---
title: "Loading NEMO in your Unix Shell"
teaching: 5
exercises: 5
questions:
- "How do I use NEMO in a Unix Shell"
objectives:
- "Loading NEMO interactively in your shell"
- "Ensure NEMO is present each time you start a new shell"
keypoints:
- "Getting started with NEMO"
---

In this lesson we will load NEMO into your shell environment.

### Loading NEMO

It is assumed somebody
has already installed NEMO. The only thing we need to know is the root directory where
NEMO has been installed.
So let us assume somebody told us that NEMO has been installed in
**/opt/nemo_4.1.1**  The following command would then load NEMO in your **bash** shell

~~~
$ source /opt/nemo_4.1.1/nemo_start.sh
~~~
{: .language-bash}

so really all you need is to find the location of the
**nemo_start.sh** file.  There is a similar file for the **csh**
shell, for the die-hards.

Obviously you should test if NEMO commands are now available. The **tsf** (Type Structured File) program
is the de-facto test for this.

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



> ## Making it persistent
>
> Each time your (bash) shell is loaded, it will read some startup files, in which
> you can add the before mentioned **source** command. This way each time
> you start a new shell, NEMO will be ready. For bash this should be **~/.bashrc**
> for interactive shells (interactive and login shells can give for confusing
> startup procedures).
>
> There is a potential danger to this method. Side-effects for other programs.
> Probably should say more about that.
{: .callout}




{% include links.md %}

