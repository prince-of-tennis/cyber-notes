- security starts from hardware
	- [[TPM]] - helps w crypto functions (RNG, key gen)
	- HSM
- UEFI BIOS 
	- Secure boot verifies signature of bootloader
	- BIOS includes manufacturer's public key -> checked during BIOS update and boot

secure boot -> bootloader -> [[OS]] kernel -> other startup components (like ELAM - early launch antimalware)

- measured boot - uefi stores hash of firmware, boot drivers, anything trusted
- remote attestation to prove to verification server to check that everything is okay