---
layout: post
categories: city-neon
tags:
  - video game
  - game jam
  - modeling
  - russian coffee
title: modeling magic
---
if your only prior experience in 3d modeling was "modeling" golf balls for a trebuchet golf game, you (like i) may not have enough intuition to reason about how to get started modeling. i spent six hours on monday trying to model my character and then scrapped all of it the next morning.

![image: character concept art][character-concept]

why? i wasn't being particularly picky (which i _am_ apt to do), but i'd actually gone about the whole process in a not ideal way. let's say you were to set about modeling a low poly character. what might your approach be? probably the most obvious is to start from some vertices and edges or shape something already low poly. welp, after reading [sunday sundae](https://sundaysundae.co/how-to-make-low-poly-characters/)'s article on making low poly characters, i tried sculpting in a modeling software i'd never used before. there are many problems with this:

1. with little experience in modeling or sculpting or blender, i had no intuition about what choices to make. did i need to break my character model into separate objects? or _should_ they be one mesh? what's a mesh? why do i have to right-click so much?
2. their method is perhaps more intuitive for those familiar with sculpting, but for a noob, sculpting is most certainly harder than the alternative
3. and from my research, i found little community documentation and tutorial on their sculpt-and-shrink-wrap method

![image: sculpting attempt][sculpting]

this ended poorly. i ended up welding her arms into her thighs.

the next morning, after a psychedelic dream where i modeled the way i should have, i deleted the file and started over. within half an hour, i had a pretty good head.

![image: what a good head][head]

<!--more-->

i don't think my time sculpting was for naught though. i climbed a good chunk of the learning curve for blender. blender is a beast. there are so many shortcuts, hidden menus, windows, and so much *power*. it's _very_ intimidating at the beginnning, but after 20 hours, navigating blender feels much more natural. through struggle-busing with sculpting, i uncovered features i might not have otherwise. i would definitely reccomend learning blender with the advice to use a tutorial and that duckduckgo (or google) is your friend.

but if you want to start modeling a low poly character, i'd point you to this wonderful [tutorial by CG Geek](https://www.youtube.com/watch?v=Ljl_QFs9xhE). with their guidance, i have what i think is a pretty darn good first model.

![image: final lavender model][lavender]

excited by my success, i dove into rigging (carried single-handedly by [Karan Shah's tutorial](https://cgi.tutsplus.com/tutorials/building-a-basic-low-poly-character-rig-in-blender--cg-16955)) and had a lot of fun messing around with poses. rigging is actually mindblowingly cool. you can set up constraints on bones so that they move more like real bone-and-joints do. for example, you can constrain legs (with inverse kinematics) so that knees don't bend "inward". it's very procedural insofar, but i'm itching to try rigging something weird.

<div class="imageGallery" markdown="1">
![image: bending those legs][legs]
![image: excited broken jumping][excite]
<!-- ![image: posing][posin] -->
</div>

time period: monday

[character-concept]: {{site.baseurl}}/assets/cityneon-20190718-1.JPG
[sculpting]: {{site.baseurl}}/assets/cityneon-20190718-2.png
[head]: {{site.baseurl}}/assets/cityneon-20190718-3.png
[lavender]: {{site.baseurl}}/assets/cityneon-20190718-4.png
[legs]: {{site.baseurl}}/assets/cityneon-whatsup-homeskillet.gif
[excite]: {{site.baseurl}}/assets/cityneon-too-excited.gif
[posin]: {{site.baseurl}}/assets/cityneon-20190718-5.png
