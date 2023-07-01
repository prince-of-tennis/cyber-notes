- can only have one ACL per protocol, per direction, and per interface
- made up of ACEs (access control entries)
- never act on packets that originate from router itself

- standard ACL - filter at L3 w source IPv4 address only
	- CLOSE TO DEST
- extended ACL - filter at L3 w src/dest IPv4, filter at L4 using TCP/UDP ports + protocol type info
	- CLOSE TO SRC

- router interface can have
	- one outbound IPv4 ACL
	- one inbound IPv4 ACL
	- one inbound IPv6 ACL
	- one outbound IPv6 ACL


- placement
	- **inbound** - when only 1 src network
		- packets processed before route determined
			- saves overhead of routing lookups if packet discarded
	- **outbound**
		- incoming packets routed to outbound int, then processed thru outbound ACL
		- 
- router processes ACL:
	1. 


## config
```
!! numbered standard

!! named standard

!! numbered extended
access-list 103 permit tcp 192.168.10.0 0.0.0.255 any eq 80

!! named extended
ip acc ex ACL_NAME
	permit tcp 192.168.10.0 0.0.0.255 any eq 80
	!! default deny any any
```