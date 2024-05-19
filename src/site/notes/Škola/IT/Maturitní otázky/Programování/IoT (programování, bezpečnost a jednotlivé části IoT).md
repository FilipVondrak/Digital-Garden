---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/IoT (programování, bezpečnost a jednotlivé části IoT)/","tags":["IOT","Maturitní_otázka","SPOSDK","Software"],"created":"2023-12-19T09:11:24.192+01:00","updated":"2024-05-16T13:26:32.377+02:00"}
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
- Chytrá žárovka připojená k [[Škola/IT/Bezdrátové sítě/Wi-Fi\|Wi-Fi]], kterou lze ovládat dálkově mobilem/hlasem
- Chytré kamery připojené k [[Škola/IT/Bezdrátové sítě/Wi-Fi\|Wi-Fi]], ke kterým se dá vzdáleně připojit

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
- [[Škola/IT/Bezdrátové sítě/Bluetooth\|Bluetooth]] 
- [[Škola/IT/Bezdrátové sítě/Wi-Fi\|Wi-Fi]]
- [[Ethernet\|Ethernet]]
- [[Škola/IT/Konektory/HDMI\|HDMI]]
### Úložiště 
- slot na paměťovou kartu 

___
## Chytré města
- soběstačná města
- metropolitní síť 
	- řídí např. tepelné ztráty
- kamerový systém
- využívají informační a komunikační technologie ke zlepšení kvality života obyvatel a efektivity provozu města
## Chytrá domácnost
- Propojené systémy a zařízení v domě, které lze ovládat a monitorovat na dálku
- Může zahrnovat osvětlení, termostaty, spotřebiče, zabezpečovací systémy a další
- jedna domácnost
## Chytrý dům
- Specifický typ chytré domácnosti, která je navržena a vybavena chytrými technologiemi od samého začátku
- Může zahrnovat integrované systémy pro osvětlení, topení, chlazení, zabezpečení, zábavu a další
- Chytré domy jsou obvykle energeticky účinnější a pohodlnější než běžné domy
- pořizovací cena chytrého domu je většinou dražší
- mnoho domácností v jednom domě
## Chytrá ulice
- Využívá senzory, datové analýzy a řídicí systémy pro optimalizaci dopravy, parkování, osvětlení a dalších oblastí
- Chytré ulice mohou zahrnovat inteligentní semafory, senzory pro detekci parkovacích míst, LED osvětlení reagující na pohyb a další technologie

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
			- [[Škola/IT/Bezdrátové sítě/Bluetooth\|Bluetooth]]
			- [[Škola/IT/Bezdrátové sítě/Wi-Fi\|Wi-Fi]]
			- mobilní sítě

## Programovací jazyky IoT
### Raspberry Pi
- malý počítač
- zmínit [[Škola/IT/Maturitní otázky/Programování/GPIO\|GPIO]]
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

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/kybernetika/dmz/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- vystrčení dané služby nebo serveru mimo firewall
- může působit jako honeypot

![Pasted image 20240519204416.png](/img/user/Images/Pasted%20image%2020240519204416.png)

</div></div>

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