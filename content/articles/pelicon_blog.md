---
date: 2020-03-20 12:30:00 +0500
# modified: 2020-05-22 14:19:00 +0500
title: Creating My Blog
summary: In wanting to create a personal blog for documenting my personal work and achievements, I set out searching for an effective and efficient way of publishing a website. This entry covers the specific sites and general techniques that I ending up using.
category: Blog Creation
tags: Blog, Github, TravisCI, VSCode
author: Acea Sands
layout: post
comments: true
lang: en
---

[TOC]

![Github Icon Image]({static}../images/articles/github1600.png)

When publishing my personal blog, there were 3 main programs/websites which I used: Visual Studio Code, GitHub, and TravisCI. 

## Visual Studio Code (VSCode)

VSCode is a common abreviation for Visual Studio Code, a lightweight version of Visual Studio managed by Microsoft. The capability and versatility of this program is one of the many reasons why I use this program for nearly all of my coding needs. Currently, I am in the Masters of Data Analytics (MDATA) program at Utah State University (USU). As part of this program, I am required to learn and write code in various kinds of languages such as R, Python, and SQL. Not only does VSCode have the ability to write in all of these languages, but it also allows for connections to SQL servers. This allows me to write and run quieries directly to my assigned database without having to work in the SQL Server Management Studio (SSMS) environment. It also has a variety of extentions written directly by Microsoft and various other members of a passionate community which further increase the capability of this already fantastic program. 

For this project specifically, however, I used VSCode because of its ability to communicate and work with GitHub, a website that was instrumental in getting my site up and running.

## GitHub

Github is an online software hosting website. In more simplistic terms, think of it like Microsoft's OneDrive or Box, but slightly different. Those programs allow you to upload and store anything whereas GitHub has a focus on publicly sharing and privately storing programming code. It allows me to upload my code for public or private sharing and has implementations with various other services, such as TravisCI. It also allows the storing of version history via repositories -- essentially a stored collection of files on GitHub -- which keep track of file version history. For example, lets say I'm working on a program that i'm constantly adding new things to, like packages I've never worked with before, or just simply new code. When I change anything in my file on my computer, I can look at GitHub's version (via the extension in VSCode) and see exactly what's changed from the file in GitHub. I can then upload my changes when I'm done making them if I'm satisfied with my work. If, for some reason, the new code I added messed up my program to the point where it no longer runs, I can go to GitHub and download a previous version of my program before I made those changes. This is an envaluable tool not just for programers, but for anyone that does a lot of work on various kinds of documents on their computer.

To get started on my blog, I first copied a blog setup published by Pablo Iranzo called "Blog-o-matic". This repository had a pre-built system of getting a blog up and running. I used his system because it uses Pelican -- a python-based static site generator (it makes websites) -- which I figured would be easier to learn and work with since Python is my most comfortable language to work with. The theme it uses, which influences the general look/layout of the website was the "elegent" theme. I then moved on to the part where I publish the site. To make this process as automated as possible, I hooked up my GitHub Token (GHToken) to TravisCI

## TravisCI

To make this process as automated as possible, I hooked up my GitHub Token (GHToken) to TravisCI. This website essentially provides Virtual Machines (VMs) for personal use. Their use is free as long as you don't go over a certain amount of usage of the VM. Now that TravisCI and my blog on GitHub are liked via the GHToken, whenever I update my blog's files on GitHub, it pushes those files to TravisCI which then runs the code. That code publishes the site via GitHub and just like that I have a website running!
