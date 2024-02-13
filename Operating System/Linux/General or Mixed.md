General commands for linux like printing strings on the terminal, listing files, changing directories, print working directory

```bash
echo - printing string and putting text on a file

	echo "hello world" - print hello world in terminal
	
	echo "hello world" > sample.txt - put hello world on a file sample.txt, create a file if the file is not exist
	
	echo "hello world" >> sample.txt - add or append the text on sample.txt, create a file if the file is not exist
	
	echo 'hello world' > * - overwrite text to all file in the current directory (use >> to append or add instead)
	
ls - list content of current directory
	
	ls [flags/switches/options] - structure of the command
	
	ls -l - list files and directories in a list down
	
	ls -a - list all files including hidden files
	
	ls -al/la - list all files including hidden files in a list down
	
	ll - shortcut for "ls -l" for some distribution
    
    ls -R   - recursive show the list of files and directories in the curretn directory

cd - change directory to home

cd [directory] - change to specified directory if valid

     you can change directory by this: ./Desktop or when going to previous directory: ./.. or ..
     you can go back to the previous directory by typing cd -

cat - concatenate content and put it terminal

pwd - print working directory (directory where you are)

apropos [use] - list command depends on the use you type 


crontab -e - edit and set automation for specific task

wget [url] - used to get file from a hosted server

dpkg - unpacking to unzip deb packages

whatis [command] - tell what is the use of that command 

whereis [command/file/directory] - give the absolute path of what users has type

head [filename] - output the first 10 lines of a filename
	

tail [filename] - output the last 10 lines of text

	- n [num of line] - output the specific number of lines of a filename

realpath [filename] - get the absolute path of the filename

cmp [filename1] [filename2]   - compare two file name

diff [filename1] [filename2]   - compare the difference between the two filenames

diff [directory1] [directory2]   - compare the difference between the two directories

wc -l [filename]    - print the number of count of lines of the text

man [command] - show the manual pages of the command

info [command] - show the information documents of the command

[command] --help  - show the commands and other useful info how to use the command

history    - show command history

![history num]    - execute the command based on its number

!-1    - execute the previous command

!!     - execute the previous command

![command]    - execute the last command used

xargs:
	command1 | xargs command2    - the output of command1 will be the argument of the command2




**Symbol/Operator:**



& - set as job

     git clone <repository> & apt-get update -y & apt-dist upgrade -y - add 3 task to the job 

     firefox google.com & - open firefox and search for google while you can use the command line/terminal

&& - execute multiple commands in 1 line after continuous successfully executed the previous commands

> - set the string on a file (doesn\'t append, means overwrite)

>> - add the string on a file (append)

  

```



# flag and switch
```python
flag
	- change output
	- does not take arguments
	- ex are -l -a -d


switch
	- change the behavior
	- can take arguments
	- ex. --sort=time, --color=green


```

# File types
```bash
-     regular file
d     directory
l     link
c     device file
s     socket file
p     named file
b     blockfile

```












