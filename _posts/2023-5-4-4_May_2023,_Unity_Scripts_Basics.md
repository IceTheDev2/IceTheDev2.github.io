---
layout: post
title: 4 May 2023, Unity Scripts Basics
---

## 🔍Introduction
Welcome to part 4 of IceTheDev2's beginner's guide to Unity!

## Creating a Script
There are 2 ways to create a script in Unity.

You can right-click in an empty space in the Assets folder within the Project tab, select Create > C# Script...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855668248/in/dateposted-public/" title="99"><img src="https://live.staticflickr.com/65535/52855668248_a4f541723b_o.png"/></a>

...Name it...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855399379/in/dateposted-public/" title="100"><img src="https://live.staticflickr.com/65535/52855399379_1982d3133b_o.png"/></a>

...and drag into onto the Cube. Save the scene with CTRL + S and click once on the Cube in the Hierarchy to open its Inspector.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855401849/in/dateposted-public/" title="101"><img src="https://live.staticflickr.com/65535/52855401849_be89836592_o.png"></a>

We can see 'BasicScript' is attached to the Cube as a Component.

To remove a component, right click on its title in the Inspector...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855403849/in/dateposted-public/" title="102"><img src="https://live.staticflickr.com/65535/52855403849_eb9280fc29_o.png"/></a>

...and select 'Remove Component'.

To delete a script from the project's assets, click on it once and press the 'DEL' key.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52854654252/in/dateposted-public/" title="103"><img src="https://live.staticflickr.com/65535/52854654252_070fde0632_o.png"/></a>

Click on 'Delete' or hit 'Enter'.

You can also right-click on the script and click 'Delete'.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855628730/in/dateposted-public/" title="104"><img src="https://live.staticflickr.com/65535/52855628730_401b8dce90_o.png"/></a>

The other way to create a script is to open the object's inspector...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52854657817/in/dateposted-public/" title="105"><img src="https://live.staticflickr.com/65535/52854657817_3cedcf4524_o.png"/></a>

...click 'Add Component', write the name of the script and hit 'Enter' twice..

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855242026/in/dateposted-public/" title="106"><img src="https://live.staticflickr.com/65535/52855242026_12208ac23c_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855687768/in/dateposted-public/" title="107"><img src="https://live.staticflickr.com/65535/52855687768_4d1713a0e8_o.png"/></a>

## Opening a Script
In the following example, I will use Visual Studio 2022. Though, you can use any code editor you want.

Firstly, let's make sure we have the right code editor selected. Go to 'Edit' at the top...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855422149/in/dateposted-public/" title="108"><img src="https://live.staticflickr.com/65535/52855422149_78b11072e2_o.png"/></a>

...select 'Preferences...' and make sure you're on the 'External Tools' tab.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855696403/in/dateposted-public/" title="109"><img src="https://live.staticflickr.com/65535/52855696403_2c23330019_o.png"/></a>

Look at the External Script Editor. If it's not your preferred editor, select and change it.

To open a script, you have 2 options similar to the ones for creating. You can either double-click on the script in the project's assets or in the object's inspector.

## Script Syntax
Once opening the script, you'll get something similar to this:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BasicScript : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        
    }
}
```

Let's talk about each section one-by-one.

### 'using' tags
In C# (C-Sharp, the programming language used by Unity) 'using' means we are importing, telling the program we will use a certain library.

System.Collections provides classes that implement various collections of objects, such as lists, queues, and hash tables.

System.Collections.Generic contains generic collection classes, which provide a type-safe and efficient way to store and manipulate groups of objects.

UnityEngine provides all the classes and functions that are specific to Unity game engine development. It includes classes for creating game objects, manipulating their properties, controlling their behavior, and rendering graphics.

### public class BasicScript : MonoBehaviour ???
1. public - This keyword specifies that the class is accessible from any other code in the project.

2. class - This keyword is used to define a class, which is a blueprint for creating objects.

3. BasicScript - This is the name of the class. You can choose any name you like for your class, as long as it follows the [C# naming conventions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions).

4. : MonoBehaviour - This is the base class that the BasicScript class is inheriting from. MonoBehaviour is a class provided by Unity that allows you to attach scripts to game objects and interact with them at runtime. By inheriting from MonoBehaviour, the BasicScript class gains access to all of the MonoBehaviour's built-in methods, such as Start(), Update(), FixedUpdate(), etc.

### void Start()? void Update??
`void` is a keyword in C# that is used to indicate that a method (such as `Start()` and `Update()`) does not return a value.

`Start()` is called when the scene is first loaded. It can be used for setting up references to other objects, initialising variables etc.

`Update()` is called every frame. It can be used for updating the position, rotation, or scale of objects based on user input, physics, responding to user input, checking for collisions, animating the object, updating variables etc.

### Comments
A comment is a piece of text that is ignored by the compiler. Use these to explain why something is done, and not what the code does. The code should be self-explanatory.

In the example above, the comments explain to new users when `Start()` and `Update()` are called.

Generally, code is written and read by people who know the language and do not need these kinds of comments.

To declare a comment use two slashes (//).

## Testing a Script
To test a script, `Debug.Log()` is commonly used. This method writes a message in the console.

Try writing `Debug.Log("Hello, World!");` in the `Start()` method. Don't forget to use double quotes (""), which are necessary in C#. "Hello, World!" is a string (piece of text) that is an argument in the method. Don't forget to end with a semicolon (;), as is required in C#.

Don't forget to save the script (CTRL + S) and run the game by clicking the play button at the top.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855717808/in/dateposted-public/" title="110"><img src="https://live.staticflickr.com/65535/52855717808_92f9ee8fca_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855666990/in/dateposted-public/" title="111"><img src="https://live.staticflickr.com/65535/52855666990_f5989cf3c4_o.png"/></a>

(Your Unity will not be red. I will show in a future post how to turn in red in play mode.)

You can also try writing `Debug.Log("Hello, World!");` in the `Update()` method.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855666990/in/dateposted-public/" title="111"><img src="https://live.staticflickr.com/65535/52855666990_f5989cf3c4_o.png"/></a>

By the way, CTRL + P is the shortcut to enter play mode.

## Conclusion
Scripts are a vital part of game development. They can be used to manipulate objects' positions, rotations, and scales, and they will get cooler with [variables](https://mammothinteractive.com/variables-in-c-unity-tutorial/) and [loops](https://learn.unity.com/tutorial/loops-z2b#).

Unity is a brilliant way to get into game development. The best way to learn any programming language or game engine is to build something you are truly passionate about with great consistency.

([ChatGPT, a language model trained by OpenAI](https://chat.openai.com/) helped write this post)

Thank you so much for checking out my blog, I sincerely hope you enjoyed this post, and expect more on Thursdays after 15:00 UTC.
