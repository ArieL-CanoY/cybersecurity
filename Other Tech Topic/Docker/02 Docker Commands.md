
# Options
```python
-d   - detach the process to background so you can continue to type commands are running an image.

-p <portNum>   - specify the port number to run specific application especially websites.


```


# Get or pull an image
```python
>> docker pull <name of image>
```


# Run an image to be a container

### OS
```python
>> docker run -t -d --name <namingForImage> <OSimageNameDownloaded>
	- ex. "docker run -t -d --name buntu ubuntu"
	-t, --tty: This option allocates a pseudo-TTY (terminal) for the container. It allows you to interact with the container shell or run an interactive process within it. For example, if you want to run a Bash shell inside a container, you would typically use the `-t` option to allocate a TTY.

	-d, --detach: This option runs the container in detached mode, meaning the container runs in the background. Docker returns control to the terminal immediately after starting the container, allowing you to continue using the terminal for other tasks while the container runs in the background.


next is go inside the OS container:

>> docker exec -i -t <namingForImage> <shellUseToInteractWithTheOS>
	- ex. "docker exec -i -t buntu bash"
	- go inside the container OS and interact with it using the "bash" shell.


	-i, --interactive: This option keeps STDIN open even if not attached. It allows you to keep the container's STDIN open, even if you don't attach a terminal to it. This option is often used in conjunction with `-t` to create an interactive session with the container.	



```


### Application
```python
>> docker run -d -p <portBindToLocalhost>:<portBindToDockerContainerApp> user/application
	- ex. "docker run -d -p 8080:3000 bkimminich/juice-shop"
	- the application on the container running on port 3000 and can be visit from localhost to port 8080.

-p, --publish: This option publishes a container port(s) to the host. It allows you to map ports on the host to ports in the container, making services running inside the container accessible from outside. For example, you can use -p 8080:80 to map port 80 inside the container to port 8080 on the host.


```


# Stopping a container
```python
>> docker stop <namingForImage>
	- ex. "docker stop buntu"
	- stop the running docker
```

# Show running docker container
```python
>> docker ps
```

# Show all downloaded images
```python
>> docker images
```


# Removing an image























