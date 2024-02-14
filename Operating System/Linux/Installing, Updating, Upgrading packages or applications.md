You don't want to use older version of an application or package with security vulnerabilities and not updated huh? 

#### APT
- stands for Advanced Packaging Tool
```bash
apt - used to get update and upgrade packages

apt-get update - looking for the update of packages/files of applications in the repository

apt-get upgrade - upgrading or installing new packages/files after updating

apt-get full-upgrade - remove packages that are no longer needed for new upgrade

apt autoremove - remove packages/files that are no longer needed

apt remove [package] - remove an application package but not user data or config

apt remove purgew [package] - remove an application package together with user data or config 

apt install [package] - install a application using only their name if it has on the repositories specified.

apt --fix-broken install - fix the broken install cause by lack of dependencies

apt edit-sources - lets you edit the sources.list where the repository is specified.

apt list --installed - show list of packages/applications installed that has on repository

apt list --upgradable - show list of packages/applications that can be upgrade after update the packages

apt search [package] - search for a package in the repo if it has

apt show [package] - show the description of a package if it has on repo
f


options:
	-y - confirming yes without prompting the user if they will install, upgrade, upgrade, remove, etc...

	


```




# dpkg
- package manager for Debian.


```python
>> dpkg <file.deb>


	options:
		-i     - install a package
		-r     - remove a package

```





