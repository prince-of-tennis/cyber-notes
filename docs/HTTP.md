(hypertext transfer protocol)
- used to load webpages on [[WWW]]

- HTTP (port 80)
	- messages are in plaintext

- HTTPS (port 443)
	- secure bc requires [[SSL-TLS]] cert from a certificate authority -> public-key encryption
		- CA-given certificate proves that this group owns a valid public key
	- also messages are encrypted
	- using https over http improves website authority
- http responses
	- 200 OK
	- 400 bad request
	- 404 resource not found

## methods
- GET - request info
- POST - client submitting info to web server
	- possibly dangerous -> sometimes disabled in [[RvB]]
- PUT - POST but idempotent
	- idempotent -> calling it multiple times has the same effect