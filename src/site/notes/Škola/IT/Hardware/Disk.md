---
{"dg-publish":true,"permalink":"/Škola/IT/Hardware/Disk/","created":"2024-02-05T19:24:38.985+01:00","updated":"2024-03-13T18:15:13.821+01:00"}
---

#Hardware #IT #Maturitní_otázka 
> [!Warning]
> Prý se budou ptát, co je to [světlo](Světlo.md)

Dělení:
- **Podle umístění**
	- Interní
	- Externí
- **Podle typu připojení**
	- [[Škola/IT/Konektory/SATA\|SATA]]1, [[Škola/IT/Konektory/SATA\|SATA]]2, [[Škola/IT/Konektory/SATA\|SATA]]3
	- [[Škola/IT/Konektory/PATA\|PATA]] (ATA, IDE)
	- [[Škola/IT/Konektory/M.2\|M.2]]
	- [[Škola/IT/Konektory/SAS\|SAS]] (Serverové rozhraní)
- **Podle typu disku**
	- SSD
		- Fyzická struktura
			- Skládá se z polovodičů - čipů
			- ==Žádná mechanická část -> vyšší rychlost==
			- Funguje díky [[Škola/Fyzika-Elektrotechnika/PN přechod\|PN přechod]]u
	- HDD
		- Fyzická a logická struktura pevného disku
		- ==Zápis probíhá elektromagneticky==
		- Fyzická struktura
			- Plotny
			- ==Ramínko se čtecí a zapisovací hlavou==
			- Řídící deska
			- Konektory
			- Vychylovací systém
		- Logická struktura
			- ==Stejná data nad sebou = cylindr==
			- Nultý sektor je zavádějící, následuje tabulka rozdělení disků a poté už data
			- Funguje pomocí **[elektromagnetismu](Elektromagnetismus.md)**
			- Souborový systém 
				- NTFS 
					- Jediný souborový systém, který uchovává práva a oprávnění
				- Exfat
				- FAT32
				- swap
				- ext4
	- SSHD
		- Klasický HDD, SSD uvnitř tvoří cache - vyrovnávací paměť