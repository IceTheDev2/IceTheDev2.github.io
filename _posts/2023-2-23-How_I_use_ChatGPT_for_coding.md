---
layout: post
title: How I use ChatGPT for coding
---

## Clearer text
English is not my native language. I'm not that good at it, but I can understand a message. The message is way too often not that clear to me, though. So, ChatGPT has helped me greatly in clarifying my documentation for functions.
For example, I feed the AI the code of my function, and let it explain what the function does. This way, I get clarifications that I could not think of, such as 'allow\[ing\] the user to start typing immediately without having to click on the input box first' in a function that focuses the keyboard to an input box.

## Simpler code
Being new to coding, I miss a lot of ways to simplify my code. ChatGPT helps me with this as well.

ChatGPT turned this:
```
global are_there_repeated_characters
are_there_repeated_characters = False

for character in input: # For every character in the input, it checks if there is another character that matches, and shows the repeated pattern warning if there is.
    count = 0
    for other_character in input:
        if character == other_character:
            count += 1

    if count > 1:
        are_there_repeated_characters = True
        return 'Repeated character(s): Your password contains at least one repeated character.'

if are_there_repeated_characters == False:
    return 'No repeated characters: Your password contains no repeated characters.'
```

to this:
```
for character in inputted_password:
    if inputted_password.count(character) > 1:
        return 'Repeated character(s): Your password contains at least one repeated character.'

return 'No repeated characters: Your password contains no repeated characters.'
```

It removed the unnecessary global are_there_repeated_characters variable and used the count method to determine how many times a character is found. If it's found more than 1 time, it's repeated, else, it's not. It's much simpler than my method of looping through every character, looping again through every character and checking if the first character is equal to the other character, unnecessarily using a global boolean variable. It didn't even have to be global!

## Explaining errors
It's not uncommon for someone new to programming, like me, to not understand what errors such as 'IndexError: string index out of range error' mean. ChatGPT can explain these errors in plain English:
'The IndexError: string index out of range error occurs when you are trying to access an element in a string that is out of range. This can happen if you are trying to access an index that is greater than or equal to the length of the string.
This line is trying to generate a random password by choosing characters from the character_sets list. If the character_sets list is empty, then the ''.join(character_sets) part will result in an empty string, which will cause an IndexError when secrets.choice() is called with an empty string.',
which is enough to understand what your code is doing wrong.

## Unique solutions
As I was on the verge of giving up for the day, trying to implement the deselection of text for [1.3.3 version of Passwordsy](https://github.com/IceTheDev2/Passwordsy/releases/tag/v1.3.3-alpha), I had an idea. Why don't I ask ChatGPT?

'I have a function in Python:
```
def copy_text(input_box) -> None:
    '''
    Called upon pressing the copy button,
    this function uses the keyboard module to simulate pressing CTRL and C to copy the selected text.
    '''
    keyboard.press(Key.ctrl_l)
    keyboard.press('c')
    keyboard.release(Key.ctrl_l)
    keyboard.release('c')
```
The input_box is a Tkinter box. How do I focus the keyboard on that input_box but also copy the user's selected text through CTRL + C?'

In seconds, the AI gave me a solution to a problem which had taken hours off my time:
'To focus the keyboard on the input_box in Tkinter, you can use the focus_set() method. You can call this method on the input_box before simulating the key presses to make sure the input_box is selected.

To copy the selected text in the input_box using CTRL + C, you can use the clipboard module in Python, which provides a way to interact with the system clipboard. Here's an updated version of the copy_text function that focuses the keyboard on the input_box and copies the selected text using clipboard:

```import clipboard
import keyboard
from keyboard import Key

def copy_text(input_box) -> None:
    '''
    Called upon pressing the copy button,
    this function uses the keyboard module to simulate pressing CTRL and C to copy the selected text.
    '''
    # Focus the keyboard on the input_box
    input_box.focus_set()

    # Simulate CTRL + C key presses
    keyboard.press(Key.ctrl_l)
    keyboard.press('c')
    keyboard.release('c')
    keyboard.release(Key.ctrl_l)

    # Get the selected text from the input_box and copy it to the system clipboard
    selected_text = input_box.selection_get()
    clipboard.copy(selected_text)
```

(For the record, the CTRL + C simulation was removed in the final release, because I realised it was unnecessary, and input_box.focus_set() was moved to the end)

I would have never found such a solution by googling or by any other method. ChatGPT is so intelligent it UNDERSTOOD human text and it thought of importing another module to alter the clipboard of the device, a totally different method to the one I was using, and which would enable me to focus the keyboard to the input_box as I needed to do that to deselect the text.

This will truly make programming much easier, especially for newbies like me. It also probably won't take programmers' jobs, as at least a little bit of knowledge about how these things work is still needed to work with the information ChatGPT gives you.

The world is going to drastically change very soon.
