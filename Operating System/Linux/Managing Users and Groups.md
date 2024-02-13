Need to delete, add, change username, change group name, print name/group name and directories? Or you want to mess up other users? Look at below
### Users:
```python
>> whoami - print current username

>> adduser [options] [new username ] - add user with guide of setting up the new user

>> useradd  [new username ] - add user without home directory and no password

>> useradd -m [new username ] - add user with home directory

>> useradd -s [location of shell] [new username]

>> usermod -l [new username] [existing username] - rename a user (does not rename the home name and should change the its directory using usermod -d)

>> usermod -d [home directory] [username] - set the default home directory of a user

>> usermod [username] --shell /bin/[type of shell like sh, bash, zsh] - change the shell type of a user. See also the command "chsh" in Shell folder/topic.

>> mkhomedir_helper [username] - create home directory for existing user without home directory (not working lately)

>> passwd [username] - create or change password of a user (leave blank for current user)

>> userdel -r [username] - removing user with its home directory

>> deluser --remove-home [username] - same as above

```
    
  
### Groups:
```bash
groups - print current group of user

groups [username] - print groups of the specify user

groupadd [groupname] - add a group

groupdel [groupname] - delete a group

usermod -G [groupname] [username] - set the group of a user

usermod -aG [groupname] [user] - add a group to a user

gpasswd -d [username] [groupname] - delete a user in a group

groupmod -n [new group name] [existing group] - rename a group

```



### Switching Users
```bash
su - switch as the root user only and stay on the current directory

su - - switch as the root user and go to its home directory

su - [username] - switch for specific user and go to the user home directory 

su [username] - switch for specific user and stay in the current directory

su [username] -c "[command]" - execute a command pretending you are that user

```


### Sudoers file

#####    User section
```bash
[username] [sessions: tty(local machine) or remote]=([username]=[group name]) [option command, can be all] - parts of privilege specification
	
[username] (ALL=ALL) - give all sudo permission with password
	
[username] ALL=NOPASSWD:ALL - give all sudo permission without password
```

#####    Group section
```bash
%[groupname] [same as username above]- same above
```



# other 
```python
>> sudo -u <user> <command>
	- execute a command on behalf of another user
	- you need to have a sudo privilege to execute this (common sense because it has sudo on it).

```