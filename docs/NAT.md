- network address translation - meant to address problems of running out of IPv4 address space

- inside/outside - (**literally**) which device is being translated by NAT or is the destination
- local/global - (**perspective**) - inside/outside network - is it local to you?

- inside local - source address seen from inside network (gen. private IPv4)
- inside global - source address seen from outside network (gen. globally routable IPv4)
- outside local - dest address seen from inside network (gen. globally routable IPv4)
- outside global - dest address seen from outside network (gen. globally routable IPv4)
	- if it ever asks about an outside host ip, assume its this one

- NAT64 translates IPv6 to IPv4, no private/public address translation

## types of NAT
- static NAT - one-to-one mapping of local and global addresses
- dynamic NAT - pool of public adds -> assign on queue basis (if run out of addresses -> next request fails)

- PAT (Port Address Translation/NAT overload) - mult. private IPv4 to few/single public IPv4 
	- done w src port numbers from TCP/IP session (port nums added to inside global adds) or smth else if packet doesn't involve TCP/UDP (e.g. ICMP uses Query ID)
	- may not translate to original port at the router bc it may already have been used -> uses next available port
	- most home routers, small businesses
		- doesn't need enough public adds for total user sessions

- [[port forwarding]] - one public IP w port numbers representing different devices in LAN

## Behavior
- dynamic
	- inside to outside - router receives packet (`ip nat inside`) from inside network
		1. check the associated ACL, is it permitted? -> yes, need to translate
		2. check NAT entries -> no entry so needs to be translated
		3. uses next available add in pool and creates translation entry
		4. replaces inside local address w new inside global address and forwards packet to outside network
	- outside to inside - router receives packet from outside network (`ip nat outside`)
		1. when receive packet, does NAT table lookup
		2. forwards it to inside PC

## problems
- still ran out of addresses anyways
- geographical distribution (50% of used IP's in US)
- use of NAT breaks end-to-end onnectivity
	- NAT [breaks](https://web.mit.edu/6.033/2002/wwwdocs/papers/what-nats-break.html) so many things including
		- [[IPsec]]
		- [[Kerberos]]
		- kinda [[VPN]]s