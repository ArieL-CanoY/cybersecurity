#### Configurations in Apache web server

# ------- NOTE -------
#### if it has an existing tag, that only one will work, it cannot duplicate again: example there is:
	<Directory "/">
		some config here
	</Directory>

#### you cannot make another one of that, put the config on that one only to make it work.

# --------------------- 

filename: httpd.conf or .htaccess
```python
>> Options -Indexes
	- will deny listing all folders and files in a browser - returns forbidden.

>> Signature Off
	- it will hide the x-powered-by which return the php version it used.

>> ServerTokens Prod
	- provide minimal information about the server - it will hide the version of the apache and operating system running on it but not the apache server.

>> ServerSignature Off
	- provide no information about the server.

>>
<Files "^.ht*">
    Require all denied
</Files>
>>
	- prevent users to access .htaccess (config files) and htpasswd (authentication) on the webserver if exist even not.

>> AccessFileName .htaccess
	- the name of file to look in each directory for additional server configurations.o

>> AddType application/pdf .pdf     or
>> AddType application/x-httpd-php .php
	- adding the MIME-type and the extension name
	- meaning execute the file as pdf when it has extension of .pdf, and execute the file as php when it has filename extension of .php
	- you can also use this:
		<FilesMatch "\.aa$">
		    SetHandler application/x-httpd-php
		</FilesMatch>




```

# htpasswd - for authentication
- the htpasswd.exe is located on (installation folder)\\apache\\bin\\htpasswd.exe. You can import the path (installation folder)\\apache\\bin in the windows environmental variable to run htpasswd anywhere in command prompt.


```python
- to add a file with user credentials, type this:
	htpasswd -c "<dir>/<dir>/<dir>/<new_filename>" <username>

	-c - create a new file

	- this will prompt the user to create a password.

- You can configure .htaccess on the folder you want to secure or go to httpd.conf and add <Directory "<location of website directory>" then add configuration. Update: make .htaccess for 100% working.

Configurations:

AuthType Basic
AuthName "<name of the pop up message/notif>"
AuthUserFile <location of the .htpasswd or the file you created>
Require valid-user
```

# Authentication Types

#### Basic
```python
- an authentication scheme that a client can authenticate using a username and password.

```


#### Digest
```python

```








