If you want to remotely control other computer you authorized to control, do this or I will sniff your cable.
```bash
installing client and server services of openssh by installing the package openssh-[client or server] using apt-get install command
```


#### Directories for configuration
```bash
/etc/ssh/ssh_config - configuration file for ssh client

/etc/ssh/sshd_config - configuration file for ssh server

on sshd_config, configure it on authentication area and run systemctl restart sshd.service to restart the ssh and apply the configuration
```



#### Copying files from/to remote server using SSH 
```bash
From your pc to remote server - scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt

From remote server to pc - scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt

scp tryhackme@10.10.177.16:/home/tryhackme/"file from remote server" "file" "file to home"

From remote server to pc (both windows)

scp <filename/filepath> <your username>@<your ip address>:/<drive name>/<path>

scp -r myfolder <remote username>@<remote ip>:/path    - copy the directory and all of its files from local to remote machine

scp -r <remote username>@<remote ip>:/path /localPath   - copy the directory and all of its files from remote to local machine
```
