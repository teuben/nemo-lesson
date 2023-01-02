---
title: "Loading NEMO in your Unix Shell"
teaching: 5
exercises: 5
questions:
- "How do I use NEMO in a Unix Shell"
objectives:
- "Getting started with NEMO"
keypoints:
- "Loading NEMO interactively in your shell"
- "Ensure NEMO is present each time you start a new shell"
---
In this lesson we will load NEMO into your shell environment.

It is assumed somebody
has already installed NEMO. The only thing we need to know is the root directory where
NEMO has been installed.
So let us assume somebody told us that NEMO has been installed in
**/opt/nemo_4.1.1**  The following command would then load NEMO into your **bash** shell

~~~
$ source /opt/nemo_4.1.1/nemo_start.sh
~~~
{: .language-bash}

so really all you need is to find the location of the
**nemo_start.sh** file.  There is a similar file for the **csh**
shell, for the die-hards.


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

