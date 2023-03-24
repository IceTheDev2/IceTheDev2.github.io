---
layout: post
title: (24 March 2023) What are Magic Numbers in Programming and Why Should You Avoid Them?
---

## Introduction
Magic numbers are hard-coded values used in programming that lack meaningful explanation or context within the code, and are often used multiple times throughout a program.

They are problematic because when a value has to be changed, it will have to be changed for every single occurance of it throughout the code. They can also make the code less readable and harder to maintain.

## What are Magic Numbers?
Magic numbers are ['unique values with unexplained meaning or multiple occurrences which could (preferably) be replaced with a named constant'](https://en.wikipedia.org/wiki/Magic_number_(programming)#:~:text=A%20unique%20value%20with%20unexplained%20meaning%20or%20multiple%20occurrences%20which%20could%20(preferably)%20be%20replaced%20with%20a%20named%20constant). They could appear when multiple similar objects are created within an app as in the following example of a Python-Tkinter program:

```
import tkinter as tk

root = tk.Tk()

file_btn = tk.Button(root, text='File', bg='blue')
file_btn.pack(pady=10)

edit_btn = tk.Button(root, text='Edit', bg='blue')
edit_btn.pack(pady=10)

view_btn = tk.Button(root, text='View', bg='blue')
view_btn.pack(pady=10)

root.mainloop()
```

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52766775295/in/dateposted-public/" title="31"><img src="https://live.staticflickr.com/65535/52766775295_e16e94c414_m.jpg" width="122" height="170" alt="31"/></a>


## Why are Magic Numbers a Problem?
It appears the 'blue' colour came out of nowhere. Also, if we want to change the attribute...

```
import tkinter as tk

root = tk.Tk()

file_btn = tk.Button(root, text='File', bg='red')
file_btn.pack(pady=10)

edit_btn = tk.Button(root, text='Edit', bg='red')
edit_btn.pack(pady=10)

view_btn = tk.Button(root, text='View', bg='red')
view_btn.pack(pady=10)

root.mainloop()
```

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52766852158/in/dateposted-public/" title="32"><img src="https://live.staticflickr.com/65535/52766852158_ffabc413b5_o.png" width="122" height="170" alt="32"/></a>

...we have to change it for every single occurance. Whereas if we had used a constant to define the color...

```
import tkinter as tk

root = tk.Tk()

btn_bg_color = 'blue'

file_btn = tk.Button(root, text='File', bg=btn_bg_color)
file_btn.pack(pady=10)

edit_btn = tk.Button(root, text='Edit', bg=btn_bg_color)
edit_btn.pack(pady=10)

view_btn = tk.Button(root, text='View', bg=btn_bg_color)
view_btn.pack(pady=10)

root.mainloop()
```

...we would have only had to change one value...

```
import tkinter as tk

root = tk.Tk()

btn_bg_color = 'red'

file_btn = tk.Button(root, text='File', bg=btn_bg_color)
file_btn.pack(pady=10)

edit_btn = tk.Button(root, text='Edit', bg=btn_bg_color)
edit_btn.pack(pady=10)

view_btn = tk.Button(root, text='View', bg=btn_bg_color)
view_btn.pack(pady=10)

root.mainloop()
```

..for the same result.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52766852158/in/dateposted-public/" title="32"><img src="https://live.staticflickr.com/65535/52766852158_ffabc413b5_o.png" width="122" height="170" alt="32"/></a>


## Best Practices for Avoiding Magic Numbers
- As soon as you start having multiple objects with the same values, evaluate your code to check if there are any magic numbers within it.
- Replace them with a constant as in the previous example.
- Preferably have a central section of your code where you define these constants:

```
gui_font_name = 'Roboto'
password_font_name = 'Consolas'
show_button_text = 'SHOW'
button_border_width = 2
button_fg_color = 'blue'
button_hover_color = 'gray'
button_border_color = 'black'
small_button_width = 60
copy_button_text = 'COPY'
title_columnspan = 2
checkbox_size = 20
checkbox_fg_color = 'grey'
checkbox_hover_color = ('grey', 'white')
password_width = 750
password_height = 30
password_border_width = 0
```

(Slightly modified snippet from [Passwordsy](https://github.com/IceTheDev2/Passwordsy))


## Conclusion
- Magic numbers are hard-coded values that seem to have come out of nowhere and that might be used in multiple places for similar objects.
- They can be problematic for the readability and maintainability of the code, as you'd have to change every single value instead of one.
- You can avoid them by checking your similar objects and making a central section to define the constants that will replace them.
