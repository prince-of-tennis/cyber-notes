- [[SIEM]] to centralize logging
- commonly use the [[syslog]] standard

- log rotation - you clear logs when it gets to a certain pt, start logging again from top of log file
	- using `head` tells you if log rotation is properly implemented

## linux logging
- `logger "backup started"`
	- add timestamped entry
- `journalctl --list-boots`
- `journalctl --since "1 hour ago"`

## windows logs
- security log - security, audit, access -> s/f
- system
- application