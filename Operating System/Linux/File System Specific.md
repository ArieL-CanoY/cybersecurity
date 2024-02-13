# /
```python
- The top-level directory is the root filesystem and contains all of the files required to boot the operating system before other filesystems are mounted as well as the files required to boot the other filesystems. After boot, all of the other filesystems are mounted at standard mount points as subdirectories of the root.

```

# /bin
```python
- link to /usr/bin which is everyday user's command

- Contains essential command binaries.
```


# /boot
```python
- Contains file that is used by the bootloader (grub.cfg)

- Consists of the static bootloader, kernel executable, and files required to boot the Linux OS.
```


# /dev
```python
- System devices (e.g. disk, cdrom, speakers, flash drive, keyboard etc.)

- Contains device files to facilitate access to every hardware device attached to the system.

```

# /etc
```python
- system configuration files
- This root directory is one of the most important root directories on your system. The etc folder (short for etcetera) is a commonplace location to store system files that are used by your operating system. 

For example, the sudoers file highlighted in the screenshot below contains a list of the users & groups that have permission to run sudo or a set of commands as the root user.

Also highlighted below are the "**passwd**" and "**shadow**" files. These two files are special for Linux as they show how your system stores the passwords for each user in encrypted formatting called sha512.


- Local system configuration files. Configuration files for installed applications may be saved here as well.

```

# /home
```python
- all user's directory other than root

- Each user on the system has a subdirectory here for storage

```


# /lib
```python
- link to /usr/lib
- C programming library files needed by commands and apps

- Shared library files that are required for system boot
```

# /media
```python
- For cdrom Mounts

- External removable media devices such as USB drives are mounted here.
```


# /mnt
```python
- To mount external filesystems

- Temporary mount point for regular filesystems.
```


# /opt
```python
- Optional add-on applications (Not part of OS apps)

- Optional files such as third-party tools can be saved here.

```

# /proc
```python
- Running Processes (Only exit in Memory)


```



# /root
```python
- superuser's home directory or the root user's home

- Unlike the **/home** directory, the **/root** folder is actually the home for the "root" system user. There isn't anything more to this folder other than just understanding that this is the home directory for the "root" user. But, it is worth a mention as the logical presumption is that this user would have their data in a directory such as "**/home/root**" by default.

- The home directory for the root user.

```


# /run
```python
- System daemons that start very early to store PID files


```


# /sbin
```python
- System/Filesystem Commands

- This directory contains executables used for system administration (binary system files).
```

# /srv
```python
```
# /sys
```python
-


```



# /tmp
```python
- Directory for temporary files needed by commands and apps

- This is a unique root directory found on a Linux install. Short for "temporary", the /tmp directory is volatile and is used to store data that is only needed to be accessed once or twice. Similar to the memory on your computer, once the computer is restarted, the contents of this folder are cleared out.

What's useful for us in pentesting is that any user can write to this folder by default. Meaning once we have access to a machine, it serves as a good place to store things like our enumeration scripts.

- The operating system and many programs use this directory to store temporary files. This directory is generally cleared upon system boot and may be deleted at other times without any warning.

```

# /usr
```python
- Contains executables, libraries, man files, etc.
- 

```




# /var
```python
- System Logs

- This directory contains variable data files such as log files, email in-boxes, web application related files, cron files, and more.
```


# /var/log
```python
- The "/var" directory, with "var" being short for variable data,  is one of the main root folders found on a Linux install. This folder stores data that is frequently accessed or written by services or applications running on the system. For example, log files from running services and applications are written here (**/var/log**), or other data that is not necessarily associated with a specific user (i.e., databases and the like).


```


























































