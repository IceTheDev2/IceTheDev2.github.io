---
layout: post
title: (16 March 2023) I have managed to solve a problem (mostly) on my own.
---

## 🔎The problem
I was using Python with the Tkinter and CustomTkinter modules. I had an input box and I needed to take the sentence the user inputted and highlight (with a red foreground, I had decided) every starting letter of every word, as well as any digits or punctuation. 

Why was I doing this? I was working on an expansive update for [Passwordsy](https://github.com/IceTheDev2/Passwordsy), in which I would introduce password-generation methods other than [a random secure string of customisable character sets](https://github.com/IceTheDev2/Passwordsy/releases/tag/v1.3-alpha).

## 👏First iteration
After working really hard to make the highlighting system work one night, I eventually had enough and asked ChatGPT to do it for me. I ended with this (I thought at the time) stunning solution:
```
        def display_password():
            """
            Called as the user types,
            this function calls the produce_password function of sentence_input_logic.py
            to get a password based on the user's sentence,
            and displays it on the screen.
            """
            password_output = produce_password(self.input_box.get())
            # Produce password would (attempt, at least, to) create a password with each starting letter of every letter, as well as any digits or punctuation.

            split_full_sentence = self.input_box.get().split(' ')
            letters_to_be_coloured = {}

            for word in split_full_sentence:
                start_index = self.input_box.get().index(word)
                letters_to_be_coloured[f'1.{start_index}'] = f'1.{start_index + 1}'

            for i in range(len(self.input_box.get())):
                character = self.input_box.get()[i]
                if character in string.digits + string.punctuation:
                    # Find the start index of the character
                    start_index = i
                    # Iterate over the remaining characters in the sentence to find any additional occurrences
                    for j in range(i + 1, len(self.input_box.get())):
                        if self.input_box.get()[j] == character:
                            # Add the start and end indices of the character to the dictionary
                            letters_to_be_coloured[f'1.{start_index}'] = f'1.{j + 1}'
                    # Add the start and end indices of the character to the dictionary for the first occurrence
                    if f'1.{start_index}' not in letters_to_be_coloured:
                        letters_to_be_coloured[f'1.{start_index}'] = f'1.{start_index + 1}'

            if password_output != '':
                self.password_label.configure(state='normal')
                self.password_label.delete('1.0', 'end')
                self.password_label.insert('1.0', self.input_box.get())
                self.password_label.configure(state='disabled')

                for index, warning in enumerate(logic.check_password_strength(None, password_output)):
                    self.warning_labels[index].configure(text=warning)
                    self.warning_labels[index].grid(row=3 + index, column=0, padx=10)
            else:
                for label in self.warning_labels:
                    label.configure(text='')
                    self.password_label.configure(state='normal')
                    self.password_label.delete('1.0', 'end')
                    self.password_label.configure(state='disabled')

            for letter in letters_to_be_coloured:
                self.password_label.tag_add('red', letter, letters_to_be_coloured[letter])
def produce_password(sentence):
    """
    Called as the user types a sentence to be turned into a password,
    this function takes the sentence the user is typing,
    splits it into words,
    and returns the first letter of each word,
    as well as any punctuation and numbers.

    Parameters
    ----------
    sentence: str
        The sentence the user is typing.
    """
    if sentence != '':
        password = ''

        split_full_sentence = sentence.split(' ')
        letters_only_sentence = ''

        for word in sentence:
            for letter in word:
                if letter not in string.digits and letter not in string.punctuation:
                    letters_only_sentence += letter

        split_letters_only_sentence = letters_only_sentence.split(' ')

        for word in split_full_sentence:
            letter_taken = False
            for character in word:
                if character in string.digits or character in string.punctuation:
                    password += character
                elif not letter_taken:
                    password += character
                    letter_taken = True

        return password
    else:
        return ''
```

## 😬 Issues start to be noticed
That solution seemed remarkable. 'I would have never thought of such a solution', I thought. 'ChatGPT is so great!'

That was until I tried inputting 'This is' and it highlighted the first 'i' in 'This'. And until I inputted anything containing quotes ('') and it highlighted everything within the quotes.🤦

(I have no screenshots, unfortunately)

## 🎯My eventual solution
I will be honest now, I put that issue off for way longer than I should have. 

I worked on other stuff, such as [going down a (lucky) rabbit hole and discovering CustomerTkinter in an attempt to design a slider](https://icethedev2.github.io/CustomTkinter_-_A_modern-looking_version_of_Tkinter/), but I was eventually fed up with the slow progress on the update and decided to group the next tasks into 6 categories: BUGS, CODE-CLEANING, CHANGES, ADDITIONS, GUI, PUBLISHING. 

This way, I would have a better sense of where I was situated in the progess for the update.

The first bug was 'The sentence in highlighted corectlyyy'. The next day (yesterday as you're reading this), early in the morning, I got to work and figured out a solution poorly written in plain English for my problem:

```
Set up a dictionary (dict)

char_dict = {}

for i, char in enumerate(sentence):
    if char.isspace():
        char_dict[i] = "space"
    else:
        char_dict[i] = char

First letter = False
for key, value in char_dict.items():
	if value is punctuation or digits:
		highlight 1.key + 1.key+1
    	elif value is space:
		first_letter = false
	elif fisrt_letter = false
		hightlight 1.key + 1.key+!
		first_letter = true'
```

I tried it, I got errors.
```
    for key, value in letters_to_be_coloured.items()
                                                    ^
SyntaxError: expected ':'
```

Easy fix. Add a ':'.

```
    for i, char in enumerate(sentence):
                             ^^^^^^^^
NameError: name 'sentence' is not defined
```

Oh, yeah. The sentence variable doesn't exist anymore. I'll just replace it with self.input_box.get()

```
    if value is punctuation or digits:
                ^^^^^^^^^^^
NameError: name 'punctuation' is not defined
```
Oh, yeah. That and digits are within the string library.

(This would be a good time to mention, I like running my code as much as possible. I prefer getting an error and fixing it immediately as I know where it is rather that going over my code to catch all of them at once before they occur.)

Aaaand now no sentence appears.

Aaaand I figured out (by printing to the console) that the entire sentence would have been highlighted if it appeared.

Aaaand I tried to fix both issues, but now only the first and last characters are highlighted (though the sentence appears, at least).

Then I had an anger moment with ChatGPT, trying to figure out the valid text indices for deleting and inserting text into a Tkinter text widget (They're '1.0' and 'end', not 0 and 'END').

Then I figured out the variable first_letter_taken variable isn't properly set to false and promptly fixed the issue.

I tested the code.

With 'This is' and single and double quotes.

It worked.

No bugs.

<a href="https://ibb.co/xq7ZmzV"><img src="https://i.ibb.co/B2Ck4T8/30.png" alt="30" border="0"></a><br /><br />

I wrote code for a solution for a problem (mostly) on my own.

```
def display_password():
    """
    Called as the user types,
    this function calls the produce_password function of sentence_input_logic.py
    to get a password based on the user's sentence,
    and displays it on the screen.
    """
    char_dict = {}
    letters_to_be_coloured = {}

    self.password_label.delete('1.0', 'end')
    self.password_label.insert('1.0', self.input_box.get())

    for i, char in enumerate(self.input_box.get()):
        if char.isspace():
            char_dict[i] = "space"
        else:
            char_dict[i] = char

    first_letter_taken = False
    for key, value in char_dict.items():
        if value in string.punctuation or value in string.digits:
            letters_to_be_coloured[f'1.{key}'] = f'1.{key + 1}'
        elif value == 'space':
            first_letter_taken = False
        elif not first_letter_taken:
            letters_to_be_coloured[f'1.{key}'] = f'1.{key + 1}'
            first_letter_taken = True

    for key, value in letters_to_be_coloured.items():
        self.password_label.tag_add('red', key, value)
```

Thank you for reading this post. Expect new ones every Thursday, at around 17:00 GMT.
