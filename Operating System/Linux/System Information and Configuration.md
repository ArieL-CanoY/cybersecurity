Need some information about the system your working at, or you want to elevate your privilege for illegal purpose, please don't.

# System Information
```python
who - current login user

users - users who logon to the current host

w  - show who is logon and what they are doing

hostname - name of the machine that current user log on

lsb_release -a - the information of the system like version 

uname -a - show system information like hostname, machine name, machine version, architecture (32 or 64 bit), OS

sudo -l - show the commands that current user can run

sudo -lU [username] - show the privilege of specificclear user

lscpu - information of the system cpu  

cat /etc/issue
cat /etc/os-release
cat /etc/release 

set - display and change shell variables

echo $0 - find the current user's shell if the environmental variable "$SHELL" does not exist
```

# Configuration

```python
~/bash_aliases     - configure aliases for shortcut commands 
	Ex.
		alias shut='shutdown 0' - typing shut will execute 'shutdown 0' command

- to work, use "source .bashrc" to refresh 


hostnamectl set-hostname [name of machine] - set the hostname of the machine
```

#### export path
```python
configure .bashrc:
	export $<name of path>=$PATH:/dir/dir...
		- add directory to $PATH variable

	export $<variable_name>="/dir/dir/dir..."
	export directory to use for other commands, or make an alias



```
















