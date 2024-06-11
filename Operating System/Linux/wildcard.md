
```python
- characters that can be used to substitute for other characters in a command.
- used for searching, copying, moving, or manipulating files or text.
```


# *
```python
- used to match any characters and any size of characters

Examples:
	>> ls f*
		- list all the directories and files that starts with f with 0 or more characters.	
	>> cp dir/* .
		- copy all the files from "dir" directory and paste it from the current directory.
```


# ?
```python
- used to match a single or one(1) character

>> ls ?.txt
	- match all text files with only 1 character in their filename
```


# \[]
```python
- match all the individual characters within the square brackets.
- commonly used for range

>> ls [mfp]ile
	- list all the directories and files that the name is like mile, file, or pile.
>> ls file[1-10]
	- list all file from file1, file2, up to file 10
```



# {}
```python
- match specific group of characters within the curly brackets.

>> ls file{2,3,34}.txt
	- list all the text files with name of file2.txt, file3.txt and file34.txt
```


# \[^] or \[!]
```python
- match all the characters other than the characters within the brackets.

>> ls file[^3-5]
- list all the files other than file3, file4, and file5, filea, fileb, filex, file@.
```


# Escaping wildcards
```python
- use backslash before the wildcard to treat it as string or part of the string character
```

