## Pv4 history
- transition from classful to classless
	- **classful** - divides addresses into 5 groups
		- class A - network ID 8 bits, host ID 24 bits
			- 1st octet `10`
		- class B - network ID 16 bits, host ID 16 bits
			- 1st octet  `10`
		- class C - network ID 24 bits, host ID 8 bits
			- 1st octet  `110`
		- class D - multicast
			- 1st octet `1110`
		- class E - reserved for experimental
			- 1st octet `1111`
	- **classless** - uses variable-length subnet masking, replacing classful
		- 1993 CIDR (Classless Inter-Domain Routing)
	
- from IPv4 (1983) to IPv6 (1998)

### structure
- 4 octets of binary digits, represented in decimal 0-255
- [[subnet]]
- [[wildcard masks]]

### private/public IP's
- originally created to counter address exhaustion problem
- public - can be accessed directly over the internet
- private - only exists w/i local network
	- packet w/ private IP destination will be dropped by routers
	- reserved blocksw
		- class A: 10.0.0.0/8
		- class B: 172.16.0.0/12
		- class C: 192.168.0.0/16

- translation from Public -> Private, vice versa thru [[NAT]]
	- NAT breaks legacy protocols/services relying on end-to-end IP traceability
	- ran out of IPv4 addresses on 11/25/2019