---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Protokoly na aplikační vrstvě/","created":"2023-12-14T18:39:09.524+01:00","updated":"2024-05-04T22:20:33.232+02:00"}
---

# Aplikační vrstva

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/iso-osi/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




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

</div></div>

# HTTP - Hypertext Transfer protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/http/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Co je HTTP
- je internetový protokol určený pro komunikaci s WWW servery
- Slouží pro přenos hypertextových dokumentů ve formátu HTML, XML, i jiných typů souborů
- Pro zabezpečení HTTP se často používá [[Škola/IT/Protokoly/TLS\|TLS]] spojení nad TCP -> **HTTPS**
## Porty HTTPS
- HTTP -> **80**
- HTTPS -> **443**
## Fungování protokolu
- Protokol funguje způsobem ==dotaz-odpověď==
- Uživatel pošle serveru dotaz ve formě textu (označení dokumentu, informace o prohlížeči, …)
- Server pošle odpověď (zda se dokument podařilo najít, typ dokumentu, …)
## Metody
### Nejčastější metody
#### GET
- Požadavek na uvedený objekt se zasláním případných dat (proměnné prohlížeče, session id, …)
- ==Výchozí metoda== při požadavku na zobrazení hypertextových stránek
- ==Celkově nejpoužívanější==
#### POST
- ==Odesílá uživatelská data== na server
- Data může odesílat i metoda GET, metoda POST se však používá pro příliš velký objem dat, nebo pokud není vhodné přenášená data zobrazit jako součást [[URL\|URL]]
	- víc než 512 bajtů, což je velikost požadavku GET
- data předávaná metodou POST jsou obsažena v HTTP požadavku
#### DELETE
- ==Smaže uvedený objekt ze serveru==
- Je zapotřebí jistých oprávnění
### Ostatní metody
#### PUT
- Nahraje data na server
- Nepoužívá se (náhrada = FTP)
#### HEAD
- Poskytne metadata (velikost, typ, datum změny)
- Podobná metodě get, akorát neposkytne data
#### CONNECT
- Spojí se s uvedeným objektem přes uvedený port
- Používá se při průchodu skrze proxy pro ustanovení kanálu SSL
#### OPTIONS
- Dotaz na server, jaké podporuje metody.
#### TRACE
- Odešle kopii obdrženého požadavku zpět odesílateli
- klient může zjistit, co na požadavku mění nebo přidávají servery, kterými požadavek prochází.

</div></div>

# FTP - File transfer protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/ftp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Co je FTP
- Slouží pro přenos souborů mezi z jednoho počítače na jiný
- nejstarší protokol pro přenos v síti
- používá **[[Škola/IT/Protokoly/TCP\|TCP]]**
- ==zabezpečené FTP používá [[SSL\|SSL]]== -> **FTPS** 
## Využití
- Přenos velkých dat
- možno poslat několik souborů naráz
- stahování ISO souborů
## Porty pro FPT
- FPT -> **21**
- FPTS -> **990**
## Jak použít
1. Přes prohlížeč
	- s prohlížečem není potřeba žádný speciální software pro stahování souborů ze serveru
2. FTP GUI klient
	- použití third-party aplikací může ulehčit uživateli odesílání souborů a připojování k serveru
		- **FTP aplikace**
			- Klienti
				- Prohlížeč
				- Windows File Explorer
				- TotalCommander
			- Servery
				- FileZilla
				- Caesar FTP
				- Cerberus FTP
1. Command-line FTP
	- většina velkých operačních systémů už mají zabudovaný 
## Jak funguje
- funguje tak, že se otevřou dvě spojení, která propojí počítače snažící se vzájemně komunikovat
- Jedno spojení je určeno pro příkazy a odpovědi, které se posílají mezi dvěma klienty
	- **Příkazy**
		- send
		- get
		- change directory
		- transfer
- druhý kanál zajišťuje přenos dat
	- **režimy přenosu dat**
		- block
			- rozděluje data do bloků
		- stream
			- umožňuje FTP spravovat informace v řetězci dat bez jakýchkoli hranic mezi nimi
		- compressed
			- používá algoritmus Lepmep-Ziv na kompresování dat

</div></div>

# Pošta (E-mail)
- funguje na principu klient-server
- **SERVER**
	- Kerio mail server (Windows)
	- Postfix (Linux)
- **KLIENT**
	- Outlook
	- ThunderBird
	- Gmail
	- Seznam
## Přenosy
![Pasted image 20240504201345.png](/img/user/Images/Pasted%20image%2020240504201345.png)
 ### MUA - Mail User Agent
 - všichni poštovní klienti
 ### MTA - Mail Transfer Agent
 - Server
 - transport mailových zpráv
 ### MDA - Mail Delivery Agent 
 - Server
 - transport mailových zpráv
## Protokoly
### SMTP - Simple Mail Transfer Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/smtp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> Simple Mail Transfer Protocol
## Co je SMTP 
- Technický standard pro posílání emailu přes síť
- slouží pro doručování, ne pro odebírání pošty
> [!Tip]- IRL přirovnání
> Poštovní služba doručí poštu do schránky, ale příjemce si musí pro zásilku do schránky dojít
## Porty
- SMTP - **25**
- SMTP (šifrované SMTP s SSL, už je zastaralé) - **465**
- SMTP (šifrované SMTP s TLS, nyní defaultní port) - **587**
## Jak funguje
- SMTP definuje proces pro výměnu dat mezi klientem a mailovým serverem
1. SMTP otevření připojení
	- První krok je ==otevření [[Škola/IT/Protokoly/TCP\|TCP]] připojení== mezi klientem a serverem
	- Zahájení procesu posílaní emailu posláním "Hello" SMTP příkazu (HELO, EHLO)
2. Přenos dat emailu
	- klient pošle sérii příkazů zároveň s daty emailu:
		- **email hlavička**
			- odesílatel a příjemce
			- destinace
			- adresy serverů, porty, protokol
			- čas a datum
			- předmět
			- název počítače a IP adresy, info o OS
		- **email tělo**
			- kontent emailu
			- ==může být plain text nebo HTML==
		- **email footer**
			- Přílohy
			- Podpis
3. MTA
	- spustí se MTA a zkontroluje doménu příjemce
	- pokud se doména liší od odesílatele, tak se podá dotaz DNS aby našel doménu příjemce
4. Zavření spojení
	- Klient oznámí serveru jakmile je přenos dat kompletní a server uzavře spojení
- obvykle není tento první emailový server poslední destinace emailu, ale server opakuje tento SMTP proces a pošle email dalšímu serveru dokud se nedostane email serveru příjemce
## SMTP příkazy
- **HELO/EHLO**
	- Zahajují SMTP připojení
	- HELO je základní verze a EHLO je specializovaný typ SMTP
- **MAIL FROM**
	- řekne emailovému serveru kdo posílá email
- **RCPT TO**
	- poslouchá příjemce emailu
	- klient pošle tento příkaz několikrát pokud má email více příjemců
- **DATA**
	- nachází se před kontentem emailu
- **RSET**
	- resetuje připojení
	- odstraní všechny dříve odeslané informace bez ukončení připojení
	- použije se v případě, že klient pošle špatné informace
- **QUIT**
	- ukončí připojení

</div></div>

### POP3 - Post Office Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/pop-3/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Post Office Protocol**
## Co je POP3
- je to starší protokol, který byl původně vytvořen k používání pouze na jednom počítači
- na rozdíl od moderních protokolů nepoužívá two-way synchronizaci
- protokol stáhne email ze serveru ke klientovi
## Porty
- POP3 -> **110**
- POP3 (zašifrovaný) -> **995**
## Nevýhody POP3
- pokaždé, když se stáhne jeden email na nové zařízení, tak vypadá jako nepřečtený i pokud byl již zobrazen na jiném zařízení
- není možné vidět odeslanou pošlu z jiných zařízení
- email se nezobrazí hned po doručení, ale až po nějaké době
- nelze synchronizovat nastavení schránky
## Výhody POP
- Přístup ke starým emailům i bez připojení k internetu
- po stažení se email zobrazí ve file systému zařízení

</div></div>

### IMAP - Internet Message Access Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/imap/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> The Internet Message Access Protocol
## Co je IMAP
- slouží k vzdálenému přístupu k vašim e-mailům na serveru
- hlavní výhodou je že uživatel může otevřít svoje emaily z jakéhokoliv zařízení
- Na rozdíl od POP3, který zprávy stahuje do vašeho zařízení, IMAP funguje spíše jako online schránka
- e-maily zabírají úložný prostor na serveru vašeho poskytovatele e-mailu
## Porty
- IMAP (šifrovaný, SSL/TLS) -> **993**
## Výhody IMAPu
- **přístup odkudkoliv**
	- Můžete kontrolovat a spravovat své e-maily z jakéhokoli zařízení
	- Všechny zprávy zůstávají uložené na serveru
- **Synchronizace napříč zařízeními**
	- Ať už zprávu přečtete, označíte jako spam nebo smažete, změny se projeví na všech vašich zařízeních
- **Hledání na straně serveru**
	- MAP umožňuje provádět vyhledávání přímo na e-mailovém serveru, což může být rychlejší a efektivnější, zejména pokud máte velké množství e-mailů

</div></div>

# DNS

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/dns/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software #SPOSDK #Maturitní_otázka 
-> Domain name services
- **port 53**
- převádí doménová jména na IP adresy (např. www.amazon.com převede na 192.0.2.44)
	- Doménová jména jsou čitelná pro lidi
	- IP adresy jsou čitelné pro zařízení

# Struktura
- . - kořen
- top level domain - .com, .cz, .edu 
- second level domain - google.com
- subdomain - photos.google.com 
![Pasted image 20240314210031.png](/img/user/Images/Pasted%20image%2020240314210031.png)
# DNS záznamy
- **A** - IPv4
- **CNAME** - Canonical Name - domény s níž souvisí subdomény (takže doména - spošdk.cz, subdomény - jidelna, moodle ..)
- **AAAA** - IPv6
- **MX** - poštovní server
- **TXT** - libovolný text (používá se např. pro ověření vlastnictví)

</div></div>

# DHCP

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/dhcp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software #Protokol
-> Dynamic Host Configuration Protocol
## Využití
- dynamická konfigurace síťového rozhraní
## Výhody oproti statickým IP adresám
- **Automatické přidělování IP adres**
	- Nemusíte ručně nastavovat IP adresu na každém zařízení, což šetří čas a minimalizuje chyby
- **Dynamické přidělování**
	- IP adresy jsou přidělovány pouze po dobu, kdy je zařízení zapnuté a připojené k síti. Tím se šetří vzácné IP adresy, což je důležité zejména u velkých sítí.
- **Centrální správa**
	- Konfiguraci sítě lze snadno spravovat na jednom místě - na serveru DHCP
## Princip
1. Po připojení zařízení k síti vyšle klient na server DHCP zprávu s dotazem na IP adresu
2. Server DHCP odpoví nabídkou volné IP adresy z jeho fondu
3. Klient si tuto nabídku vyžádá a server mu zašle kromě IP adresy i další důležité informace, jako je maska podsítě, výchozí brána a DNS servery
4. Zařízení pak může na základě získaných informací komunikovat v síti
![](https://lh7-us.googleusercontent.com/Z2Uf8LIQXLvDlb7l9dF50MLf-kXp1SvQKkzoyUxV7QhtpFEgCVgWWnrLU1rX_KyWQPnuPN3yEitrd2FPgiJwENPYUlOgRbn38N6E6Cy-4liZ8URA5hlEvUmDn4pL9tzxIHpYlHyNn5YhBQMUQCCq29o)


</div></div>
