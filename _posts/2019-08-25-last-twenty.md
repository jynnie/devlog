---
layout: post
categories: city-neon
tags:
  - video game
  - game jam
  - shaders
  - unity3d
  - turkish coffee
title: the shiny last 20%
---

there's a saying that the last 20% of polish takes 80% of the effort. (or something like that). while in theory, the game mechanics were now in place - basic as they were - it's not anywhere near fun to look at.

the last bit of my time, which took more thought than implementing colliders and the like, was spent writing shaders and making attack animations.

going for the clean, donut county look, i went with implementing a toon shader.

![image: shader][shader]

what's a shader?

in a nutshell, shaders are a computer program that does calculations for rendering shading such as light and color. it can be used to do some fun graphical effects and runs on the graphics card (GPU). for more information, i'd suggest reading [the book of shaders](https://thebookofshaders.com/01/).

toon shaders tend to be the simplest (in theory). in simple terms, we calculate how much light hits the object at a certain point. if that's above or below some threshhold, we treat it as one base light amount. so let's say, anything with greater than 50% brightness get's treated as 60% bright and everything else as 20%. thus instead of getting smooth gradients, we get a "flattened", toon look. i think blender's visual interface for shaders might be useful for explaining this.

![image: blender interface][blender]

blender shaders are unfortunately inncompatible with unity. so with the help of these references ([roystan's](https://roystan.net/articles/toon-shader.html) and [willchyr's](http://willychyr.com/2013/11/unity-shaders-depth-and-normal-textures/)) i got this:

![image: pretty toon shaders][shaded]

the hardest polish was attack animations. even with a multitude of references,

<div class="imageGallery" markdown="1">
![image: aikido stance reference][aikido0]
![image: aikido throw reference][aikido1]
![image: aikido moves reference][aikido2]
</div>

not only was making the actual animations difficult,

![image: failure to throw][fail]

but syncing up the enemy's animation to the player's was SOOOO difficult

![image: attack animations][attack]

but, i finished. and the final showcase is up next.

time period: friday and saturday

<!--more-->

a brief aside

> i got a little confused on how to apply unity shaders to specific parts of a model in unity, so here's a gif to help other people. i first assigned different materials to the model in blender. and then could reassign them in blender.

![image: applying unity shaders to a blender model][help]

[shader]: {{site.baseurl}}/assets/cityneon-20190825-shader.png
[blender]: {{site.baseurl}}/assets/cityneon-20190825-blender.png
[shaded]: {{site.baseurl}}/assets/cityneon-20190825-shaded.gif
[help]: {{site.baseurl}}/assets/cityneon-20190825-applying.gif
[attack]: {{site.baseurl}}/assets/cityneon-20190825-attackref.gif
[fail]: {{site.baseurl}}/assets/cityneon-20190825-fail.gif
[aikido0]: {{site.baseurl}}/assets/aikido-reference.jpg
[aikido1]: {{site.baseurl}}/assets/aikido-reference-2.jpg
[aikido2]: {{site.baseurl}}/assets/aikido-reference-3.jpg
