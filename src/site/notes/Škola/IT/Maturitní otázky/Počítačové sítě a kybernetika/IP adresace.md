---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/IP adresace/","tags":["SPOSDK","Maturitní_otázka","IT"],"created":"2023-12-14T18:39:58.589+01:00","updated":"2024-05-06T15:00:02.105+02:00"}
---

# Síťová vrstva

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

# Transportní vrstva

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

# IP Adresace
- probíha na 3. vrstvě [[Škola/IT/ISO OSI\|ISO OSI]] modelu
- je to logická adresace ([[Škola/IT/ISO OSI/Linková vrstva#Media Access Control (MAC)\|MAC]] je fyzická adresace)
## Statická IP adresace
- musíme nakonfigurovat ručně
- aby se IP adresa neměnila, nebo pokud nefunguje [[Škola/IT/Protokoly/DHCP\|DHCP]]
- Použití:
	- tiskárny
	- servery
	- nepřítomnost [[Škola/IT/Protokoly/DHCP\|DHCP]] serveru
## Dynamická IP adresace
### APIPA

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/apipa/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Automatic Privata IP Address**
- adresu přiděluje operační systém
- použije se v případě, kdy není nastavená statická adresa a systém nemůže najít [[Škola/IT/Protokoly/DHCP\|DHCP]] server

</div></div>

### DHCP

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/dhcp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Dynamic Host Configuration Protocol**
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

## IPv4

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/i-pv4/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Co je IPv4 
- obsahuje ==4 oktety== (desítková soustava) po 8 bitech (binární)
- oktet má hodnotu 0-255
- je ==32 bitová==
- jednotlivé oktety jsou odděleny tečkou - **.**
- příklad IPv4 adresy -> 192.168.0.1 
- **localhost** -> 127.0.0.1
### Privátní IP
- lokální (LAN) síť
- IP adresy se opakují v různých oddělených privátních sítích
### Veřejná IP
- Unikátní na celém světě
- Neopakuje se nikde
- Dostupnost služeb, odkudkoliv na světě
## Maska sítě
- speciální IP adresa
- Rozděluje IP adresu na NET ID a HOST ID
	- maskuje levou část
	- Neměnná: 1 = NET ID 
	- Měnná: 0 = HOST ID 
	- popř SUBNET ID
- 4 oktety, 0-255
- zapisuje se za IP adresu -> říká se jí **prefix**
	- Např. 10.19.0.0 **/16**
- Třídy A, B, C
	- A -> /8
	- B -> /16
	- C -> /24

| Třída | Rozsah veřejných IP adres | Rozsah privátních adres       | Prefix    |
| ----- | :------------------------ | ----------------------------- | --------- |
| A     | 1.0.0.0 - 127.0.0.0       | 10.0.0.0 - 10.255.255.255     | /8 - /15  |
| B     | 128.0.0.0 - 191.255.0.0   | 172.16.0.0 - 172.31.255.255   | /16 - /23 |
| C     | 192.0.0.0 - 223.255.255.0 | 192.168.0.0 - 192.168.255.255 | /24 - 31  |

## Adresa sítě
- Adresa sítě určuje skupinu zařízení v rámci dané sítě
## Broadcast
- Broadcast adresa v IPv4 slouží k odesílání paketů všem zařízením v dané síti najednou
- je to poslední adresa v (pod)síti
## Počítání IPv4
- potřebujeme minimálně 2 bity pro podsítě, jinak budeme mít jednu velkou síť

</div></div>

## IPv6

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/i-pv6/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Co je IPv6
- aktuálně nejnovější verze internetového protokolu
- má 8 hextetů po 16 bitech
- má 128 bitů
- používá šestnáctkovou/hexadecimální soustavu
- jednotlivé hextety jsou odděleny **:**
	- pokud jsou 2 dvojtečky po sobě (Př. **::**), tak to znamená, že je hextet naplněn nulami, lze použít pouze jednou v IP adrese
		- Plná adresa -> 2001:0db8:0000:0000:0000:0000:0000:7334
		- Zkrácená adresa -> 2001:db8::7334
## Druhy 
![Pasted image 20240506195156.png](/img/user/Images/Pasted%20image%2020240506195156.png)
### Unicast adresy
- individuální adresy
- jeden uzel, jedno vybrané zařízení
#### Global unicast adresy
- globální individuální adresy
- jednoznačná identifikace zařízení v celém internetu
- veřejné IPv6 unikátní v celém internetu
##### Části global unicast adresy
###### Prefix
- První část adresy
- určuje síť, ke které zařízení patří
- 48/56/64 bitů
###### Subnet ID
- určuje podsíť, ke které zařízení patří v rámci globálního prefixu
- 16/8/0 bitů
###### Host ID (ID rozhraní)
- identifikuje konkrétní zařízení v síti
- zbývající část adresy
#### Local unicast adresy (ULA)
- mají **host ID** a mohou mít **subnet ID**, pokud je to nutné pro rozlišení podsítě v jedné síti
- Prefix tvoří **ULA prefix** a **ID subnetu (volitelně)**
- Unikátní lokální adresy
- individuální privátní adresy i pro více sítí
- jsou určeny pro privátní adresování v rámci sítě bez nutnosti globální registrace
- začínají sekvencí **fc00**
- Používají se pro:
	- privátní adresování v sítích, které nemají přístup k globálně registrovaným adresám
	- vnitřní komunikace v rámci velkých firem
#### Link-local adresy
- mají **host ID** ale nemají **subnet ID** ani **prefix**
- automaticky vygenerované adresy používané v rámci lokální sítě
- Individuální privátní adresy jen pro danou síť
- nejsou routovány; nemají přístup k routerům
- automaticky se generují na základě MAC adresy
- jsou méně bezpečné, jelikož je snadné je vygenerovat
- začínají sekvencí **fe80::**
- Používají se pro:
	- Automatická konfigurace adres - **SLAAC**
	- Sousedské objevování - NDP
	- lokální komunikace
### Multicast adresy
- Nemají **host ID** ani **subnet ID**
- Prefix tvoří ==rezervovaný multicastový prefix==, který identifikuje skupinu multicastových adres
- adresy určené pro skupinovou komunikaci
- nahrazuje broadcast, který se nachází u [[Škola/IT/IPv4\|IPv4]]
- začínají sekvencí **ff::**
### Anycast adresy
- Nemají **host ID** ani **subnet ID**
- Prefix tvoří ==rezervovaný anycastový prefix==, který identifikuje skupinu anycastových adres
- adresy určené pro ==komunikaci s nejbližším dostupným zařízením== z dané skupiny
- běžně se používají pro servery s replikovanými daty, aby uživatelé byli automaticky směrováni k nejbližšímu dostupnému serveru
- začínají sekvencí **ff::a**

</div></div>
