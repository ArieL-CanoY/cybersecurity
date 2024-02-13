Need to delete, rename, move, copy files and directories? Or you want to change the ownership of file/directory of your workmate to your name to mess things up? This is what you looking for.
#### Create, Copy, Delete, Move
```bash
mkdir [directory name] - make directory

cp [source directory and/or file] [destination directory and/or file] - copy file or directory

mv [source directory and/or file] [destination directory and/or file]  - move or rename a file or directory

rm [filename or directory name] - remove file

rmdir [directory name] - remove empty directory

rmdir -fr [directory with subdirectory] - remove non empty directory

rm -r [directory] - remove directory and files

rm [directory]/*  - remove all files in the directory

file [filename] - tell what file type of file a file or directory

     file letter.txt - tell what type of file is letter

     file * - tell all the file types of the current directory

touch [file name] - create a file, can be multiple files

ln -s [filename] [link name]- make a symbolic link

nano - used to edit text files and other editable, also create a file

```



#### File Permission, Ownership
```bash
chown [user:group] [file] - change the owner or group of a file 

chown [user:group] -R [directory] - change the user and group of a directory and all files inside it

chmod [permission] [filename] - change the permission of a file
	
	u - user - who owns the file
	
	g - group - who has group of the file
	
	o - other - other user except the user and group
	
	a - all user
	
	----------------------------------------
	
	- - subtract permission
	
	+ - add permission
	
	= - set permission
	
	---------------------------------------
	
	r - read permission
	
	w - write permission
	
	x - execute permission
	
	  ex.
	
		   chmod ug=w [filename] - set the user and group of a file to write only
	
		   chmod u+x [filename] - add the user of a file to execute it

		   chmod o-r [filename] - remove the read permission for other users
	
	-------------------------------------
	
	4 = read
	
	2 = write
	
	1 = execute
	
	  ex:
		  chmod 456 letter.txt - set the permission of user to read, group to read and execute, other is read and write of the file letter.txt


chgrp [group name] [filename]- change group owner of a file or directory
```
