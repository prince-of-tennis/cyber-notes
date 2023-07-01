- fuzz testing - automated code testing w random inputs to find zero-days or code faults 

- attacks
	- memory leak - where memory not returned to system
	- null pointer deref
	- integer overflow
	- directory traversal
	- improper error handling - having too much info in error messages
	- improper input handling
	- API attack
	- resource exhaustion - DoS that may only require one device and low bandwidth
		- e.g. ZIP bomb, [[DHCP]] starvation

- attacks
	- shimming - alter external behavior of app w/o changes to code
		- refactoring - change code w/o changing external behavior
			- metafactoring
		- sideloading - downloading an app w/o using the official install method
## app sec
- to find vulns
	- fuzz testing - automated code testing w random inputs to find zero-days or code faults 
- input validation -> normalization to fix weird stuff
- secure cookies
- [[HTTP]] secure headers
	- enforce HTTPS
	- only allow scripts, stylesheets, img from local site
	- prevent data from loading into iframe
- code signing - confirm it has not been changed
	- trusted [[CA]]
- allow/deny list