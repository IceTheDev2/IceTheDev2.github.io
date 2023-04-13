---
layout: post
title: (13 April 2023) How to Get Started with the Unity Game Engine, Scene and Game View
---

## Introduction
If you've wanted to make a video game, you have most likely stumbled upon Unity. 

Unity is [the most popular game engine on itch.io](https://itch.io/game-development/engines/most-projects), an online video game marketplace. Unity can be used to create a wide variety of applications, not just video games. It is also really easy to get started with and not too complicated!

One thing to note is that the interface may look slightly different depending on which version of Unity you're using, but the general principles remain the same.

Unity has a wealth of online resources available for learning and troubleshooting, including official documentation, forums, and tutorials. As a beginner, it can be overwhelming to navigate all of this information, but it's important to take advantage of these resources to continue improving your skills.

## How to Install and Set Up a Project
Head to https://unity.com/download, click 'Download', run the installer and follow its instructions. It should install Unity Hub.

Run Unity Hub and click on 'Installs' on the left side of the window. Click on 'Instal Editor' and selected the latest version.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52811298757/in/dateposted-public/" title="50"><img src="https://live.staticflickr.com/65535/52811298757_6d0ea34da8_o.png" alt="50"/></a>

Once it's done installing, head back to the projects tab, click on new projects, and select a template that you want (keep in mind all of them only change a few settings or add a scene you can on other templates as well), name your projects, double-check the version and hit 'Create project'.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812267540/in/dateposted-public/" title="51"><img src="https://live.staticflickr.com/65535/52812267540_8c32d36fe9_o.png" alt="51"/></a>

And now you have a Unity project.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52811298732/in/dateposted-public/" title="52"><img src="https://live.staticflickr.com/65535/52811298732_33daf68cdb_o.png" alt="52"/></a>

## Unity's Interface
### Scene view
The is where users will create and manipulate the objects in their game world...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52811301537/in/dateposted-public/" title="53"><img src="https://live.staticflickr.com/65535/52811301537_849bc57241_o.png" alt="53"/></a>

...You can hold left-click (or the middle mouse button if you've selected a Tool) and move your mouse to pan, use the mouse wheel to zoom and hold right-click and move your mouse to look around.

At the top of the scene...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812267505/in/dateposted-public/" title="54"><img src="https://live.staticflickr.com/65535/52812267505_2696668fbe_o.png" alt="54"/></a>

...there are various useful buttons such as:
- <a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52811860581/in/dateposted-public/" title="55"><img src="https://live.staticflickr.com/65535/52811860581_cec277a758_o.png" alt="55"/></a> 2D, used to toggle the view between 3D and 2D.
- <a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812308998/in/dateposted-public/" title="56"><img src="https://live.staticflickr.com/65535/52812308998_45d9a3ec96_o.png" alt="56"/></a> The megaphone, used to toggle audio on and off.
- <a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812308983/in/dateposted-public/" title="57"><img src="https://live.staticflickr.com/65535/52812308983_9d71c31739_o.png" alt="57"/></a> Three layers, used to toggle various elemnts of the scene on and off: skybox, fog, post-processing, particles etc.
- <a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812308928/in/dateposted-public/" title="58"><img src="https://live.staticflickr.com/65535/52812308928_5327dabcaa_o.png" alt="58"/></a> The scene camera, used to change various attributes of the scene camera, such as the field of view.

There's also the side tools panel...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812055519/in/dateposted-public/" title="59"><img src="https://live.staticflickr.com/65535/52812055519_44f1b894e8_o.png" alt="59"/></a>

...which includes:
- The View Tool, used to view the scene from various angles, as described above.
- The Move Tool, used to select multiple objects and move one of them...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52811860656/in/dateposted-public/" title="60"><img src="https://live.staticflickr.com/65535/52811860656_5ae71e0348_o.png" alt="60"/></a>

- ...The Rotate Tool, used to select multiple objects and rotate one of them...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812309228/in/dateposted-public/" title="61"><img src="https://live.staticflickr.com/65535/52812309228_4921790779_o.png" alt="61"/></a>

- ...The Scale Tool, used to select multiple objects and scale (make) one of them (smaller or bigger).

- The Rect Tool, used to create and manipulate rectangular shapes.

- **The Transform Tool, used to move, rotate, and scale objects simultaneously**

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812309218/in/dateposted-public/" title="62"><img src="https://live.staticflickr.com/65535/52812309218_0b9efd00dd_o.png" alt="62"/></a>

In the top right corner, you might have noticed a weird construction...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812055474/in/dateposted-public/" title="63"><img src="https://live.staticflickr.com/65535/52812055474_3461ae704e_o.png" alt="63"/></a>

...This helps you figure out what perspective you are seeing the scene from. Try looking around the scene (holding right-click and moving the mouse) and watch it change!

You can also click on the cones or on the cones to change the perspective and a line of text below the construction will tell you from which side you are looking at the scene.

### Game view
The Game View is where users will see their game as players would see it.

Next to the 'Scene' tab, there is a 'Game' tab; this is the Game View...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52811298797/in/dateposted-public/" title="64"><img src="https://live.staticflickr.com/65535/52811298797_1b275afd46_o.png" alt="64"/></a>

...which is pretty self explanatory - it shows you what your game looks like.

The first option it includes...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812267605/in/dateposted-public/" title="65"><img src="https://live.staticflickr.com/65535/52812267605_d4db6c22fd_o.png" alt="65"/></a>

...lets you choose whether to view the game on your screen (in various aspect ratios and resolution as we see later) or to 'simulate' how it'd look on a different devices without actually having those devices.

Remaining on the 'Game' option, you can select which display to show your game in the next tab, what aspect ratio an resolution to use in the next, and adjust the scale (zoom) on the slider.

On the left side, you can choose whether to play focused, unfocused, or maximised, whether to include sounds, Unity Shortcuts, or Gizmos (icons for objects)...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812270475/in/dateposted-public/" title="66"><img src="https://live.staticflickr.com/65535/52812270475_79f48d8d88_o.png" alt="66"/></a>
...Under the Simulator option, you can choose a device to 'simulate', change the scale (zoom), to fit the device to the computer's screen, to rotate it, or to show the safe area.

On the left side, you can open a control panel to select the language of the device and its internet access.

## Some more tips
- To create an cube, for example, right-click in the Hierarchy (by default on the left side), select '3D Object' -> 'Cube'...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812052669/in/dateposted-public/" title="67"><img src="https://live.staticflickr.com/65535/52812052669_f3096b5eaf_o.png" alt="67"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52812052649/in/dateposted-public/" title="68"><img src="https://live.staticflickr.com/65535/52812052649_d0f3e21f43_o.png" alt="68"/></a>

- An asterix next to your scene name (by default 'SampleScene') means it's unsaved. **DO NOT FORGET TO REGULARLY SAVE YOUR SCENE AFTER EVERY CHANGE.**

## Conclusion
(Also, you can move each part of Unity around to your desire. If you want to return to the default layout, click 'Window' -> 'Layouts' -> 'Default')

Don't forget to save your project constantly by typing the key combination of CTRL + S. Do this as often as possible, even at the smallest change as you might forget later; this way, you can minimise the loss of progress in case of a power outage or other undesireable events.

Unity is a brilliant way to get into game development. The best way to learn any programming language or any game engine is to build something you are truly passionate about with great consistency.

([ChatGPT, a language model trained by OpenAI](https://chat.openai.com/chat) helped write this post)

I hope you enjoyed this blog post. Expect more!
