---
layout: post
title: "Unkoalified OSCP Guide"
tagline: Study Methods
date: 2019-12-02 19:30
categories: [Certification]
tags: [OSCP, Certification, Tools, Tips]
image: oscp-koalifications.jpg
---

**UPDATE: I have since learned you have to do some lab time before attempting an exam. Get the shortest amount and do what's suggested here.** 

Offensive Security says "Try Harder!" I say "Try Google!". 

Up front I don't think you need to pay for any more than the minimum lab time to pass the exam. 

I'm going to recommend you pay for a few things but they will be cheaper that paying for even the shortest lab time. As a disclaimer I receive no payment from any of the recommendations it's just what I personnally use. 

Hopefully you'll find this blog post short and helpful so let's get into it.
<p>&nbsp;</p>
## My Background
<p>&nbsp;</p>
When I first started I had no background in pentesting. What I had done was maybe three of the **easy** hack the box machines. 
<p>&nbsp;</p>
## Tools you'll need
<p>&nbsp;</p>
Something to run your virtual machine. I use [VMWare Workstation Pro](https://www.vmware.com/au/products/workstation-pro.html), I paid for this license because I use it for work as well. If you're going to keep doing stuff like this then I think it's a good investment if you just want to try it OSCP out then use [VMWare Player](https://www.vmware.com/au/products/workstation-player/workstation-player-evaluation.html) which will do the same thing but it's free.

The latest stable [Kali Linux 64-Bit](https://www.kali.org/downloads/). If you did purchase the PWK course it will recommend to use theirs but it is riddled with problems and you only need it for one course exercise. 

At this point I can't even remember how I started learning about VMWare but I'm sure you can Try Google!

Once it's installed there are a few key tools in Kali that I used all the time:

**Cherry Tree** - This should be installed by default and I will show you how I took notes later.

**tmux** - An easy to use terminal, `sudo apt-get install tmux`. Ham Vocke has a good blog [here](https://www.hamvocke.com/blog/a-    quick-and-easy-guide-to-tmux/).

**xclip** - Allows the user to `cat` a file and pipe it to `xclip -sel c` which puts the contents onto your clipboard. Install with `sudo apt-get install xclip`.

**nmapautomator** - The enumeration tool I use for HTB and all of the exam machines. The user 21y4d created the tool to use during their OSCP exam, check it out [here](https://github.com/21y4d/nmapAutomator).
<p>&nbsp;</p>
## What to study
<p>&nbsp;</p>
These suggestions are somewhat in order.

I had no idea what to do in Linux and the tricks in the command line. Over The Wire's [Bandit](https://overthewire.org/wargames/bandit/) is awesome and it's free!

[Hack The Box](https://www.hackthebox.eu/)... goes without saying. **Buy a VIP subscription!** This will allow you to do the retired boxes. Then do the following:

Complete the boxes compiled by tjnull which can be found [here](https://docs.google.com/spreadsheets/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/edit#gid=1839402159). If you want to read the blog post look [here](https://www.netsecfocus.com/oscp/2019/03/29/The_Journey_to_Try_Harder-_TJNulls_Preparation_Guide_for_PWK_OSCP.html#capture-the-flag-competitions-ctfscyber-competitions). 

Try the boxes in order (kind of a difficulty rating) when you get stuck watch how [IPPSEC](https://www.youtube.com/channel/UCa6eh7gCkpPo5XXUDfygQQA) does it and then continue on by yourself. 

On each machine take notes in Cherry Tree. I used a template like the image below and then stored extra information about the machine like nmap scans or ssh keys in sub nodes. This was a suggestion from my friend [Apr4h](https://github.com/Apr4h), make sure to check out their work. 
<p>&nbsp;</p>
![process image](https://cybercodebear.github.io/images/blog/oscp-process.png)

The buffer overflow box is just a skill you learn. justinsteven wrote a great tutorial called [dostackbufferoverflowgood](https://github.com/justinsteven/dostackbufferoverflowgood). Make sure you do them and don't just read the PDF. You'll need a Windows VM networked in VMWare to exploit some of the examples. 
<p>&nbsp;</p>
## What to read
<p>&nbsp;</p>
Google "how to pass OSCP" and read as many blogs as you can, they will all give you references. Save references as bookmarks if you find them useful. 

Save the exploits you use in HTB and document how you used them so you can replicate it during the exam if you need to. 

Your own documentation will be invaluable. 
<p>&nbsp;</p>
## Exam tips
<p>&nbsp;</p>
Eat good food.

Take breaks.

Have a good nights sleep before and during the exam.

Have a doggo keep you company.
<p>&nbsp;</p>
![moo burrito image](https://cybercodebear.github.io/images/blog/oscp-moo_burrito2.png)

During my first attempt I spent way too long on the buffer overflow machine but in the end I think the binary on the test machine was different from the victim machine.

To prepare for my second attempt I pretty much followed the advice I'm giving here and got the buffer overflow in under 2 hours. Then I got both 20pt machines, and the 10pt machine. All of these I got root on in less then 12 hours and then had a good sleep and spent the rest of the time trying to get the 25pt machine.

Getting your exam ticket and booking a good time for yourself is key. I started around 7am both times so I was fresh from a good nights sleep. 

There are 5 exam machines:

25pts = buffer overflow (follow the process, pretty easy)

25pts = hard machine (multiple vulnerbilities strung together)

20pts = med machine (pretty easily found open source)

20pts = med machine (pretty easily found open source)

10pts = easy machine (should be obvious single step)
<p>&nbsp;</p>
## Report 
<p>&nbsp;</p>
whoisflynn passed their exam with an updated template. I found it easy to use, check it out on [whoisflynn's github page](https://github.com/whoisflynn/OSCP-Exam-Report-Template)
<p>&nbsp;</p>
## Conclusion 
<p>&nbsp;</p>
So what's the final cost?

HTB VIP membership

Minimum OSCP lab time + exam ticket

Time. 

I achieved my goal of completing what I've just listed above before doing my exam and I passed (the second time). 

Don't be afriad of failing the first time either. You'll gain valuable experience and figure out your weaknesses. Plus it's much cheaper than purchasing the labs.
