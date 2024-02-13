--- This is default config ---

- config for aliases. startup
```python
	~/.config/fish/config.fish
```

- command history
```python
	~/.local/share/fish/fish_history
```


- syntax highlighting
	- invalid command and path turn color red
	- valid command and path turn color blue

- support wildcards
```python
	ls *.txt
```

- pipes and redirection
	- pipe - take output of the first command as input to the second command
	 ```python
		 echo 'hello in the world' | wc --words
	 ```

	- redirection - redirection any error to void 
	 ```python
		 find / -type f -name "*.txt" 2> /dev/null
	 ```

- autosuggestions

- tab completion

- variables
```python
	echo $PATH
```

- export shell variables

- command substitution
```python
	echo "we are in" (pwd)
```

- separating commands using semicolon
```python
	echo fish; echo shell 
```

- combiners using and, or, not in script

- functions in script








