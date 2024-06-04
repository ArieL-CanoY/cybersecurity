
# Definition
```python
- stands for Content-Security Policy
- additional control that the server set
- meant for the browser to prevent XSS payloads from being rendered on the client.
- an example of HTTP header
- set via HTTP header, by the web server, for the browser to enforce.
- controls what resources (scirpts, styles, images, etc.) a browser is allowed to load and execute on a web page.
```



# Header format
```python
Content-Security-Policy: default src 'self' *.trusted.com
```



# Implementation
```python
>> You can configure your web server to have a CSP HTTP Header

>> Alternative is by using a meta tag on HTML:
	<meta
	  http-equiv="Content-Security-Policy"
	  content="default-src 'self'; img-src https://*; child-src 'none';" />
```



# Defense types
```python
>> can create CSP rules to the following:
	- default
	- script
	- style
	- image
	- font
	- connect
	- media
	- object
	- frame
	- report
```



# Bypass
```python
>> use whitelisting bypass using wildcard "*" where you can load script from any subdomain of specific domain: *.amazonaws.com, by this, you can create subdomain, insert a malicious script to that subdomain, and load it from the target web server.
```







# Websites
```python
>> cspisawesome.com/content_security_policies
	- generate CSP HTTP header rules

>> report-uri.com/home/generate
	- see the CSP rules of specific domain

>> 
```

















