```python
ping          - send ping or echo request to show if a device on a network is reachable

tracert       - show route of a packet to different routers on the internet

ipconfig     - show network configuration setting

netstat       - how current connections or active connections

     options:

          -a     - all connection include close and wait

          -b     - connection and the name of application

nslookup     - information about dns server and resolve ip address of domain name

netsh wlan show profile     - show wifi that has been connected before

shutdown [options]     - shutdown the computer

     options:

          /s             - shutdown completely the computer     

          /t [num]    - timer the command of shutdown in seconds

          /r             - restart or reboot

          /a            - abort the countdown 

sfc          - system file checker

     required arguments:

          /scannow          - scan the file system and repair it when possible

tasklist          - list the task running on the background

taskkill          - kill a task by using their name of Process Id (PID)

          required arguments:

               /im [name of .exe]          - kill a process using the name of application including .exe on its name

               /pid [pid of an app] /t      - kill a process using the PUI of an application including the its child process

copy [existing file] [new filename to rename or directory to move]          - copy single file or directory

     options:

          /v          - verifies that new files are written correctly

          /y          - prompt to confirm that you want to overwrite an existing destination file

xcopy [existing directory] [new directory name or existing directory]         - copy all contents in a folder to another

robocopy [existing directory] [new directory name or existing directory]     - same as xcopy but more information it provides

del          - delete a file

rmdir        - delete a directory

start/explorer .     - open the current directory


# get the hash value of a file
	certutil -hashfile (filename.extension ex. zuma.exe) (encryption type ex. sha1, sha256, sha2)
	


```


# System information
```python
>> systeminfo
	show informations about the system


```











