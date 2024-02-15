Hard to find files and directories on your linux machine? Used this and some of commands has an advanced searching



### Find command
```bash
find - find files or directory. ex. find -type [d-directory, f-file] -name [filename] 

	Flags and Switches (Options):
	
	   -type [f - files, d - directories, l - link, s - socket, ]
	
	   -name [*.txt - ends with .txt]
		   -iname   - ignore case sensitive name 
	
	   -user [name of owner or user of the file]

	   -group [name of group own of the file]
	
	   -size - 
	
			c - bytes, k - kilobyte, M - megabyte
	
			ex:
			
				find myfolder/ -size +2k

                    

		-perm - can use octal(643) or symbol(u=rwx)

		ex. for symbolic:

			o=x         - permission for other user is only execute. treat it as AND operator
						- ex. only match --x for other user permission
						- exactly executable only

			-o=rx       - permission for other user have at least have x, treat it as AND at least operator
						- ex. will match for other user permission: r-x, rwx
						- at least have read and execute permission

			/o=xr        - permission for other user has execute. treat it as individual/independent from other permission
						- ex. will match for other user permission: r--, rw-, rwx, r-x, --x, -wx
						- have execute OR have read permission

				
			ex. for octal:

				find -perm -415 - means find all files in the current directory who has at least read on the user AND execute on the group AND read and execute on the other user.
	
				find -perm /415 - means find all files in the current directory who has at least read on the user OR execute on the group OR read and execute on the other user.

	   TIME:

			- a - access, m - modified, c - changed

			- min - minutes, time - days

			- (-) - within or no more than, (+) - more than

			ex. find -type f -amin -30 - find files in the current directory that has been accessed no more than 30 minutes ago

		   - [commands with flags or switches] -exec [another comand] {} \;
			   ex. find / -name "*.jpg" -exec mv /home/user/allJPG

		  additional:
			-daystart       - search for files within the current day, starting from 12:00am


		-empty          - find empty files and directories
			ex. find / -empty      - files and directories, can be specific the -type (f, d)



```
	


### Grep command
```bash
 useful for piping (|)
 
grep - search for string in files. 
	ex. grep [string value to search] [file to search in]
		grep letter.txt 'take care'

		cat letter.txt | grep 'take care' - show the line with this string
		cat /etc/group | grep 'a' - groups with a on their letter
	
	
	options:
		-i      - ignore case sensitive
		-v      - match the pattern and exclude it
		-E      - treat pattern as Extended Regular Expression (ERE/ERegEx)
				- can be used as multiple pattern:
					- grep -E "pattern1|pattern2" file

```


### Locate Command
```bash
note: run updatedb first to update the index of database before running locate command

locate [directory] [filename/string] - locate any files on the computer (run updatedb first to update the database index or cache)

locate [filename/directory name] - 
locate [filename/string] | grep [directory] - improve searching for specific files on a directory

	-i - ignore case

locate -c [filename/directory] - count the number of result
```