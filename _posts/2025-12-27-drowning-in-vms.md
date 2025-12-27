---
layout: post
title: "Drowning in VMs"
date: 2025-12-27
---


Over the past week I've been figuring out the direction I wanted to take my personal projects and study. My interests have been kind of all over the place and I expect it will stay like that for a while. More out of a desire to feel like I was making progress than anything else, I spent this week setting up my environment for a few of my different interests. For me, that meant a whole lot of time spent on virtual machine setup. I'm probably getting ahead of myself but I ended up with four separate virtual machines configured, so I figured I'd spend a little time explaining what I did.

## Hypervisor choice
All these machines have to run on something, and for me that is VMWare Workstation Pro. I don't really know much about pros and cons of the different platforms, but this seems to work well enough and it's free so I can't complain.


## Kali Baby
The first VM I set up was my Kali Linux vm. I actually set this one up earlier this year when I started getting into TryHackMe CTFs, and that's pretty much exactly what I'm going to continue using it for. I'm not very good at those but I just liked having my own machine rather than trying to do it in the browser. 

The draw of Kali to me is that it just has a whole bunch of the relevant tools for these types of challenges from the start and it's an easy way to interact with them. I have very limited experience with these challenges but some of the included tools I have found useful are
- nmap
- gobuster
- burp suite

and I've just scratched the surface. This is the CTF machine.

## Malware Analysis Twins
Another topic I've been interested in is malware analysis and so I did a bit of setup for an environment for those. I haven't gone very in depth with this setup so I'm not really sure what my workflow will be but I should have a good set of tools now for learning and getting experience.

First, I setup a host-only network in VMWare to connect my two machines to. This is so any malware I run won't be able to reach the internet and is trapped in my machine. Sounds like the plan is to get malware samples from a password-protected zip file and put it into a shared file in my sandbox.

Next, I setup a REMnux VM. I have a bit of experience with some static analysis in linux so this is where I'll want to practice with that. It was a very simple install and also comes with a good suite of tools. No complaints, easy peasy.

Flare-VM was a different story.

I decided to setup a different VM for Windows malware and as a sandbox for dynamic analysis. The first step was setting up a Windows 10 VM, which was already a bit of a challenge. I had some trouble getting past the account setup and had to do some weird stuff to setup a purely local account. The bigger issue, though, was the Flare-VM install script. I had to do a bunch of weird stuff to bypass Windows Defender to get the script to run in the first place, and it still broke halfway through a few times for some reason. On my third try, it finally worked after running for three hours. Definitely not super fun but I'm glad I did it.

## Research Box
The last virtual machine I set up was simple and plain Ubuntu machine. Nothing fancy installed on it or anything, my plan for this one is to use it to roleplay as a security researcher until I eventually figure out what's going on in that sphere. I plan on working with AFL++, GDB, and trying to learn the process behind finding vulnerabilities and building exploits. This sounds really hard but it also sounds really cool so I'm gonna give it a try.

## Conclusion
So there you have it! I've got pretty much every tool I could need for the next while, and now I can start digging into some real projects. It is very likely I won't end up using all the stuff I have installed, but at least now I have a good starting point. I'll get back to you with some actual experience someday!