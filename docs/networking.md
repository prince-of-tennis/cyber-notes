- models
	- [[OSI model]]
	- [[TCP-IP]] model
	- [[cisco-3-layer model]]

- topologies - bus, star, mesh, hybrid
- [[devices]]
- through wired [[Ethernet]] or later, [[Wi-Fi]]
- how good is smth? -> [[network measurements]]

- tools
	- [[Wireshark]] to analyze traffic
	- [ping](ICMP.md)
	- [[netstat]]
	- pathping
	- tracert/[[traceroute]]

- SDN (Software -designed networking)
	- centrally managed
	- functions/abilities of devices defined by software
- SDV (Software-design visibility)
	- see the traffic to secure the data

## behaviors
### [[HTTP]] GET
- random port is used for client source port (ephemeral port)
	- sockets pair a port and ip address

### [[DNS]] query -> HTTP GET
1. user types in web address into browser -> browser requests IP of given domain name
2. host checks to see if [[DNS]] server on LAN
3. not on LAN, so forwards DNS query to default gateway
4. default gateway forwards it to DNS server
5. DNS server undergoes recursive DNS lookup
	- main DNS server queries multiple other DNS servers for the actual IP
6. DNS server forwards found IP to default gateway
7. default gateway receives it and forwards to original IP
	- knows the original host despite private address bc of PAT and use of ephemeral port
8. host now knows IP and sets up TCP connection w/ web server (on web server's port 80)
9. host can now send [HTTP GET request](https://support.google.com/chrome/a/answer/6271392?hl=en) to get webpage contents

- fundamentally syncronized w/ [[NTP]]

# connectivity?
1. basic stuff
	- default gateway not configured
	- L2/L3 port not on
	- [[DNS]] not configured correctly
	- does not have an IP
	- timeout (spam ping or change ping TTL)
	- pinged private IP not on network, dropped by router
	- [[ARP]] problem (? extremely rare)
2. [[VLAN]]
	-  trying to ping dif VLAN
	- wrong default gateway on VLAN
	- native VLAN mismatch
	- trunk not configured
	- VLAN not allowed on trunk
3. routing
	- default/static route goes somewhere weird
	- wrong/no network commands in dynamic routing
4. security
	- [[ACL]] rules

## vulns on os's related to networking
- on linux and Mac, check /etc/hosts.equiv file (trusted hosts file) - remote computers on that file can login to your computer without pass
- also check .rhosts file - holds host name and account name → trusted remote users