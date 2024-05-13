---
{"dg-publish":true,"permalink":"/Škola/IT/Bezdrátové sítě/Wi-Fi/","created":"2024-05-12T22:00:07.226+02:00","updated":"2024-05-13T23:24:18.195+02:00"}
---

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
