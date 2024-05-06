---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/IoT (programování, bezpečnost a jednotlivé části IoT)/","tags":["IOT","Maturitní_otázka","SPOSDK","Software"],"created":"2023-12-19T09:11:24.192+01:00","updated":"2024-05-06T09:44:12.413+02:00"}
---

## Definice
-> **Internet of things** (internet věcí)
- síť ==chytrých fyzických zařízení==
- vzdálený přístup
- zařízení spolu mohou spolupracovat
- zařízení mají integrované **senzory** (např. na zvuk, jas, atd.), software a konektivitu
- potřebuje přístup k síti
- sběr a výměna dat mezi zařízeními
___
## Příklady
- Chytrá žárovka připojená k [[Wi-Fi\|Wi-Fi]], kterou lze ovládat dálkově mobilem/hlasem
- Chytré kamery připojené k [[Wi-Fi\|Wi-Fi]], ke kterým se dá vzdáleně připojit

___
## IoT zařízení
- [[Arduino\|Arduino]] - 8bitů
- [[Raspberry Pi\|Raspberry Pi]]
- **Nositelná elektronika**: 
	- Chytré hodinky 
	- fitness náramky 
	- chytré oblečení
- **Domácí spotřebiče** 
	- Chytré ledničky, pračky 
	- termostaty 
	- osvětlení
- **Průmyslové senzory**
	- Monitorování strojů 
	- výrobních procesů 
	- environmentálních podmínek
- **Automobily** 
	- Konektivita 
	- autonomní řízení 
	- diagnostika
- **Zdravotnické pomůcky**: 
	- Monitorování pacientů
	- diagnostika
	- telemedicína

___
## Z čeho se skládá Raspberry Pi
### [[Škola/IT/Maturitní otázky/Programování/GPIO\|GPIO]]

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



 - piny, vstup a výstup 
	- 2 typy pinů
		- Digitální - 1 a 0
		- Analogový - vrací hodnotu přes velikost napětí (0-255)

</div></div>

### Konektivita 
- [[Bluetooth\|Bluetooth]] 
- [[Wi-Fi\|Wi-Fi]]
- [[Ethernet\|Ethernet]]
- [[Škola/IT/Konektory/HDMI\|HDMI]]
### Úložiště 
- slot na paměťovou kartu 

___
## Chytré města
- soběstačná města
- metropolitní síť, řídí např. tepelné ztráty
- kamerový systém
## Chytrá domácnost
## Chytrý dům
## Chytrá ulice

___
## Ovládání IoT
### Aplikace na webu
### Aplikace v telefonu
___
## Programování IoT
- liší se od klasického programování v několika způsobech:
	- **Omezené zdroje**
		- mají omezenou paměť, výpočetní výkon a energetickou kapacitu
		- vyžadují dobrou optimalizaci
	- **Bezpečnost**
		- Zabezpečení dat a ochrana proti kybernetickým útokům je v IoT klíčová
	- **Konektivita**
		- Programování musí zohledňovat různé typy konektivity
			- [[Bluetooth\|Bluetooth]]
			- [[Wi-Fi\|Wi-Fi]]
			- mobilní sítě

## Programovací jazyky IoT
### Raspberry Pi
- malý počítač
- má vlastní OS 
- velká škála využítí
- programuje se v hlavně v [[Škola/IT/Programování/Programovací jazyky/Python\|Pythonu]]
### Arduino
- mikrokontroler
- je [[Open-Source\|Open-Source]]
- platforma pro prototypování
- programuje se v upravené verzi [[Škola/IT/Programování/Programovací jazyky/C\|C]]/[[Škola/IT/Programování/Programovací jazyky/C++\|C++]]
### ESP
### Ostatní jazyky k programování IoT
- [[Škola/IT/Programování/Programovací jazyky/Java\|Java]]
	- Je robustní jazyk pro programování komplexních IoT systémů.
- [[Škola/IT/Programování/Programovací jazyky/JavaScript\|JavaScript]]
	- Je vhodný pro programování webových aplikací a frontendových částí IoT systémů.
- [[PHP\|PHP]]
	- Je vhodné pro programování backendových částí IoT systémů.
- Scratch
	- blokové programování
___
## Zabezpečení
- je v IoT kritickým aspektem vzhledem k širokému rozšíření chytrých objektů a citlivým datům
- IoT je nutno zabezpečit kvůli přístupu ke kamerám, senzorům, datům o lidech, atd.
- Zařízení bez operačního systému je bezpečnější, jelikož nemusíme řešit zabezpečení [[Škola/IT/Operační systém\|operačního systému]] 
### DMZ
![[DMZ\|DMZ]]
### Použití VLAN
- oddělení síte pro IOT a lokální sítě
![[VLAN\|VLAN]]
___
## Periferie
### Vstupní
- Světelný senzor
- tepelný senzor
- zvukový senzor
- pohybový senzor
### Výstupní
- LED
- Display
- Servo Motor
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- zná pozici svého natočení
- lze nastavit o kolik stupňů se otočí a kam
- lze nastavit rychlost otočení

</div></div>

- bzučák
- spínače