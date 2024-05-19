---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Hardware/","created":"2023-12-14T18:39:38.527+01:00","updated":"2024-05-16T11:24:22.434+02:00"}
---

**Je to hmotné technické aktivum**

# Dělení
- Vnitřní - Komponent
	- Např. [[Škola/IT/Hardware/Procesor\|Procesor]], [[Škola/IT/Hardware/Operační Paměť\|Operační Paměť]], [[Škola/IT/Hardware/Grafická karta\|Grafická karta]]
- Vnější - Periferie
	- Např. externí [[Škola/IT/Hardware/Disk\|Disk]]
# Komponenty
# Disk

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/hardware/disk/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




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

</div></div>

# Operační paměť

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/hardware/operacni-pamet/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- Má určitou kapacitu v GB nebo TB
- Má pracovní frekvence
- Jsou použity i v grafických kartách, jsou ale mnohem rychlejší - [[Škola/IT/Hardware/VRAM\|VRAM]]
- Normálně se nachází ==na základní desce==
# ROM

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




#Hardware #IT #SPOSDK 
# Druhy
- **ROM** -> Read-only Memory
- **PROM** - programovatelná, ale pouze 1x
- **EPROM** - E jako erasable, dá se naprogramovat a poté smazat pomocí UV světla
- **EEPROM** - stejná jako EPROM, ale dá se mazat pomocí elektrického napětí
- **CMOS** - zapisuje se elektricky, je na ní uložený [[Škola/IT/BIOS\|BIOS]], část paměti je readonly a další se zapisují hodnoty
- **FLASH** - novější verze CMOSu

</div></div>

# RAM

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




- Liší se podle toho, kde jsou použité (Desktop, laptop, server)
- jsou na ==bázi kondenzátoru==
- po vypnutí se z nich smažou všechny data
- ECC - ==dokáže opravovat chyby==
- **SDRAM**
	- DDR1
	- DDR2
	- DDR3
	- DDR4
	- DDR5

</div></div>


</div></div>

# Procesor

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/hardware/procesor/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- zpracovává úlohy, počítá
- **Dělení:**
	- **Podle umístění**
		- Integrovaný na základní desce
		- v matici
	- **Podle umístění pinů**
		- PGA (AMD)
		- LGA (Intel)
	- **Podle instrukčních sad**
		- RISC - redukovaná instrukční sada
		- CISC - kompletní
	- **Podle použití**
		- 32 bitů
			- méně efektivní
			- max 4 gb ram
			- starší technologie, dnes už se moc nepoužívá
			- může rozběhnout 16 bit software
		- 64 bitů
			- max 16 exabitů
		- ARM
			- Jsou hodně optimalizovaný
			- Hlavní využití v mobilních telefonech, embed zařízení (auta, spotřebiče)
			- úsporný na baterii

# Frekvence procesorů
- udává se v hercích
- určuje počet výpočtů za jednu vteřinu
# Multitasking
- možnost běhu několik různých procesů naráz
## Druhy 
- Preemptivní
	- OS řídí celý proces
	- Vyhradí procesu čas a při vypršení 
- Kooperativní
	- Program se domluví s OS (podle důležitosti)
	- Např. - antivirus si řekne o čas navíc, aby mohl provést důležitý sken systému
# Multi Threading
- Poddruh multitaskingu
- Jedno jádro má více vláken
- možnost ==dělat několik věcí naráz==
- Jeden proces se rozdělí na několik úloh (např. v jedné aplikaci naráz běží backend a frontend)
# Hyper Threading
- patentované Intelem, AMD používá "Simultaneous Multi-Threading"
- jeden procesor se rozdělí na několik logických procesorů
- Vlákna se chovají stejně jako jádra procesoru
- Optimalizuje využití procesoru
# AMD
- čipset napůl na desce
- jižní můstek na desce, severní na procesoru
# INTEL
- čipset na desce

</div></div>

# Grafická karta

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/hardware/graficka-karta/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- může být integrovaná na základní desce nebo dedikovaná
- Dělí se na:
	- grafický procesor
		- stará se o grafické výpočty
		- je to mozek GPU
		- stará se o komunikaci s grafickou pamětí
	- grafická pamět (VRAM)
		- úložiště pro zpracované data

# Výstupy
- vga - dnes se už moc
- HDMI
- Display port

# Chlazení
- aktivní
	- musí být napájené aby chladili
	- např. větrák
- pasivní
	- nepotřebuje napájení

</div></div>

# Základní deska

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




- Může mít integrovanou síťovou a zvukovou kartu
# Severní můstek
- připojuje CPU, GPU, RAM
- je velmi rychlý, rychlejší než jižní můstek
- poznávací znaky
	- má chladič
# Jižní můstek
- řadiče
- USB
- Síťová karta
- zvuková karta
- WiFi
- firmware
- PCI
- ISA

# Von Neumannovo schéma
**![](https://lh7-us.googleusercontent.com/q6dosps03cCR5Ds5nMJb_P-0_-CG0jATp5zv79nErYb6nrYj2V6sNpmqFVcCwi3FUCRp9QAJRy3otTn4H20c7g4tAjFDx6fN3DxWO9G3Bkd2hXFg38ES0USbq2z1lWC4iAfB8kgDgBw4DyG2wqUb-JE)**

# Harvardské schéma
**![](https://lh7-us.googleusercontent.com/0I53mHmBmb7VMGTDKxW5CZgyLlZIyVX28fcj7XUMxcJdjjZeKD_s-9angz4AQhIdtW1-Q9TxFFfnFRVGDRfl7cw7M6bsUXMneI1LHpzvRAfArgL7y8JPXWvshe9fJJlfpQb_8G_fD4o1THw9M3ZMI1k)**

</div></div>
