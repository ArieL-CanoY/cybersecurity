### Problem
```python
The installation says the computer is not compatible to install windows 11 using ISO file from windows to VirtualBox.
```

### Fix 
```python
1. In the page of typing the activation key, press Shift + f10 and cmd will show up.
2. Type regedit and registry editor will show up.
3. Go to HKEY_LOCAL_MACHINE > SYSTEM > SETUP.
4. Create new folder called "LabConfig" under SETUP folder. The name is case sensitive.
5. Right click the that folder and create new 32 bit value called "BypassTPMCheck".
6. Right click the that folder and create new 32 bit value called "BypassSecureBootCheck".
7. Double click each one and set their value to 1.
```



















