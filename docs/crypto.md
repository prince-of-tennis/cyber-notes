- deterministic encrypt -  same c for a given pt and key
- probabilistic encrypt - encrypting same pt multiple times gives dif c

- can use nonce to add a random factor to encryption
	- e.g. Initialization Vector
	- salt is associated w password [[hash]]ing

luv [[RSA]]

[[PFS]]

- digital signatures
	- integrity
	- auth
	- non-repudiation

- key stretching done w
	- Bcrypt - based on blowfish
	- PBKDF2 - used by [[WPA]]2 and iOS

## encryption
- homomorphic encryption -> ciphertext can still be used and worked with as if plaintext
[[symmetric encryption]]
[[asymmetric encryption]]

## ciphers
- stream - enc done one bit or byte at time
- block - block done at a type (usually 64 or 128 bit)
	- block cipher modes
		- ECB - use same key for each block
		- CBC (cipher block chaining) - each block XORed w previous block + add random IV
		- CTR - ECB but key is a counter
		- GCM - enc w auth
			- seen in [[IPsec]], [[SSH]], [[SSL-TLS]]
