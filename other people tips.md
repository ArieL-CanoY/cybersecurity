In Linux hacking and exploitation, attackers commonly manipulate various files to gain unauthorized access or execute malicious activities. Some of the most common files targeted for manipulation include:

1. Configuration Files: Attackers may modify configuration files such as /etc/passwd, /etc/shadow, /etc/sudoers, or application-specific configuration files to escalate privileges, create backdoors, or modify access controls.
2. System Files: Critical system files like /etc/hosts, /etc/hosts.allow, /etc/hosts.deny, /etc/rc.local, or files under /etc/init.d may be tampered with to disrupt system functionality, enable remote access, or execute unauthorized commands.
3. Log Files: Attackers manipulate log files located in /var/log/ to cover their tracks and evade detection. They can delete or modify log entries to hide malicious activities or prevent forensic analysis.
4. User Files: User-specific files, such as ~/.bashrc, ~/.bash_profile, or ~/.ssh/authorized_keys, can be targeted to gain unauthorized access, install persistent backdoors, or steal user credentials.
5. Web Server Files: For web server attacks, files like index.php, .htaccess, or web application configuration files may be modified to inject malicious code, enable remote file inclusion, or perform other web-based attacks.
6. Executable Files: Attackers may replace legitimate executable files or modify their permissions to execute malicious code with elevated privileges or install persistent malware.
7. Network Configuration Files: Network-related files such as /etc/network/interfaces or /etc/sysconfig/network-scripts/ifcfg-* may be manipulated to enable unauthorized network access, modify routing tables, or intercept network traffic.




---
- Any command that runs with root privilege by a script, daemon, or init. I am not sure about what systemd does, but same likely applies.
- Any command that is suid or sgid root.
- Any file that modifies configuration for a command that runs with root privilege.
- Any file that changes how authentication works. For example, pam.conf can introduce a way to authenticate without a password.
- Any command that root users would commonly run.

  
There are too many such files and so a shortlist will not be helpful. The shell is one of them. ~/.ssh/authorized_keys is especially bad. The entire /etc should be read-only and monitored.

Ideally, the system should be locked down so hard that nothing can be written to disk. Tripwire must be deployed for production servers.

Here is an old exploit by yours truly [Pathetic hole in HP/UX 10.20 CUE](http://insecure.org/sploits/hpux.cue.pathetic.html "insecure.org"), complete with my teenage writing skills.