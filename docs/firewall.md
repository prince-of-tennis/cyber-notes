- overall purpose:
	- filter traffic
	- stop [[network attacks]]
- can be a "firewall device" (e.g. [[ASA]], but technically they do a lot more), but usually a "firewall service" (e.g. [[wf.msc]], [[iptables]], ufw, simplewall, tinywall)

- devices
	- WAF (web app firewall)- applies rules based on HTTP/HTTPS conversations
		- allow/deny based on expected input
		- specifically protects web apps
		- part of Payment Card industry Data Security Standard (PCI DSS)
	- UTM (Unified Threat mgmt)

## design/rule principles
- DENY ALL, allow only needed (like [[ACL]])
	- blocklist or allowlist?

## types of firewalls

- routed vs transparent modes
	- routed - shows as a hop in the network
	- transparent - invisible to attackers

- open-source vs proprietary
	- open-source more tradit features
	- proprietary has app control, purpose-built hardware
	
- hardware vs software

- appliance vs host-based vs virtual

- stateless vs stateful
	- stateless
	- stateful
		- most firewalls today
		- more easily DoS-able bc need for more computing

- tradit vs NGFW
	- traditional
		- stateful inspection incoming/outgoing
		- partial application control/visibility
		- L2-L4 only
		
		- cannot decrypt/inspect SSL traffic
		- integrated [[IPS]] and IDS are deployed separately
		
	- next gen (NGFW)
		- also known as application layer gateway, stateful multilayer inspection, deep packet inspection
		
		- stateful inspection on incoming/outgoing
		- comprehensive application control/visibility