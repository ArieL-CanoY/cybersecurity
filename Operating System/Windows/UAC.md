# Definition
```python
- stands for User-Access Control
- User Account Control (UAC) in Windows is a security feature designed to prevent unauthorized changes to the operating system. These changes could be initiated by applications, viruses, or other users. When UAC is enabled, it ensures that changes to the system require approval from an administrator, thereby protecting the system from potentially harmful modifications.
```



# 4 Levels

#### Always Notify - Critical
```python
- At this highest level, UAC will always notify you when apps try to install software or make changes to your computer and when you make changes to Windows settings. This is the most secure setting and ensures that you are informed about every potential security risk.
```


#### Notify me only when apps try to make changes to my computer (default) - High
```python
- This level notifies you only when apps attempt to make changes to the system or when apps try to install software. It does not notify you when you make changes to Windows settings. This is the default setting in Windows and provides a balance between security and usability.
```


#### Notify me only when apps try to make changes to my computer (do not dim my desktop) - Medium
```python
- Similar to the default level, this setting notifies you only when apps make changes, but it does not use the secure desktop mode (which dims the screen). This setting can be useful if the dimming of the desktop is slow or causes other issues, but it is less secure because malicious software could potentially interfere with the UAC prompt.
```


#### Never Notify - Low
```python
- At this lowest level, UAC is turned off, and you are not notified when apps try to install software or make changes to the computer. This setting makes the system vulnerable to unauthorized changes and is not recommended unless you are confident in the security of your applications and the behavior of users on the system.
```






























