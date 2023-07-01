domain name service

- translates domain names to [[IP]] addresses
- #1 cause of stupid connectivity issues in [[RvB]] bc windows/linux config files rely on it

- [[UDP]] 53 for queries for speed and bc its connectionless
- [[TCP]] 53 for zone transfers - when name servers exchange updated records 

- common DNS servers
	- google IPv4
		- `8.8.8.8`
		- `8.8.4.4`
	- cloudflare IPv4
		- `1.1.1.1`
- sometimes have DNS sinkhole so we know who's trying to go to malicious sites

recursive DNS
iterative DNS

- DNS record request (typing in a URL into browser)
	1. go to DNS recursive revolver (librarian), revolver makes additional requests
	2. goes to root nameserver
	3. goes to TLD (Top level domain) name server
		- hosts last portion of domain name, like `.com`

## attacks
- DNS cache poisoning / DNS [[spoofing]]
	- false info into DNS cache so that domain name goes to wrong IP
	- can be done thru
		- modifying DNS server
		- modifying client host file (takes precedence over DNS queries)
		- [[MITM]] - send fake response to valid DNS request

## security
- DNSSEC - validate DNS responses using public key [[crypto]]
- DNS resolve malicious site to sinkhole address
	- identify PC's infected w malware
	- this is essentially content filtering


