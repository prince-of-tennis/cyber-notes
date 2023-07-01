IP addressing - logical L3 address (network) of [[OSI model]]
- think mailing address
- globally managed by IANA (Internet Assigned Numbers Authority) + RIRs (regional Internet registries)
- from [[IPv4]], we moved to [[IPv6]]

- automatically given out by [[DHCP]]

- types of addresses:
	- loopback (localhost) - traffic thru [[NIC]] but never make it to LAN, point is to check that internal [[TCP-IP]] path is working
		- IPv4: `127.0.01`
		- IPv6: `0:0:0:0:0:0:0:1`
	- [link-local](https://superuser.com/questions/342149/what-is-the-difference-between-a-link-local-address-and-an-ip-address-in-the-pri) - addresses allocated automatically to computer if DHCP fails them - has sep space so that it will not run into public, private IP's
		- IPv4: `169.254.0.0/16`
		- IPv6: `fe80::/64`
	- unique local - essentially [[IPv6]]'s version of private
	- private (like used in [[NAT]])