---
layout: default
title: Why Machine Init?! 
date: 2018-12-9
permalink: 
---
<figure class="center">
<a href="/images/mrrobot.jpg"><img alt="Mr. Robot" src="/images/mrrobot.jpg" style="width:600px;height;200px;"></a>
<figcaption>Image by <a href="https://www.bleedingcool.com/2018/08/29/mrrobot-usa-season-4-series-finale/"><strong>Bleeding Cool</strong></a></figcaption>
</figure>

My thoughts for the title of this blog, really spawned from a few sources of inspiration. First, as you may likely already have noticed, I really find a connection to Marvel's fictional character named Tony Stark, a genius, billionaire, philanthropist who became the armored superhero known as Iron Man. His "always tinkering" mentality lead me to begin tinkering on my own too; however, not only with simple electronics, like the [Raspberry Pi][1], but also with complex ideas and processes, including information security, secure programming, and network and server infrastructure automation. 

In many scenes, Tony Stark/Iron Man is seen constantly working, like a machine that's constantly running. It as though he runs on batteries...wait...he technically does run on batteries, or rather a single, mini arc reactor embedded in his chest. Perhaps that is why I was inspired, because I am constantly trying to learn new things and constantly working on expnanding my skillset...like a machine, iterating through new data inputs. Hmmm...*Machine Learning*...sounds like a good topic for a future post.

<figure class="center">
<a href="images/arcreactor.png"><img alt="Arc Reactor" src="/images/arcreactor.png" style="width:75%;height;50%;"></a>
<figcaption>Image by <a href="http://marvelcinematicuniverse.wikia.com/wiki/File:Proof_that_Tony_Stark_has_a_Heart.png"><strong>Marvel Cinematic Universe Wiki</strong></a></figcaption>
</figure>

Anyways, another source of inspiration came from USA Network's show called ***Mr. Robot***. In this show, a cybersecurity engineer demonstrates his persistence and knack for finding out how something works...or in many cases how it shouldn't work. He dissects problems, in processes, technology and people and learns to implement ways of bypassing their functions to discover another layer of information. In other words, he's "*bug-hunting*", finding ways in which someone, or something works or doesn't work by utilizing tools and techniques to explore more complex topics. In particular, there have been a few episodes that show the character utilizing **[Raspberry Pis][1]**, **[USB Rubber Duckies][2]**, **[femtocells][3]**, bluetooth signal sniffers, **[steganography][4]**, python scripts, **[Putty][5]**, **[ProtonMail][6]**, **[Elasticsearch][7]**, and **[Kali Linux][8]** to showcase the skills of a cybersecurity engineer or even to give a simple depiction of the white hat hacker mentality.

In one episode of Mr. Robot, the protagonist explains the topic of system runlevels. In very simple terms, a runlevel is one of the modes that a Unix-based operating system will run in. A runlevel is, for lack of a better term, a phase of the systems operation. At each of these phases certain processes are stopped or initialized (this is where ***Init*** comes from). When a linux system is restarted, or commonly referred to as rebooted, a program called ***init*** reads a set of instructions to determine what processes should run during a specified phase. Typically, the default phase is for a system to start normally. Below is a quick snapshot of the seven different runlevels, numbered from 0 to 6:


|  **Runlevel** |             **Mode**            |                                   **Action**                                   |
|:-------------:|:-------------------------------:|:------------------------------------------------------------------------------:|
|       0       |               Halt              |                                Shuts down system                               |
|       1       |         Single-User Mode        | Does not configure network interfaces, start daemons, or allow non-root logins |
|       2       |         Multi-User Mode         |             Does not configure network interfaces or start daemons.            |
|       3       | Multi-User Mode with Networking |                           Starts the system normally.                          |
|       4       |            Undefined            |                             Not used/User-definable                            |
|       5       |               X11               |                       As runlevel 3 + display manager(X)                       |
|       6       |              Reboot             |                               Reboots the system                               |
{:.mbtablestyle}

Source: [Linux Runlevels Explained][1]


Yet another source of inspiration came from the movie ***[Ghost in the Shell][9]***, mainly because the movie features many references to advances in technology and a prevalent theme of system security and data security throughout the movie. But also for the reason that the protagonist is, in essence, a conscious, human mind, embedded in a cybernetic body. However, this amalgamation of a the human mind and machines seems quite relateable to most of us today. We've come to have a persistent connection to our computing devices. Some users even having, what seems to be a second persona in the cyber-world, masking themselves from within the physical world. The title ***[Ghost in the Shell][9]***, somewhat represents how I connect with the computing device from within the command line terminal, commonly known to others in the IT profession as the shell.
 
Simply put, ***Machine Init*** is just me navigating the shell, including the exploration of my operating system's programs, navigating the linux file system, writting bash and python scripts to automate tasks, writing blog posts in Markdown using the Vim text editor, exploring data science topics and hardware/software integration projects.

[1]: https://www.liquidweb.com/kb/linux-runlevels-explained/
[2]: https://latesthackingnews.com/2017/06/16/20456/
[3]: https://www.techrepublic.com/blog/data-center/pros-and-cons-of-using-femtocells/
[4]: https://www.wired.com/story/steganography-hacker-lexicon/
[5]: https://unix.stackexchange.com/questions/375095/whats-the-difference-between-putty-and-ssh
[6]: https://protonmail.com/
[7]: https://dzone.com/articles/what-is-elasticsearch-and-how-it-can-be-useful
[8]: https://www.kali.org/about-us/
[9]: https://www.imdb.com/title/tt1219827/
