- network interface card/network adapter
	- laptops generally have 2+ ([[Wi-Fi]], [[ethernet]])
		- generally built in now, but used to be plug-in (needed to install corresponding drivers manually)
	- each NIC has
		- speed rating - 10 Mbps, 100 Mbps, 1000 Mbps, 1 Gbps
		- driver software - software to pass data btwn [[OS]] and NIC
		- MAC address
	
- a bunch of these on a router
	- each router port has a NIC, each port is thus associated w a [[MAC]] address

- note
	- the dest mac add of a packet **changes** 
	- dest [[IP]] of packet never changes

- to show NIC on:
	- [[windows]] `ipconfig /all`
		- shows up as “Ethernet adapter local connection” for wired network or “ethernet adapter wireless network connection
	-   Mac OS X `ifconfig`
		- shows up as “en0, en1...” for each NIC in your computer
	- [[Linux]] and Unix `ifconfig`
		- shows up as “en0, en1...” for each NIC in your computer 