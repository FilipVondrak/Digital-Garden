---
{"dg-publish":true,"permalink":"/Škola/IT/Hardware/Procesor/","created":"2024-02-05T19:17:03.331+01:00","updated":"2024-03-13T18:14:35.318+01:00"}
---

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