- cloud computing deployment models
	- private
	- community - several orgs
	- public
	- hybrid

- service models
	- SaaS - software as a service 
		- remote access to applications based on monthly or annual subscription fee
		- log in and just use it, not respon for maintenance
	-  PaaS - platform as a service
		- best solution for a web developer intending to create a web app?
		- you get the hardware and stuff, but have to develop yourself
	- IaaS/HaaS - Infrastructure as a service
		- responsible for mgmt/sec/data
		- ex: web service provider
	- XaaS - anything as a service
		- any IT function done as a service
		
![[cloud_models.PNG]]


- DaaS - desktop as a service - thin client
- FaaS - function as a service - just worry about web app, no worry about OS

- fog computing ("cloud btwn cloud and LAN") - operation of computing, storage, and networking services between end devices and computing data centers

- users use transit gateway to connect to [VPC](https://www.cloudflare.com/learning/cloud/what-is-a-virtual-private-cloud/) (virtual private cloud)
	- VPC is an isolated, private cloud inside public one
		- isolated thru use of 
			- subnets
			- VLAN
			- VPN
- SIAM (service integration and mgmt) - many diff service providers integrating together for single business
## security
- CASB (cloud access security broker) -  sheriff of cloud computing env
- CSA - nonprofit org promoting best practices related to cloud computing environments
- CCM (cloud controls matrix) - 

### comparisons of security
on-premises sec
- full control
- on-site IT team
- system check anytime, no need for phone calls
- security change can take some time

cloud sec
- no physical access
- 3rd party may have access
- cloud providers w large-scale security
	- users must follow sec best-practices
- limited downtime
- scalable sec options

## comparisons for data storage
- speed
- money
- security