- Internet Control Message Protocol - L3, primarily used for error-reporting
	- not associated w TCP or UDP - connectionless
	- cannot target a specific port
- ping sends ICMP echo request packets
	- hosts reply w ICMP echo reply packets

- windows ping sends 4 echo requests, while linux ping sends continuously
	- linux (cont) on windows: `ping -t 192.168.1.1`
	- windows (4) on linux: `ping -c 4 192.168.1.1`

- kinds of ICMP messages
	- 0 - time exceeded
		- traceroute uses this one to get its data back to sender
	- 3 - destination unreachable
	- 8 - echo request
	- 9 - router advertisement
	- 10 - router solicitation
	- 11 - time exceeded