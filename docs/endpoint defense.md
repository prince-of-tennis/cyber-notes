- antivirus/antimalware

- EDR (endpoint detection and response)
	- look at more than signatures to find malware
	- look at actions, then isolate threat

- DLP (data loss prevention)

- use of NGFW or host-based [[firewall]] like [[wf.msc]]

- HIDS (host-based [[IDS]])
	- log files, reconfigure firewall to block
- HIPS
	- recognize, block known attack
	- secure [[OS]], app configs
	- often built into endpoint protec software
	- see weird signatures
- [[boot integrity]]

- FIM (file integrity monitoring) - check the files that should never change
	- [[windows]] SFC
	- [[linux]] Tripwire