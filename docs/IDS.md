Intrusion Detection Service - watch network traffic
- [[IPS]] can actually block stuff


- passive monitoring can be done w 
	- port mirror (SPAN), network tap
	- cannot actually block traffic
		- will do out-of-band response by sending [[TCP]] RST frames
			- shuts down traffic flow after the fact
			- this only works for TCP
- in-line monitoring - IDS/IPS can actually block


- identification technologies
	- signature-based - is this a match w XYZ?
	- anomaly-based - does this deviate from normal?
	- behavior-based - is this behavior weird?
	- heuristics - use [[ML]]

