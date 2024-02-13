general command
```
system-view/sy - go to system view where user can configure the device
q - quit the current view/subview
```



router configuration
```
[r1]<interface/int> <interface (e/eth/Ethernet)/(g/GigabitEthernet)/(s/Serial) <interface number (0/0/n)>


[r1-Serial0/0/1]ip address 192.168.1.1 (24/255.255.255.0)

[r1]ip route-static 192.168.1.0 (24/255.255.255.0) 192.168.10.2

[r1]display ip routing-table

[r1]disp




```


shortcut command:
```
system - sy
interface - int
display - dis
GigabithEthernet - g - ex: int g0/0/1
Ethernet - e - ex: int e0/0/0
Serial - s - ex: int s0/0/3
255.255.255.0 - 24 - ex: ip address 10.0.0.1 24
save - sa
quit - q

ip ad(tab) - ip address
ip ro(tab)-(tab) - ip route-static
dis ip ro(tab) - dis ip routing-table

```













