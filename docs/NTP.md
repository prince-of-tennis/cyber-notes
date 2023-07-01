network time protocol

- works by defining an authoritative NTP source (ex: time.gov)
	- given stratum 1
- every hop out is +1 stratum
	- network devices take most trustworthy stratum

- classic NTP had no sec features -> NTP DDoS attacks
	- NTPsec in 2015