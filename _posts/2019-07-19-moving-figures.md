---
layout: post
categories: city-neon
tags:
  - video game
  - game jam
  - animations
  - unity3d
  - mint mojito (philz)
title: moving pieces and creepy crawlies
---
there's a lot of potential once you've got a skeleton. both of an idea and of a rigged model. i realize i didn't do much explaining last post, so i'll briefly do a deep dive of what rigging is and why it's so powerful. _if you really don't care or already know, skip to the next 🐬._

**rigging** is a technique for animating models by associating a skeleton with parts of your model. for 3d models, there's a **mesh**, which is a bunch of polygons that cover the surface area of the model (pictured 1st below). it's how the volume and shape of a model is determined. like flesh. rigging provides a **skeleton** (pictured 2nd) - giving logic to the way the flesh/mesh should move. 

how? 

each bone in a skeleton can affect parts of the mesh by different amounts, called **weights**. kind of like an area of influence. many programs can automatically associate weights between bones and mesh (by simply only influencing the mesh neearest to that bone). you can also manually associate weights between a bone. blender represents the weights a bone has on mesh in a kind of heatmap (pictured 3rd), where red is having a high weight and blue is none. 

<div class="imageGallery" markdown="1">
![image: mesh of lav][mesh]
![image: skeleton of lav][skelly]
![image: weight of the left thigh on mesh][weight]
</div>

getting this right makes animations a lot easier 🐬 and therefore my wednesday too. i quickly sculpted a rough mesh and rig for my enemy on wednesday and got to making idle and walking animations for all my models. another showcase for how powerful blender is, all this modeling, rigging, and animating were done in blender. and my little macbook pro also cried very minimally while running blender (the same of which cannot be said of running unreal engine). 

_skip to the next 🌊if you want to avoid a rant about how cool and easy 3d animation is with tech._

animating is also insanely easy. you basically pose your character and save all the details of a bones location and rotation to a keyframe associated with a certain time. then you do the next pose your character should hit and save it like ten seconds downstream. and when you hit play, the program can interpolate what transformations need to happen to get from one pose to another within the given time. it's actually insane how much work is extrapolated away. if you think about the alternate of posing all the frames in between (like with claymation), so much time is saved.

![image: crawl animation][crawl]

this doesn't mean posing is easy. it's hard to think about what's a natural-looking way for a model to move and it's harder to think about what keyframes are necessary to get that. but it's mindboggling to me that the above crawl animation is made of only two unique, keyframed poses. (maybe that's why it looks a little awkward though haha).

🌊 so, jessica, you've been doing all this in blender. but is blender a game engine? nope, it is not, haha. and i realized it was time to migrate into a game engine. initially, i really wanted to try to use unreal engine 4. i even installed the epic games store launcher*. i put the model in and managed to get things to move.

![image: a posing][a]

but you might notice, after all i talked about animations, that she's awfully stiff in that gif.

<!--more-->

well, after a lot of research and trying, i was unable to get any of my animations to associate with the imported models. and while i really wanted to see if unreal's graphics are as great as people attest - the lack of resources (both relevant tutorials and community posts) that i decided it was not worth the time tradeoff**. 

so i switched to unity. why unity? i have previous experience developing 2d games in unity, but don't have as much experience with 3d development. and unity, while buggy, has an extensive trail of resources. i might also claim that unity is more intuitive and friendlier than unreal. to attest to that, i set up models, a basic environment, cameras, lighting, player movement, and ✨_animations_✨ on the same day. BUT, i'm not gonna share any screenshots till next post. it deserves it's own post :P

time elapsed: wednesday

*which i think is stupid to need to run a game engine, but i digress. <br/>
**a time tradeoff that i didn't even have a good sense of how long it might take. and while i want to learn new technology, i also think i'd learn plenty in another program.

[mesh]: {{site.baseurl}}/assets/cityneon-20190719-mesh.png
[skelly]: {{site.baseurl}}/assets/cityneon-20190719-skelly.png
[weight]: {{site.baseurl}}/assets/cityneon-20190719-weight.png
[crawl]: {{site.baseurl}}/assets/cityneon-20190719-scaries.gif
[a]: {{site.baseurl}}/assets/cityneon-20190719-a-posing-around.gif