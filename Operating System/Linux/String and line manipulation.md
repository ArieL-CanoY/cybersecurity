# tr

```bash
- definition: translate or delete characters
- meaning translate.

Examples:

cat file.txt | tr -d ' '       - delete a space on a file

cat file.txt | tr 'a-z' 'A-Z'   - make all the small letter to capital letter

cat file.txt | tr ' ' '-'     - change all space to hyphen 

```

# awk

```bash
- definition: pattern scanning and processing language
- awk word comes from three(3) people who made the command.

note: use only single quote

Examples:

echo 'hello world' | awk '{print $1}'  - will output the first word which is hello
	
 awk 'length($1) > 5' sample.txt    - output the first word of every line in sample text that has length of more than 5

	options:
		-F [delimiter]       - match a separator
			ex. awk -F ":" '{print $1}' /etc/passwd

```

# cut

```bash
definition: remove sections from each line of files

Examples:

echo 'hello world' | cut -b 1-7    - will select binary from index number 1 to 7 and output is "hello w"

cut -c 1,3,5 message.txt       - the message is "hello world" and the output is "hlo"

	options:
		-c         - characters same as -b
		-b         - bytes same as -c
		-d         - delimeter - string separator like /, :, ' ', etc. Same as <string>.split() in Python

echo 'this:is:an:example' | cut -d ':' -f 3      - output is 'an'





```



# uniq

```python
definition: report or omit repeated lines, does not include repeated string in single line,
uses: must use sort before uniq because it will not treat duplicate string if multiple strings are not in consecutive line.
	this will work because duplicate is in contact with each other.
		hello
		hello
		world

	this will not work because duplicate string are separated from each other.
		hello
		world
		hello

normal use: uniq [filename]
using pipe: cat <filename> | uniq

	options:
		-c   - print every line and their number of occurence
			ex.
				uniq -c [filename]
					1 this
					2 none
					1 hello

		-d    - list all the duplicates

Example/s:
message.txt:
	hello
	world
	hello

command: uniq message.txt
output:
	






```


# sed

```python
definition: stream editor for filtering and transforming text

sed -n '/textToSearch/p'     - just like grep

sed '/s/[text to find]/[text to replace]/' [filename]      - find and replace text once in a line on a file

sed '/s/[text to find]/[text to replace]/g' [filename]      - find and replace all text in a line on a file

sed '/[text to find]/d' [filename]     - delete the line where the text is found

echo 'hello:world:this' | sed 's/:/\n/g'
	- search for - 's/', colon ':', then replace with new line - '/\n' and apply to all colon in the same line '/g'
	- output is:
		hello
		world
		this



```



# expand and unexpand
```python

definition:
	expand - convert tabs to spaces
		ex. expand [filename]


	unexpand - convert spaces to tabs
		ex. unexpand [filename]
	






```


# tee
```python
definition: read the output and use tee to write or input it on a file

	ex. 
		ls -al | tee output.txt
```