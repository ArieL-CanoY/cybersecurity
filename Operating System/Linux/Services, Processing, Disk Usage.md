Want to start, restart, stop a service like web service, remote access service, etc. and see what your computer processed? Here it is
#### Services
```bash
systemctl - control systemd system and service manager

systemctl [option(start,stop,enable,disable,etc.)] [service] - all about services

systemctl is-enabled [service] - check if the service is enabled so it can start (enable means start the service on startup

systemctl enable ssh

systemctl reload ssh - reload the configuration of a service without shutting the service down

systemctl restart ssh - reload the configuration of a service after shutting the service down

systemctl reload-or-restart ssh - reload the config of a service if possible, else restart

systemctl restart network-manager.service or service network-manager restart

systemctl list-units - list all application and system services
	arguments:
		--type, -t      can be service like --type=service or -t service
		--state     can be active or inactive like --state=active

service [service] [option(start,stop,enable,disable)]- run a system V init script

service apache2 start - start apache2 service for web 



python3 -m http.server 80 - start a web service on current directory using python

python3 -m SimpleHTTPSever 80 - same as the above






```



#### Processes
```bash
top - display linux processes

htop - display interactive process viewer

ps aux or ps -aux - snapshot the current service running of the system

ps -u [username] - show all the processes running on specific user

kill [process id] - send a signal kill to a process which has the id

kill -l - see all the signal options
	when using option 2 which is signint, then use kill -2 [process name]

pgrep [process name] - show the process id running from that process name

pkill [process name] - send a signal kill to a process which has the process name

free - amount of free and used memory in the system

2 types of processes:
foreground - a process that is running directly from the shell. You cannot do anything when this kind of process is running. You can get it to sleep or stop (using ctrl + z)
	
background - a process that is running from the background. You cannot do anything when this kind of process is running. You need to send it as a foreground by typing fg and to get it to sleep or stop (using ctrl + z) 

ctrl + z = put the current process to sleep mode where it stop

using bg and fg:
	- bg (option xNum if more than 2 process that sleep)
	- if there is more than 2 process sleep and use only bg, it will continue a process that has + sign on the right side of its process nubmer



```



#### Disk Usage
```bash
du - list the disk space of file of current working directory recursively

du -shc * | grep [string]- list the disk space of files of current working directory

df - show information about the file system on which file reside 
  
```


#### Storage/Partitions
```
fdisk -l  - manipulate disk partition table 
	-l         - list the partition tables for specific partition

gparted - GNOME Partition Editor for manipulating disk partitions.

lsblk - list block devices



```






