---
layout: post
categories: city-neon
tags:
  - video game
  - game jam
  - ai
  - unity3d
  - turkish coffee
title: in the sandbox
---

i migrated my models and animations into unity with relative ease and switched my focus to building in basic mechanics. basic movement was controlled by arrow keys and her move would be a counter, inspired by aikido. but to counter, something needs to attack.

![image: planning the enemy ai][plans]

i first setup our creepy crawly boys to follow you if you are in their line of sight (left). i used Unity's AI to set this up, following these tutorials for [following a player](https://www.youtube.com/watch?v=LDcIDUAXVFU) and [raycasting line of sight](https://answers.unity.com/questions/386909/how-do-i-get-my-emeny-ai-to-detect-if-he-sees-a-pl.html). and if you aren't in line of sight, i had our creepers wander around randomly (right), reference [thread](https://forum.unity.com/threads/solved-random-wander-ai-using-navmesh.327950/).

<div class="imageGallery" markdown="1">
![image: following the player][following]
![image: wandering aimlessly][wander]
</div>

altogether this resulted in some funny behaviors :)

![image: being rolled away][rolling]

next, actual attacks! i gave the creepy crawly boys a grab attack (one of the first attacks you learn to deflect in aikido). if in a certain range of a creepy, he will start to attack. if the player collides with a grab, they are "caught" (left). but, if the player collides with the grab and is countering, the attack will be rendered useless (right). i focused on just setting up the technical aspects - so i used colors to reflect states (i.e. attacking is red, caught is black, and countered is yellow). and used a pill geometry as the attack collider.

<div class="imageGallery" markdown="1">
![image: captured][captured]
![image: countered][counter]
</div>

with this working, it was time to return to polishing animations and shaders :)

time elapsed: thursday

[plans]: {{site.baseurl}}/assets/cityneon-20190825-plans.JPG
[following]: {{site.baseurl}}/assets/cityneon-20190825-following.gif
[wander]: {{site.baseurl}}/assets/cityneon-20190825-wander.gif
[counter]: {{site.baseurl}}/assets/cityneon-20190825-counter.gif
[captured]: {{site.baseurl}}/assets/cityneon-20190825-captured.gif
[rolling]: {{site.baseurl}}/assets/cityneon-20190825-getit.gif
