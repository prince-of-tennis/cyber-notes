- digital forensics and incident response
	- cypat forensics like digital forensics, the rest is like IR

- NIST 6 stage IR process
	1. prep - plan, staffing, software
	2. detect - [[SIEM]] tools in conjuction w [[ISP]], police etc
	3. analysis - logs
	4. containment - [[C2]] infra, lock down [[ports]], physically air-gap
	5. eradicate/recovery - bsuiness continuity, disaster recovery
		- reinstall [[OS]], software
		- put back in backups
		- audit user accts
		- run [[vuln]] scan
	6. post-incident activity - debriefs/reviews

- types of disaster recovery site
	- hot - fully functional + immediate recovery from disaster
	- warm - no prod work until disaster
		- equipped site w no customer data
	- cold - infrastructure to support IT, but not actual tech