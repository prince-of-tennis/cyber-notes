(dynamic host config protocol)

- assign [[IP]]'s, default gateways, [[DNS]] servers, domain names to hosts
- can be assigned in 3 ways
	- manual - user sets IP, DHCP server forwards it to PC
	- automatic - DHCP server picks from pool, assigns it to PC permanently
	- dynamic - DHCP server picks from pool, assigns it to client for a lease time

- relay agent can be any [[TCP-IP]] host, used to forward requests/replies from server to device in another LAN
	- will receive DHCP msg and generate new msg to send out on another interface
	
### on cisco, maybe APIPA
- if DHCP fails, goes to APIPA
	- APIPA - device self-configures IP/subnet when DHCP server not reachable
	- uses range 169.254.0.1-169.254.255.254 with subnet 255.255.0.0

## DHCP behavior
- lease origination (DORA)
	1. **DHCP DISCOVER** (ethernet broadcast 255.255.255.255)- client boots up w/o IP and sends msg on subnet to find DHCP servers
		- if router present and config to be BOOTP relay agent, request passed to DHCP servers on dif subnets
		- broadcast includes client ID (generally [[MAC]], but can be overrided to be smth else)
	1. **DHCP OFFER** - broadcast w client ID to inform client of an IP
	2. **DHCP REQUEST** (subnet broadcast) - client confirm address and requests addit. info
	3. **DHCP ACK** - unicast to client after IP is verified
		- DNS server IP, domain name, lease time also given here

- lease renewal
	1. **DHCP REQUEST** (unicast) - client to server, asking for lease renewal
	2. **DHCP ACK** (unicast) - server verifies lease

- if DHCP server receives invalid or unsupported request (no more addresses in pool), will send **DHCPNAK** response to client
- when lease expires
	- clients sends **DHCPRELEASE** to tell server that address can be redistributed

## attacks
- DHCP starvation attack (done w [[MAC]] [[spoofing]])
	1. attacker spams a server w spoofed source MACs to use up its pool
	2. attacker sets up their own rogue DHCP server (DHCP spoofing)
		- usually the attacker will set up their server to try to be the DNS server
-> cred harvesting for NetNTLM [[hash]]
- when victim tries to reach a url, and attacker replies with IP of its own host
	- victim sends [[HTTP]] request
	- attacker returns HTTP 401 (unauth response) which starts auth process
		- attacker gets NetNTLM hash

- mitigate w DHCP snooping (which is rlly just logging)

## security
- DHCP snooping - DHCP only allowed on trusted ints
	- i.e. DHCP messages shouldn't be coming from ports that should be only leading to workstations
- in [[AD]], DHCP servers have to be authorized

