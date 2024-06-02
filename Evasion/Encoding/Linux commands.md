# Command execute using Base64 
```python
1. Encode the command you want to execute to a base64, type this on the terminal:
	echo -n "command_here" | base64
2. Use eval command that will evaluate the decoded base64 you encoded before:
	eval $(echo base64EncodedHere | base64 --decode)
```
































