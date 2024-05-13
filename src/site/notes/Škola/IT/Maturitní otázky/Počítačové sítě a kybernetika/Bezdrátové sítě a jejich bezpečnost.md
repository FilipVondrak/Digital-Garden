---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Bezdrátové sítě a jejich bezpečnost/","created":"2023-12-14T18:40:04.139+01:00","updated":"2024-05-13T23:28:24.458+02:00"}
---

# Elektromagnetické vlnění

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/fyzika-elektrotechnika/elektromagneticke-vlneni/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- šíří se v prostředí
	- čím je prostředí hustší, tím se zvětšuje tlumení signálu
- má určitou dobu v periodách
- když se mění vlnová délka, vnímáme jinou barvu
- čím menší má délku, tím vyšší má energii
- lidské oko vnímá pouze vlnění o délce mezi 390 nm až 790 nm ([[Škola/Fyzika-Elektrotechnika/Světlo\|světlo]])
![Pasted image 20240221164812.png](/img/user/Images/Pasted%20image%2020240221164812.png)![Pasted image 20240221164836.png](/img/user/Images/Pasted%20image%2020240221164836.png)
![Pasted image 20240513191903.png](/img/user/Images/Pasted%20image%2020240513191903.png)

</div></div>

# Druhy bezdrátových sítí
## Bluetooth

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/bezdratove-site/bluetooth/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- je to bezdrátová technologie, která umožňuje komunikaci mezi elektronickými zařízeními na krátkou vzdálenost, přibližně 10m
- Byla vyvinuta v 90. letech 20. století
- Jedná se o standardizovaný protokol pro bezpečnou a spolehlivou komunikaci mezi zařízeními různých výrobců
- využívá rádiové vlny v frekvenčním pásmu 2,4 GHz
- Umožňuje vytváření osobních sítí (**PAN**) mezi zařízeními
- Komunikace probíhá ==na bázi krátkých paketů== dat, což umožňuje efektivní využití energie a rychlou přenosovou rychlost
- Bluetooth standard zahrnuje ==řadu bezpečnostních funkcí, včetně šifrování dat a autentizace zařízení==

> [!info] Fun fact
> Je pojmenován po dánském králi Haraldovi "Bluetooth" Gormssonu.
> Logo Bluetooth je runa spojení. ![Pasted image 20240513191240.png](/img/user/Images/Pasted%20image%2020240513191240.png)

## Funkce Bluetooth
### Párování
- Proces, při kterém se dva Bluetooth zařízení navzájem identifikují a vytvoří spolehlivé spojení
### Přenos dat
- umožňuje přenos souborů, jako jsou fotografie, videa, hudba a dokumenty, mezi zařízeními
### Audio streaming
- často využíván pro bezdrátový přenos zvuku mezi zařízeními, jako jsou reproduktory, sluchátka nebo audio systémy v autech
## Výhody
- bezdrátové propojování s ostatními zařízeními
- nízká spotřeba energie
- kompatibilita
## Nevýhody
- Krátká vzdálenost
- je náchylný k odposlechu
- rychlost je pomalejší než u ostatních technologií (např. [[Škola/IT/Bezdrátové sítě/Wi-Fi\|Wi-Fi]])

</div></div>

## Wi-Fi

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/bezdratove-site/wi-fi/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> *Wireless Fidelity*
- umožňuje se zařízením připojit k internetu a k sobě navzájem bez nutnosti kabelů
- Funguje na principu rádiových vln, které přenáší data mezi zařízeními a [[Škola/IT/Hardware/AP\|AP]]/[[Škola/IT/Hardware/Router\|Router]]
- Standardy WiFi jsou definovány organizací IEEE (například IEEE 802.11b/g/n/ac/ax)
- začala v 80. letech jako experimentální technologie a postupně se rozšířila
- První standard 802.11 byl přijat v roce 1997 a nabízel přenosovou rychlost až 2 Mb/s
## Zabezpečení Wi-Fi
### Nastavení sítě
#### Změnit defaultní heslo
- hned po nastavení routeru bychom měli změnit defaultní heslo
#### Vypnout broadcast SSID
- **SSID** -> jméno sítě
- pokud vypneme posílání jména sítě, tak ho schováme před ostatními 
- nebude se zobrazovat na seznamu dostupných síti
- když se bude někdo chtít k síti připojit, musí vědět že ta síť tu je a jaké má jméno
#### Filtrování MAC
- pouze zařízení s povolenou [[Škola/IT/ISO OSI/Linková vrstva#Media Access Control (MAC)\|MAC]] adresou se mohou připojit k síti
- pro hosty pak můžeme vytvořit hostovskou síť, která nemá přístup k našim datům
#### Zapnout firewall
- ujistit se, že máme zapnutý [[Škola/IT/Firewall\|Firewall]]
#### Pravidelně aktualizovat firmware
- pravidelně kontrolovat, že máme aktuální firmware
### WEP
-> *Wired Equivalent Privacy*
- prvním protokolem zabezpečení Wi-Fi
- dnes se již nedoporučuje používat
- Je náchylný k prolomení a neposkytuje dostatečnou ochranu proti moderním hackerským útokům
### WPA
-> *Wi-Fi Protected Access*
- nabízí značné zlepšení zabezpečení
- Používá šifrování TKIP
- ověřování pomocí RADIUS serveru
### WPA 2
-> *Wi-Fi Protected Access 2*
- nejrozšířenějším protokolem zabezpečení Wi-Fi v současnosti
- Používá silnější šifrování AES
- ověřování pomocí protokolu PSK (Pre-Shared Key) nebo RADIUS serveru
### WPA3
-> *Wi-Fi Protected Access 3*
- nejnovější protokol zabezpečení Wi-Fi
- nabízí nejvyšší úroveň ochrany, šifrování na 192 bitů
- Zavádí několik nových funkcí
	- **Individualized Data Encryption (SAE)**
		- nahrazuje Pre-Shared Key
		- silnější ověřování a ochranu proti útokům typu offline cracking
	- **Protected Management Frames (PMF)**
		- Chrání řídicí rámce Wi-Fi před odposlechem a manipulací
	- **Enhanced Roaming**
		- Usnadňuje a zrychluje roaming mezi přístupovými body
## Problémy Wi-Fi
- **rušení signálu**
	- může být způsobeno
		- okolními zařízeními
		- fyzickými překážkami
		- přetížením síťového kanálu
- **omezený dosah**
- **bezpečnostní hrozby**
	- útoky typu "krádež identity"
	- riziko prolomení hesla
	- neoprávněný přístup k datům
## Standardy Wi-Fi

| Generace | IEEE standard | Rok  | Frekvence              | Max rychlost (Mbits/S) |
| -------- | ------------- | ---- | ---------------------- | ---------------------- |
| Wi-Fi 0  | 802.11        | 1997 | 2.4                    | 2                      |
| Wi-Fi 1  | 802.11b       | 1999 | 2.4                    | 11                     |
| Wi-Fi 2  | 802.11a       | 1999 | 5                      | 54                     |
| Wi-Fi 3  | 802.11g       | 2003 | 2.4                    | 54                     |
| Wi-Fi 4  | 802.11n       | 2008 | 2.4, 5                 | 600                    |
| Wi-Fi 5  | 802.11ac      | 2014 | 5                      | 6933                   |
| Wi-Fi 6  | 802.11ax      | 2019 | 2.4, 5                 | 9608                   |
| Wi-Fi 6E | 802.11ax      | 2020 | 6                      | 9608                   |
| Wi-Fi 7  | 802.11be      | 2024 | 2.4, 5, 6              | 46120                  |
| Wi-Fi 8  | 802.11bn      | 2028 | 2.4, 5, 6, 7, 42.5, 71 | 100000                 |


</div></div>

## NFC

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/bezdratove-site/nfc/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> *Near Field Communication*
- bezdrátová komunikační technologie, která umožňuje bezkontaktní přenos dat
- funguje na krátkou vzdálenost, obvykle do 10 cm
- vychází z radiofrekvenční identifikace (RFID)
- umožňuje rychlou a jednoduchou výměnu informací mezi zařízeními
- často se nachází v mobilech a hodinkách
## Využití NFC
### Platební karty
- používá se v bezkontaktních platebních kartách a mobilních telefonech
- usnadnění a zrychlení plateb v obchodech a na přepravě v MHD
### Kontrola přístupu
- používá se v identifikačních kartách a přístupových systémech k autentizaci uživatelů
- k povolení přístupu do zabezpečených oblastí
### Sdílení dat
- ke sdílení kontaktů, webových stránek a dalších dat mezi zařízeními
### Spárování zařízení
- používá se k párování zařízení
## Hrozby NFC
### NFC Skimming
- hrozba, že útočník zachytí NFC signál a přečte ho
- zachycené informace se pak dají znovu použít
- Cílem bývá získání informací o platební kartě, identifikačním průkazu nebo jiném zařízení

</div></div>

## Infrared

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/bezdratove-site/infrared/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- **Infračervená (IR) komunikace** je technologie bezdrátového přenosu dat, která využívá neviditelné světelné vlny
- používá vlnové délky delší než 700nm
## Použití infračerveného světla
### Dálkové ovládání
- používá se v dálkových ovladačích k odesílání signálů do televize a dalších zařízení
### Senzory
- se používá v senzorech přiblížení a pohybu k detekci existence objektů a jejich pohybu
### Lékařské zobrazování
- IR se používá v některých lékařských zobrazovacích technikách, jako je termografie
## Jak funguje
- IR komunikace funguje na principu odesílání a přijímání modulovaných infračervených paprsků
- zařízení odesílající signál vysílá pulzy infračerveného světla, které jsou modulovány informacemi
- zařízení přijímající IR signál zachytí infračervené paprsky a dekóduje z modulace
## Výhody
### Nízká cena
- IR komponenty jsou relativně levné
### Malá spotřeba energie
- spotřebovává jen málo energie
- je ideální pro přenosná zařízení
### Odolná proti rušení
- šíří se v přímce, takže je odolná proti rušení z jiných zařízení

</div></div>

## GPS

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/bezdratove-site/gps/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> *Global Positioning System*
- je to globální navigační satelitní systém
- umožňuje určit polohu, rychlost a čas na Zemi s vysokou přesností
- je provozován americkým ministerstvem obrany
- bezplatně dostupný pro civilní účely
## Jak funguje
- funguje na principu trilaterace
	1. Zařízení (např. telefon) zachytává signál z několika satelitů GPS, které obíhají kolem Země
	2. Každý satelit (obvykle alespoň 4 nebo více) vyšle signál, který obsahuje informace o jeho poloze a přesném čase
	3. Zařízení vypočítá svojí polohu podle doby, kterou trvalo signálům dorazit k zařízení 
## Výhody 
### Přesnost
- je to vysoce přesný systém
- dokáže určit polohu s přesností na několik metrů
### Dostupnost
- je k dispozici po celém světě
### Všestrannost
- používá se v široké škále aplikací
## Nevýhody
### Závislost na satelitech
- GPS je závislý na dostupnosti satelitních signálů
- V oblastech s nízkým pokrytím signálem nebo v budovách může být GPS nepřesný nebo nedostupný
### Ovlivnění rušením
- GPS signály mohou být ovlivněny rušením z jiných zdrojů, jako například vysoké budovy či rušičky signálu
### Možnost zneužití
- mohou být zneužity ke sledování osob bez jejich souhlasu

## Alternativy GPS
### GLONASS
- Ruský navigační systém
- Srovnatelná přesnost s gps
### BeiDou
- Čínský navigační systém
- Je ve fázi rozvoje
### Galileo
- Evropský navigační systém
- Je ve fázi rozvoje
- má za cíl nezávislost na GPS a GLONASS
## Další technologie geolokace
### Triangulace mobilních věží
- využívá signály z mobilních věží k určení polohy zařízení
- přesnost na desítky až stovky metrů
- Používá se běžně v mobilních telefonech pro nouzové volání a sledování polohy
### [[Škola/IT/Bezdrátové sítě/Wi-Fi\|Wi-Fi]] lokalizace
- využívá signály z Wi-Fi routerů k určení polohy zařízení
- přesnost na několik metrů
- Používá se v nákupních centrech, na letištích a dalších místech s hustou sítí Wi-Fi routerů

</div></div>

## Mobilní síť

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/bezdratove-site/mobilni-sit/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- systém, který umožňuje komunikaci mezi mobilními zařízeními, jako jsou mobilní telefony a tablety, a sítí operátora
- Tyto sítě umožňují hlasové hovory, posílání textových zpráv, přístup k internetu a další služby
- používají vysílače, které jsou umístěny na věžích a vysílají signály, které pokrývají oblast
## Typy mobilních sítí
### 1G
- Analogová síť
- pouze hlasová komunikace
### 2G
- Digitální síť
- hlasová komunikace a SMS
- nízká rychlost přenosu dat
### 2.5G (EDGE)
- je rychlejší než 2G
- rychlost až 384Kbps
- umožňuje MMS
### 3G
- síť s vyšší rychlostí
- možné videohovory, mobilní internet a širokopásmové služby
### 4G
- velmi vysoká rychlost internetu
- podpora VoIP (volání přes internet)
- zvládne HD videa
### 5G
- nejnovější generace mobilních sítí
- extrémně vysoké rychlosti
- nízká latence
## LTE
- standard 4G mobilních sítí
- poskytuje vysokorychlostní připojení k internetu
## Architektura mobilních sítí
![Pasted image 20240513225807.png](/img/user/Images/Pasted%20image%2020240513225807.png)
### BTS (Base Transceiver Station)
- základnová stanice, která zajišťuje bezdrátové spojení s mobilními telefony
- formované do ==tvaru benzenového jádra==
- pomocí ==3 vysílačů lze určit polohu==
### BSC (Base Station Controller)
- řídící prvek pro skupinu BTS
- podobné jako RNC
- stará se o alokaci kanálů a řízení hovorů
### MSC (Mobile Switching Centre)
- ústředna, která spojuje mobilní sítě s pevnou telefonní sítí (PSTN) a dalšími mobilními sítěmi
### HLR (Home Location Register)
- databáze uchovávající informace o mobilních telefonech a jejich umístění
## SIM
-> *Subscriber Identity Module*
- čipová karta obsahující informace o uživateli
- slouží k autentizaci

</div></div>

## Satelitní

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





</div></div>

## TV

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





</div></div>

## FSO

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





</div></div>

## Rádiová síť

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





</div></div>

# ISP

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/isp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> *Internet Service Provider*
- organizace, která poskytuje přístup k internetu a související služby koncovým uživatelům
- sám ISP platí nadřazeným ISP pro přístup k internetu 
## Typy připojení
### DSL
- připojení pomocí telefonní infrastruktury
- stabilní připojení
### Kabelové připojení 
- je rychlé a spolehlivé
- Používá se kabelový televizní kabel
### Fiber-optic
- přístup k internetu pomocí optických vláken
- vysokorychlostní přenos dat
### Satelitní
- přístup k internetu pomocí satelitní komunikace
- zejména v oblastech s omezeným pokrytím jinými typy
### Mobilní
- Poskytuje přístup k internetu pomocí mobilních sítí a bezdrátových technologií

</div></div>

# Typy antén
- Antény jsou důležitou součástí bezdrátových komunikačních systémů
- slouží k přenosu a příjmu elektromagnetických vln
## Směrová
- soustředí svůj signál do určitého směru, což zlepšuje jejich dosah a snižuje rušení
- Mají vyšší zisk než všesměrové antény a jsou vhodné pro konkrétní účely, jako je například point-to-point spojení
### Yagi anténa
- sestávající z jednoho dipólu a řady direktorů a reflektorů
- soustředí signál do určitého směru
![Pasted image 20240513232600.png](/img/user/Images/Pasted%20image%2020240513232600.png)
### Parabolická anténa 
- používá se pro satelitní komunikaci a mikrovlnná spojení
![Pasted image 20240513232707.png](/img/user/Images/Pasted%20image%2020240513232707.png)
## Sektorová
- speciálním typem směrových antén
- mají širší směrový vzor a pokrývají větší úsek prostoru
- používají v mobilních sítích a ve Wi-Fi infrastruktuře pro poskytování širokého pokrytí
## Všesměrová
- přijímají a vysílají signály ze všech směrů
- vhodné pro situace, kdy je třeba pokrýt širokou oblast nebo když není známá přesná poloha přijímače
# Hrozby bezdrátových sítí
## Odposlech
- Neoprávněný přístup k komunikaci mezi mobilními zařízeními a sítí nebo mezi jednotlivými mobilními zařízeními
## Man-in-the-Middle
- Neoprávněná osoba se dostane mezi komunikující strany a zachycuje nebo manipuluje s přenášenými daty
## DDoS
- útoky typu "odmítnutí služby"
- cílí na přetížení síťových prostředků a způsobení výpadku služeb mobilní sítě 

