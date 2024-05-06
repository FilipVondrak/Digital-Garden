---
{"dg-publish":true,"permalink":"/Škola/IT/ISO OSI/","created":"2023-12-14T19:07:35.550+01:00","updated":"2024-05-06T12:15:02.512+02:00"}
---

# 1. **Fyzická** vrstva

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



-> **Physical Layer**
## Co je fyzická vrstva
- nejnižší vrstva ISO OSI
- slouží jako ==základ pro přenos dat== v počítačových sítích
- Zabývá se ==fyzickým propojením počítačů== a přenosem bitů mezi nimi
- Obsahuje rozložení pinů, napěťové úrovně a specifikuje vlastnosti kabelů
- ==pracuje s bity==
## Hlavní funkce
- **Převod dat na signály (tvorba bitů)**
	- Fyzická vrstva přenáší data v podobě ==elektrických signálů, optických signálů nebo bezdrátových signálů==
- **Řízení přenosu**
- **Propojení**
- **Přenos bitů**
## Fyzické topologie
- fyzická reprezentace propojení zařízení
- následující jsou 4 druhy fyzických topologií
### Mesh Topologie
- v mesh topologii má každé zařízení dedikovaný point-to-point připojení s každým dalším zařízením
- je zde větší zabezpečení dat
- je náročnější na nastavení jelikož je více komplexní
![Pasted image 20240505152233.png](/img/user/Images/Pasted%20image%2020240505152233.png)
### Star Topologie
- ve star topologii by mělo každé zařízení mít připojení k centrálnímu kontroleru nebo hubu
- je jednoduchá na nainstalaci
- je nejčastější
![Pasted image 20240505152411.png](/img/user/Images/Pasted%20image%2020240505152411.png)
### Bus Topologie
- v bus topologii jsou zařízení propojené pouze jedním kabelem
- je levný
- přepojení a přeinstalace je komplikovaná
![Pasted image 20240505152654.png](/img/user/Images/Pasted%20image%2020240505152654.png)
### Ring Topologie
- v kruhové topologii je každé zařízení připojené k [[Škola/IT/Hardware/Repeater\|repeateru]] v kruhovém tvaru
![Pasted image 20240505152828.png](/img/user/Images/Pasted%20image%2020240505152828.png)
## Hardware
- [[Škola/IT/ISO OSI/Síťový kabel\|Síťový kabel]]
- [[Škola/IT/Hardware/Síťová karta\|Síťová karta]]
- [[Škola/IT/Hardware/Repeater\|Repeater]]
- [[Škola/IT/Hardware/HUB (Rozbočovač)\|HUB (Rozbočovač)]]
- [[Škola/IT/Hardware/Převodník\|Převodník]]

</div></div>

# 2. **Linková** vrstva

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/iso-osi/linkova-vrstva/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Data Link Layer** (DLL)
## Co je linková vrstva
- známá také jako spojová vrstva nebo vrstva datového spoje
- Je to bezpečná, opravuje chyby
- Kóduje a dekóduje data
- považuje se za nejkomplexnější vrstvu [[Škola/IT/ISO OSI\|ISO OSI]]
## Průběh dat
1. Linková vrstva přijme data ze [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvy]] ve formě packetů
2. Rozdělí packety do rámců
3. Přidá do na začátek a konec speciální bity pro opravu chyb a adresaci
4. Pošle rámce bit-po-bitu do [[Škola/IT/ISO OSI/Fyzická vrstva\|fyzické vrstvy]]
![Pasted image 20240505140420.png](/img/user/Images/Pasted%20image%2020240505140420.png)
## Podvrstvy
### Logical Link Control (LLC)
- stará se o flow control
- je zodpovědná za poskytování chybových zpráv a potvrzení
- Používá ji například protokol NetBIOS Frames
- Většina protokolů ji nepoužívají, místo ní se o flow control a error management stará protokol [[Škola/IT/Protokoly/TCP\|TCP]] na [[Škola/IT/ISO OSI/Transportní vrstva\|transportní vrstvě]] 
### Media Access Control (MAC)
- stará se o interakce zařízení
- adresuje rámce
- ovládá přístup k fyzickým médiím
- MAC adresa je vypálena do čipu
## Hlavní funkce
### Vytváření rámců
#### Na straně odesílatele
1. Přijme packety ze [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvy]] a přidá k nim speciální bity pro opravu chyb a adresaci
2. Postupně pak předá bit po bitu do [[Škola/IT/ISO OSI/Fyzická vrstva\|fyzické vrstvy]]
#### Na straně příjemce
1. Linková vrstva si vezme bity z [[Škola/IT/ISO OSI/Fyzická vrstva\|fyzické vrstvy]] a zorganizuje je do rámce
2. Zpracuje rámec
3. Pošle ho do [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvy]]
### Zajištění spolehlivé komunikace
- zajišťovat spolehlivou komunikaci mezi dvěma nebo více uzly v jednom datovém spoji
	- **Typy datových spojů**
		- Dvoubodový
			- sériová linka spojující 2 počítače
		- Mnohabodový
			- Lokální (LAN) sítě
### Fyzické adresování
 - přidá k datům MAC adresy odesílatele a příjemce
 - MAC je unikátní fyzická adresa, která je přiřazená zařízení při výrobě
### Řízení přístupu k MAC
### Detekce chyb
- Odpovědnost linkové vrstvy je detekce a oprava chyb při přenosu
- Používá tyto techniky
	- [Pro detekci](https://www.geeksforgeeks.org/error-detection-in-computer-networks/)
	- [Pro opravu](https://www.geeksforgeeks.org/hamming-code-in-computer-network/)
- Přidává do dat bity pro detekci chyb
- Přidává spolehlivost fyzické vrstvě přidáním mechanismu pro přeposlání poškozených a ztracených rámců
### Ovládá řízení toku dat
- Pokud je rychlost odesílatele rychlejší než příjemce, tak se mohou ztratit některé rámce
- linková vrstva synchronizuje rychlost mezi příjemcem a odesílatelem
### Fragmentace a defragmentace
## Zapouzdření
-> **Rámec (Frame)**
![Pasted image 20240505153242.png](/img/user/Images/Pasted%20image%2020240505153242.png)
## Hardware
- [[Škola/IT/Hardware/L2 switch\|L2 switch]]
- [[Bridge\|Bridge]]

</div></div>

# 3. **Síťová** vrstva

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/iso-osi/sitova-vrstva/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Network Layer**
## Co je síťová vrstva
- je to 3. vrstva [[Škola/IT/ISO OSI\|ISO OSI]] modelu
## Hlavní funkce
### Routování
- hledá nejkratší cestu k poslání packetu
### Logická adresace
- k identifikaci každého zařízení v síti používá IP adresy
## Zapouzdření
-> **Packet**
- Obsahuje
	- IP odesílatele
	- IP příjemce
	- Data
![Pasted image 20240505193444.png](/img/user/Images/Pasted%20image%2020240505193444.png)
## Hardware
- [[Škola/IT/Hardware/Router\|Router]]
- [[Škola/IT/Hardware/L3 switch\|L3 switch]]

</div></div>

# 4. **Transportní** vrstva

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/iso-osi/transportni-vrstva/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Transport Layer**
## Co je transportní vrstva
- je to 4. vrstva [[Škola/IT/ISO OSI\|ISO OSI]] modelu
- přidává porty zdroje a destinace do headeru segmentu
## Hlavní funkce
- poskytuje potvrzení o doručení
- pokud je v datech chyba, tak je pošle znova
### Segmentace
- při odesílání přijme data z [[Relační vrstva\|relační vrstvy]] a rozdělí je do několika menších segmentů
### Složení dat
- transportní vrstva u příjemce příjímá rozdělená data a skládá je zpět
### Service Point Addressing
- aby se data doručily do správné destinace, tak se transportní vrstva stará o přidávání portů
- data se doručí správnému procesu
## Postup vytvoření segmentů
### Na straně odesílatele
1. Přijme formátovaná data z vyšších vrstev
2. Provede segmentaci
3. Přidá kontrolu průběhu a chyb, aby se zajistil bezproblémový přenos dat
4. Přidá porty zdroje a destinace do headeru
5. Pošle segment [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvě]]
### Na straně příjemce
1. transportní vrstva přečte porty
2. provede sekvencování a složí segmentovaná data
3. pošle data určité aplikaci
## Protokoly na transportní vrstvě
### TCP - Transmission Control Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/tcp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- spolehlivý, spojovaný protokol  
![Pasted image 20240505202256.png](/img/user/Images/Pasted%20image%2020240505202256.png)
## Využití
 - web. Stránky, 
 - emaily, 
 - služby, kde se nesmí ztratit data 
## Výhody
- má detekci a opravu chyb
	- Pokud od příjemce neobdrží zprávu, že data přišla v pořádku, tak je pošle znova
## Nevýhody
-  je pomalý

</div></div>

### UDP - User Datagram Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/udp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- nespolehlivý a nespojovaný protokol
	- Nemá jak zkontrolovat, zda data dorazili k příjemci
## Využití
- videa
	- video se načte rychle a nevadí, pokud pár pixelů ve snímku chybí 
- Microsoft DHCP server
## Výhody
- předává aplikaci přímí přístup k datagram delivery službě
- má minimální 
## Nevýhody
- je rychlý

</div></div>

## Zapouzdření
-> **Segment**
- Obsahuje
	- IP příjemce
	- IP odesílatele
	- Porty
	- Data

</div></div>

# 5. **Relační** vrstva
# 6. **Prezenční** vrstva
# 7. **Aplikační** vrstva
![[Aplikační vrstva\|Aplikační vrstva]]

![Pasted image 20240505153558.png](/img/user/Images/Pasted%20image%2020240505153558.png)
![OSI_Model_v1.svg.png](/img/user/Images/OSI_Model_v1.svg.png)
![Pasted image 20240506121500.png](/img/user/Images/Pasted%20image%2020240506121500.png)