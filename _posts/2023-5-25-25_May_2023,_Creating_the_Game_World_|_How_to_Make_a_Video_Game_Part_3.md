---
layout: post
title: 25 May 2023, Creating the Game World | How to Make a Video Game Part 3
---

For this tutorial, I'll be using the Unity game engine. Check out [this](https://icethedev2.github.io/(13_April_2023)_How_to_Get_Started_with_the_Unity_Game_Engine-_Scene_and_Game_View/) tutorial to install Unity and set up a project.

In the [last post](https://icethedev2.github.io/18_May_2023_,_Creating_the_Game_World_-_How_to_Make_a_Video_Game_Part_2/), I made the player and the ground.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911146236/in/dateposted-public/" title="133"><img src="https://live.staticflickr.com/65535/52911146236_0dfe7c5602_o.png"/></a>

I'll make a Maze Runner in this tutorial series. Let's get started!

## Creating the Game World
To create the maze, you can either design it in a 3D modeling software such as Blender or use Unity's built-in tools. Here's how to create a maze using Unity's built-in tools.

Let's first make the plane bigger by increased the X and Z fields of the Plane's Transform from 1 to 10 (remember, Y is vertical).

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911345854/in/dateposted-public/" title="134"><img src="https://live.staticflickr.com/65535/52911345854_d5b35f823c_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911194846/in/dateposted-public/" title="135"><img src="https://live.staticflickr.com/65535/52911194846_04845f6ab8_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911651233/in/dateposted-public/" title="136"><img src="https://live.staticflickr.com/65535/52911651233_463540335d_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52910622982/in/dateposted-public/" title="137"><img src="https://live.staticflickr.com/65535/52910622982_99d1282b26_o.png"/></a>

## Creating the Maze
Let's make a cube and scale it to look like a wall.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911351034/in/dateposted-public/" title="138"><img src="https://live.staticflickr.com/65535/52911351034_6a55fca31b_o.png"/></a>

Press F to focus on it.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911589710/in/dateposted-public/" title="139"><img src="https://live.staticflickr.com/65535/52911589710_f5812e5c2b_o.png"/></a>

Move it above the ground. 

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911203286/in/dateposted-public/" title="140"><img src="https://live.staticflickr.com/65535/52911203286_4c07ae696d_o.png"/></a>


And use the [Scale Tool](https://icethedev2.github.io/(13_April_2023)_How_to_Get_Started_with_the_Unity_Game_Engine-_Scene_and_Game_View/#:~:text=%E2%80%A6The%20Scale%20Tool%2C%20used%20to%20select%20multiple%20objects%20and%20scale%20(make)%20one%20of%20them%20(smaller%20or%20bigger).) to scale it to be tall and long.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52910632522/in/dateposted-public/" title="141"><img src="https://live.staticflickr.com/65535/52910632522_0873004c70_o.png"/></a>

You may also want to round the values in the Transform component of the Cube (on the right side, in the Inspector).

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911208411/in/dateposted-public/" title="142"><img src="https://live.staticflickr.com/65535/52911208411_eef0c037cd_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911666468/in/dateposted-public/" title="143"><img src="https://live.staticflickr.com/65535/52911666468_04691e09de_o.png"/></a>

Just to be clean.

Don't forget to save with CTRL + S.

Now, look at the Scene Gizmo ([which I refered to as 'weird contruction' 🤦](https://icethedev2.github.io/(13_April_2023)_How_to_Get_Started_with_the_Unity_Game_Engine-_Scene_and_Game_View/#:~:text=In%20the%20top%20right%20corner%2C%20you%20might%20have%20noticed%20a%20weird%20construction%E2%80%A6)), and click the Green Y coordinate part of it.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911605580/in/dateposted-public/" title="145"><img src="https://live.staticflickr.com/65535/52911605580_876bc835c5_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911216516/in/dateposted-public/" title="146"><img src="https://live.staticflickr.com/65535/52911216516_5a2b064919_o.png"/></a>

You now have a top-down view of the game, which will help you build the maze.

You can now use CTRL + D to duplicate the 'Cube' and use the Move, Rotate, and Scale tools to move, rotate, and scale the cubes to make a maze! 

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52911373619/in/dateposted-public/" title="147"><img src="https://live.staticflickr.com/65535/52911373619_c324a7dd1c_o.png" alt="147"/></a>

Don't forget to round values in the Inspector and save!

Tip: Build the correct pathway to the end of the maze first and then build secondary paths from the main one.

## Conclusion
Developing a video game requires a lot of effort and dedication, but with the right tools, guidance, and motivation to be consistent (consistency is the most important thing in learning any skill) it's an achievable goal. In the future articles, I'll walk you through the entire process, from creating the game world to programming the player movement, adding enemies and obstacles, and implementing game logic.

Unity is a brilliant way to get into game development. The best way to learn any programming language or game engine is to build something you are truly passionate about with great consistency.

([ChatGPT, a language model trained by OpenAI](https://chat.openai.com/) helped write this post)

Thank you so much for checking out my blog, I sincerely hope you enjoyed this post, and expect more on Thursdays after 15:00 UTC!
