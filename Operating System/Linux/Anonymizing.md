So you want to become abnonymous/banonymous to become famous huh? Install it quick!

#### Installing
```python
install tor and proxychains via sudo apt install
```


[[Bash Shell]]
#### TOR
```python
	sudo systemctl enable tor.service - enable the tor service
	
	sudo systemctl start tor - start the tor service (otherwise change start to stop)
  
```



#### Proxychains
```python
/etc/proxychains.conf - configuration file

	add proxy server like this:

		[type] [ip address] [port] [username option] [password option]

  

	use proxychains like this:
	
		sudo proxychains [application] - use the application while using the proxychains
```

