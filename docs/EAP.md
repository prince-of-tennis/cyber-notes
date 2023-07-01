
types
- PEAP 
- EAP-TLS is most secure
	- EAP-TLS relies on both client-side and server-side certs for mutual auth
		- needs [[PKI]]
- EAP-TTLS
	- supports other auth protocols in TLS tunnel
	- only requires certificate on the auth server
- can use EAP w federation
	- often w [[RADIUS]] and 802.1x auth method
		- this is eduroam
