## components
- everyone has [[NIC]]
- [[CPU]]

## behavior of all devices
- switch boot sequence
	1. switch loads a power-on self-test (POST) program stored in ROM
		- POST checks the CPU subsystem. 
		- tests the CPU, DRAM, and the portion of the flash device that makes up the flash file system
	2. Switch loads the boot loader software stored in ROM
	3. Boot loader performs low-level CPU initialization
	4. boot loader initializes the flash file system on the system board
	5. boot loader locates and loads a default IOS operating system software image into memory and gives control of the switch over to the IOS

- end device boot sequence on 1st startup
	- boot from HD or SDD or [[USB]] drive
		- device must request address if network interface is up ([[Ethernet]] or W[[LAN]]) -> [[DHCP]] Discovery 

## network devices
- [[routing]]
- [[switching]]
- modems - modulation/demodulation legacy device -> meant to port data onto Internet thru telephone lines/existing infrastructure
	- converts digital data to analog radio/telephone/etc signals, vice versa
	- modern devices still all have some sort of modem (wifi convert digital to analog to transmit)

## end devices