
Definition: [[Networking/Network Protocols/SMB|SMB]]



# Exploitation
After enumeration, use smbclient: [[smbclient]]
```python
>> smbclient //IP/sharename_with_ok_response_from_enum4linux
	or
>> smbclient //IP/sharename_with_ok_response_from_enum4linux -U anonymous 
	- anonymous login


>> once you are in the system, get any file by typing this command:
	>> get "sample_document.txt"
		!! note that you have to put the filename inside quote or else it will not found the object name

```


# Methodology
```python
> find workgroup name
> find OS information
> enumerate users
> enumerate sharenames
> map shares if they are available or with response "OK"

```
































