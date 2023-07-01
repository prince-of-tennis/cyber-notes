- full backup
- incremental backup - only back up changes since last *incremental* backup
- differential backup - backup changes since last *full* backup

- media
	- magnetic type 100 GB to multiple TB
		- easy to ship and store
	- disk
		- faster than magnetic type
		- can do deduplicate/compress
	- copy

- NAS vs SAN
	- NAS (network attached storage)
		- file-level access -> will need to overwrite entire files
	- SAN (Storage Area Network)
		- block-level access -> cjust change portion of disk

- maybe cloud
	- limited by bandwidth

- can backup image

- locations
	- offline -> to local devices
	- online -> remote connected third-party thru encrypted channels
		- also accessible, requires good bandwidth