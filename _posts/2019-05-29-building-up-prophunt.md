---
layout: post
title:  "building up basic features"
date:   2019-05-29 21:11:22 -0400
categories: prophunt
tags: [web dev, video game, team work, gin]
---

![image: recent PRs][lots-of-prs]

our teams been hard at work since school's let out (look at all the pull requests)! 

mattf has been polishing up lobbies so people can join games and games immediately divide teams and start when filled. (also did some nice styling in his typical aesthetic, haha)

kvfrans has started on broadcasting player movement and calculating collisions on the server-side. initially we were using the [p5.play](http://molleindustria.github.io/p5.play/) for front-end collision calculation. however, we decided to do calculations on the server-side to ensure that lag doesn't factor into collisions, deaths, etc. 

i've been working on the data representation of maps (we really want to be able to do custom maps!) and also implementing the basics of the editor.

![image: making a map][map-updates]

cor previously did a lot of work earlier on setting up the project and doing realtime multiplayer movement. for now, he's taking a break as he starts interning, but also sending us a lot of good code review comments and suggestions.

<!--more-->

![image: great comments][pr-comments]

[lots-of-prs]: {{site.baseurl}}/assets/prophunt-20190529-1.png
[map-updates]: {{site.baseurl}}/assets/prophunt-20190529-2.gif
[pr-comments]: {{site.baseurl}}/assets/prophunt-20190529-3.png