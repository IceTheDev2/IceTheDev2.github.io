---
layout: post
title: 18 May 2023, Creating the Game World | How to Make a Video Game Part 2
---

For this tutorial, I'll be using the Unity game engine. Check out [this](https://icethedev2.github.io/(13_April_2023)_How_to_Get_Started_with_the_Unity_Game_Engine-_Scene_and_Game_View/) tutorial to install Unity and set up a project.

I'll make a Maze Runner in this tutorial series. Let's get started!

## Creating the Game World
To create the maze, you can either design it in a 3D modeling software such as Blender or use Unity's built-in tools. Here's how to create a maze using Unity's built-in tools.

## The Ground
To build a ground for the player to stand on, we can use a plane. Right-click in the hierarchy -> 3D Object -> Plane.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877734850/in/dateposted-public/" title="113"><img src="https://live.staticflickr.com/65535/52877734850_3dfc93559d_o.png"/></a>

Let's make it grey before creating other elements so we can distinguish it.

To color an object in unity, we need a material. Right-click in the Project tab -> Create -> Material.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877806903/in/dateposted-public/" title="114"><img src="https://live.staticflickr.com/65535/52877806903_a6cdc88afa_o.png"/></a>

Name it.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876781842/in/dateposted-public/" title="115"><img src="https://live.staticflickr.com/65535/52876781842_2b0c12c77a_o.png"/></a>

And change its color (Albedo - the term 'Albedo' is a scientific term used in the field of physics to describe the ratio of the amount of light reflected by a surface to the amount of light that falls on it).

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877748085/in/dateposted-public/" title="116"><img src="https://live.staticflickr.com/65535/52877748085_1f7d128939_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877528749/in/dateposted-public/" title="117"><img src="https://live.staticflickr.com/65535/52877528749_9d3a5a5a70_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877819013/in/dateposted-public/" title="118"><img src="https://live.staticflickr.com/65535/52877819013_f181fd61a4_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877755840/in/dateposted-public/" title="119"><img src="https://live.staticflickr.com/65535/52877755840_06d8e2b073_o.png"/></a>

Finally, drag the material...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876795597/in/dateposted-public/" title="120"><img src="https://live.staticflickr.com/65535/52876795597_f837193712_o.png" width="75" height="89" alt="120"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

...onto the plane in the Scene View...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876798087/in/dateposted-public/" title="121"><img src="https://live.staticflickr.com/65535/52876798087_0c8e1876c7_o.png"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

And save your changes with CTRL + S.

Also, reset the transform on the Plane to centre it at the 0, 0, 0 coordinates.

Right-click on the Transform component...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877837083/in/dateposted-public/" title="122"><img src="https://live.staticflickr.com/65535/52877837083_b8d9ea4e52_o.png"/></a>

...and click 'Reset'.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876813212/in/dateposted-public/" title="123"><img src="https://live.staticflickr.com/65535/52876813212_027f3ed7ce_o.png" width="603" height="90" alt="123"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

## The Player
Let's create a Capsule for the player.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877822950/in/dateposted-public/" title="124"><img src="https://live.staticflickr.com/65535/52877822950_6a0145e025_o.png"/></a>

Reset its Transform.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877892613/in/dateposted-public/" title="125"><img src="https://live.staticflickr.com/65535/52877892613_65b9c81e06_o.png"/></a>

Drag it a bit up.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877828685/in/dateposted-public/" title="126"><img src="https://live.staticflickr.com/65535/52877828685_eae9459e22_o.png"/></a>

And apply a red material to it.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877452051/in/dateposted-public/" title="127"><img src="https://live.staticflickr.com/65535/52877452051_511424ed82_o.png"/></a>

## Conclusion
Developing a video game requires a lot of effort and dedication, but with the right tools, guidance, and motivation to be consistent (consistency is the most important thing in learning any skill) it's an achievable goal. In the future articles, I'll walk you through the entire process, from creating the game world to programming the player movement, adding enemies and obstacles, and implementing game logic.

Unity is a brilliant way to get into game development. The best way to learn any programming language or game engine is to build something you are truly passionate about with great consistency.

([ChatGPT, a language model trained by OpenAI](https://chat.openai.com/) helped write this post)

Thank you so much for checking out my blog, I sincerely hope you enjoyed this post, and expect more on Thursdays after 15:00 UTC!
