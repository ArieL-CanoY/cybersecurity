 


#### SNMP - Simple Network Management Protocol
- used to collect and organize device information in a network 
	- monitor the device's network bandwidth, CPU usage, temperature, up time status, etc.
	- used UDP 161
	- a device that enables SNMP is called agent
	- MIB stores all the information or the object of the agent
	- to interact with the object, it needs NMS (Network Management System) - piece of software that can communicate with the SNMP agent
	NMS speak to the agent by using:
	  Get Request - used to request information from an SNMP agent:
			- Get
			- GetNext
			- GetBulk
	  Set Request - used to change the value of SNMP object on the device:
	  Trap/Inform - SNMP agents can actively notify us by using Trap or Inform messages. Both do the same thing but only Inform messages are reliable.


#### 