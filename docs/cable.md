- RJ45 is the name for the connectors on the ends of the Ethernet cables

- gigabit ethernet is full duplex

- signal strength drops over distance
- VGA


auto-mdix
- why standards
	- if frame goes from point A to B, may go over cables w diff capabilities
		- may be doing a lot of standards translating
	- but also everyone uses [[Ethernet]] frame so kinda okay

## types of cables
- twisted pair
	- modern [[Ethernet]] + telephone
		- 2 types
			- unshielded twisted pair (UTP)
				- most common kind
				- managed by IEEE as 802.3
			- shielded twisted pair (STP)
				- slight damage = a lot more electromag interf/crosstalk
				- more easily damaged than UTP
				- cost more → rarer
- coaxial - copper cable within insulator within copper shield
	- for higher frequency than twisted pair
	- technically faster than twisted pair
	- difficult to install/maintain bc of the layers
- [[fiber-optic]]
- what kind of [endings](https://networkengineering.stackexchange.com/questions/55017/whats-the-difference-between-serial-dce-and-serial-dte-link) do you use? (straight-through, crossover, rollover)
	- DTE - data terminal equipment 
	- DCE - data circuit-terminating equipment
	- DTE to DCE or whatever determines this
	
- referring to the pins at the end - these below are *all* copper
	- straight-through - pin order is the same to the other side
	- crossover - data input pins are now reversed to be data output pins
	- rollover/console cable - reverse pin order
		- reverse the pin order of each wire in a cable
			- if it rolled over, looks same
		- somewhat legacy bc used for RS-232 connectors for PC, printer, monitor serial ports

- [[wireless networking]]
	- most wireless devices are half-duplex bc a device's transmitted signals are generally much stronger than signals it receives
	- if need to transmit and receive at same time -> use dif frequencies

## how use
- typical net connection is PC-> switch -> router = all straight-through
- anything else is cross-over, as in any like devices as well (includes PC -> router)

## mgmt
- out-of-band mgmt
	- network isn't available
	- serial connection/[[USB]] port can be used -> connect a modem to manage device
		- sometimes have dedicated comm router/server that does this