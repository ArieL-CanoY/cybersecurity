# Normal Mode

These commands are applicable when in normal mode


You can combine most of these commands for advanced text manipulation and navigation

```python
l - move the cursor to the right 1 by 1
nl - move the cursor to the right by n number
```

```python
h - move the cursor to the left 1 by 1
nh - move the cursor to the left by n number
```

```python
j - move the cursor down 1 by 1
nj - move the cursor n lines down
```

```python
k - move the cursor up 1 by 1
nk - move the cursor n lines up

```

```python


```

```python
I - go to the first character of the line and go to insert mode
```

```python
a - go to the right of the character of the insert box and go to insert mode
```

```python
A - go to the last character of the line and go to insert mode
```

```python
u - undo
ctrl + r - redo
```

```python
o - insert new line at the bottom of the cursor's current line and go to insert mode
O - insert new line at the top of the cursor's current line and go to insert mode
```

```python
gg - go to the very top of the document
G - go to the very bottom of the document
```

```python
0 - go to the first character of the current line
0 - go to the first character of the current line
```

```python
$ - go to the last character of the current line
```

```python
w - go to the first character of the next word
b - go to the first character of the previous word
e - go to the last character of the current or next word 
ge - go to the last character of the previous word
```

```python
. - do all the commands you have done previously to the current word or line of the cursor
```

```python
y - enter to be copy
yy - copy/yank the current line
yi<character> - yank/copy inner characters of the character
	ex. yi', yi" yi() - this will copy all the characters inside the quote or parenthesis, etc.
ya<character> - yank/copy all characters including the character
 
```

```python
s - cut (current) the current character and go to insert mode
  - faster way for typing v + c
```

```python
S - cut (copy and delete)/substitute/delete the current line and go to insert mode
	- the same as command cc
```

```python
x - copy and delete a character from the left of the cursor box to the left side (just like pressing delete button) - in short it will cut

nx - delete n number of character/s
```

```python
X - delete a character from the left of the cursor box to the right side (just like pressing backspace) 
```

```python
d - cut (copy and delete) the specific condtion
dd - cut (copy and delete) the current line
dw - cut (copy and delete) a word forward from the right (delete the word)
db - cut (copy and delete) the word backward from the left (backspace the word)
dj - cut (copy and delete) the current and next line
dk - cut (copy and delete) the current and previous line the current and previous line
dG - cut (copy and delete) the current til the end line of the document
dgg - cut (copy and delete) the current til the first line of the document
```

```python
zz - make the cursor be on the middle of the screen
zt - make the cursor be on the top of the screen
zb - make the cursor be on the bottom of the screen
```

```python
D - delete all chars from the cursor to the end of the line
```

```python
r - relace single character
how to use:
	press r then press a character to change the currrent character of cursor
```

```python
/(string to search) - search for string in the entire document
/(string)\c - search for string and ignore case in the entire document
```

```python
f - find single string forward on the current line
F - find single string backward on the current line

after finding it:
; - go to the next occurrrence
, - go back to the previous occurrence
```

```python
H - puts cursor to the top of the screen
M - puts cursor to the middle of the screen
L - puts the cursor to the bottom of the screen

```

```python
<commands>t<commands> - this will do a command til a specified character
dt<character> - delete the charater from cursor up to the character specified
ct<character> - change til character specified
vt<character> - highlight current cursor's character til character specified
vt<aksdflkasjdf> - highlight current cursor's character til character specified
```

```python
<commands>i<character> - this will do the command inside/current character yiw - yank/copy the current word of the cursor 
yi' - yank/copy the characters inside the quote of the cursor
yi() - yank/copy the characters inside the parenthesis of the cursor
di() - cut (copy and delete) the characters inside the parenthesis of the cursor
ci() - delete all the characters inside the parenthesis of the cursor and go to insert mode

```

```python
print('asdfasdf')
```

hello
print('hello')

# Visual mode
```python
v - enter visual mode or highlighting mode and starts from the character of your cursor
```

```python
V - highlight the current line
```


```python
vnj - highlight n numbers of lines downward
vnk - highlight n numbers of lines upward
ve - highlight current character up to the end of the 
viw - highlight all the characters or the word on the cursor
```

```python
print('hello world')

print{'hello world'}
```

```

```



# Customization / Plugins

note: configure plugins by creating folder: ~/.vimrc.plugins

```python
>> set nocompatible - set plugins compatibility to VIM only

>> set wrap - wrap text when it extends beyonds screens

>> set number - show line number on the left side of the editor

>> set relativenumber - show and relates the number from the current line

>> set relativenumber number - show and relates the number from the current line and show the actual line number.

>> colorscheme <color> - set the background color of the editor
	colors:
		default
		ron
		habamax

>> xnoremap "_dP
	- after pasting the text you copied, it retains it to the register for future pasting.



```































