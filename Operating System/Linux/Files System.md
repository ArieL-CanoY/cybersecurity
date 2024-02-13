So you need more information about the linux file system, where you can find specific files and directories huh? Here you go
```bash
/etc - system configuration

/var - logs

/root - home of root/admin user

/tmp - temporary file. Any user can access this file. Best for uploading scripts and malware

/usr/bin - shell commands, binary file of system commands

/home - directory of all users other than root

  

/etc/passwd - list of user info

/etc/shadow - list of users password

/etc/group - list of all user group

/etc/sudoers - file for users permission configuration (same as running "sudo visudo" command if the users has a sudo group or a root user)

/etc/rsyslog.conf - All system and kernel messages get passed to rsyslogd. For every log message received Rsyslog looks at its configuration file, **/etc/rsyslog.conf** to determine how to handle that message.

/etc/logrotate.conf - handles the logging storage

  

/var/log/apache2 - access and error logs

/var/log/fail2ban - for anti bruteforce

/var/log/ufw - for firewall

/var/log/user.log - log of users
```