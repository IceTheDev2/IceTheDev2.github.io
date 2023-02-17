---
layout: post
title: A few things I learned this past week
---

## Tkinter already has a pop-up menu built-in
I didn't know this when I first built the copy and paste buttons for my [password generator](https://github.com/IceTheDev2/Passwordsy)
in [version 1.2](https://github.com/IceTheDev2/Passwordsy/releases/tag/v1.2-alpha).

I struggled to get the mouse position by binding the root window to Motion, 
to send the mouse coordinates to each file for each tab of the program through parameters of a function,
to place a Tkinter button at those coordinates, but with a slight offset,
to remove the button when the user released their mouse button on a password_label.
Only for it to look ugly and work awkwardly.
  
<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52689140821/" title="1"><img src="https://live.staticflickr.com/65535/52689140821_c3a0dc3aa5_c.jpg" width="800" height="357" alt="1"></a>

Nevertheless, I discovered a much easier to do what I tried to do there when I found [this video from codemy.com on Tkinter menus](https://youtu.be/KRuUtNxOb_k)
and I updated the app with the better pop-up menus in [version 1.2.2](https://github.com/IceTheDev2/Passwordsy/releases/tag/v1.2.2-alpha).

## It's not 'occured', it's 'occurred'.
## The screenshots for the README.md on [Passwordsy](https://github.com/IceTheDev2/Passwordsy) are the ones inside of the main branch.
<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52689428944/in/dateposted-public/" title="2"><img src="https://live.staticflickr.com/65535/52689428944_feaa492944_c.jpg" width="800" height="175" alt="2"></a>

Which means that the screenshots will only update AFTER I merge a pull request into main.
  
All the struggle and questioning why my screenshots weren't updating is finally over.
  
## The sticky attribute and weight in Tkinter
The sticky attribute pins (sticks) the widgets to north, south, east or west.

The weight attribute makes a widget occupy as much space as it can, without obstructing other widgets.

## End
I really hope you enjoyed this short devlog and I can't wait to make the next one!
