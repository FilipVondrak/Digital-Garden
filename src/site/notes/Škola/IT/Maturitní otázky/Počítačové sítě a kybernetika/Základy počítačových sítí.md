---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Základy počítačových sítí/","tags":["IT","SPOSDK","Maturitní_otázka"],"created":"2023-12-14T18:39:48.640+01:00","updated":"2024-05-08T17:09:44.308+02:00"}
---

## Co jsou počítačové sítě
- síť je vzájemné propojení 2 a více zařízení za účelem komunikace
### LAN

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




- LAN (Local area network)
- místní síť
- stará se o ní admin
- **je tvořena:**
	- koncovými zařízeními
	- [switch](L3%20switch.md), [routery](Router.md)
- používá se v domech nebo menších firmách
- nachází se za routerem
- **Síť ve firmě **- klient->server
- **Síť doma** - klient-klient (peer to peer)

</div></div>

### Internet

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/internet/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# Co je internet
- zařízení mimo lokální síť
- **WAN** síť - Wide area network
- tvořen [routery](Router.md), [servery](Server.md)
- obrovská síť propojených zařízení bez centrálního bodu
# Bezpečnost na internetu
- Nesdělovat o sobě informace
	- jméno
	- lokaci
	- atd. ..
- Navštěvovat pouze ověřené a zabezpečené stránky (HTTPS)
- Využívat zabezpečené služby
- využívat vícefázové ověření
- neukládat cookies
- neklikat na neznámé/podezřelé odkazy
- kontrolovat adresní řádek
- nestahovat obsah z neověřených zdrojů, kvůli riziku [[Škola/IT/Malware\|malwaru]]
	- pirátské kopie
	- ilegální software
## Bezpečné heslo
### Složitost hesla
- Dlouhé heslo, alespoň 12 znaků
### Unikátní
- neopakovat heslo mezi službami
- vybrat heslo, které nelze lehce vymyslet
# Dělení internetu
## Surface web
- Veřejně přístupný web
- je indexován webovými prohlížeči
## Deep Web
- je k němu často potřeba heslo
- není veřejně přístupný
- např. emailová schránka
## Dark Web
- nutnost speciálního softwaru pro přístup (např. TOR)
- často se zde dějí nelegální věci (např. prodej drog)
- nelze otevřít normálním webovým prohlížečem
___
![Pasted image 20231218170915.png](/img/user/Images/Pasted%20image%2020231218170915.png)

</div></div>

# Bezpečná komunikace

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/maturitni-otazky/pocitacove-site-a-kybernetika/bezpecna-komunikace/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- Jsou zachovány CIA (Confidentiality, Integrity, and Availability) principy
    - **Důvěrnost**
        - Do komunikace nevstupuje žádní neoprávněná třetí strana
    - **Integrita**
        - Nedochází k neoprávněné úpravě [[Škola/IT/Data\|dat]]
    - **Dostupnost**
        - Data i systémy jsou dostupné
- Komunikující strany si musí být jisté, že nejsou odposloucháváni nebo narušeni

___
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

___
# Způsoby narušení komunikace
### Man in the middle

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Komunikace je odposlouchávána třetí stranou
- Není nutné být uprostřed na fyzické cestě (komunikace se dá přesměrovat)
- **Jak se bránit?**
    - Koncové šifrování komunikace

</div></div>

### Phishing

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Někdo cizí se vydává za příjemce zprávy
- Falešné stránky, které vypadají jak ty pravé (Internetové bankovnictví, sociální sítě)
- Šíří se e-maily
- **Jak se bránit?**
    - Kontrolovat certifikáty stránky
    - Kontrolovat název domény
    - Kontrolovat odesilatele e-mailu

</div></div>

### Fyzická krádež korespondence

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




- Odcizení dopisu/dat pro určitou osobu na přenosovém médiu
- **Jak se bránit?**
    - Fyzické zabezpečení - zamknout do stolu/trezoru
    - Používat [[Škola/IT/Šifrování\|Šifrování]]/zabezpečení - šifrovat data na flashce a mít na ní biometriku

</div></div>

___
# Zabezpečení komunikace
- Využití [kryptografie](Šifrování.md) - šifrování (ot.5)
- Užití digitálních certifikátů a podpisů
    - ověření komunikujících subjektů
- Dodržovat [obecnou bezpečnost na sítí](Bezpečné%20chování%20v%20lokání%20síti%20a%20na%20internetu.md) (ot.2)

___
# Šifrování

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/sifrovani/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# Co je to šifrování
- převod dat do nečitelné podoby pro lidi, kteří nemají klíč/neví jak je vrátit zpět
- dají se opačným postupem vrátit do původní podoby
- šifrování se děje na 6. vrstvě [[Škola/IT/ISO OSI\|ISO OSI]]
# Způsoby šifrování dat
- **Podle Implementace**
	- [Softwarově](Softwarové%20šifrování.md)
	- [Hardwarově](Hardwarové%20šifrování.md)
- **Podle šifry**
	- [[Škola/IT/Symetrické šifrování\|Symetrické šifrování]]
	- [[Škola/IT/Asymetrické šifrování\|Asymetrické šifrování]]
# Jak softwarově šifrovat 
### Bitlocker

# End-to-end šifrování
- Přenos dat ochráněn proti odposlechu
- Šifrování po celé cestě dat
    - Od klienta na server i ze serveru na dalšího klienta a od klienta ke klientovi
    - Může odposlouchávat dále, ale jen šifrované data
## OpenPGP
- End-to-end pro e-mail
- Digitální podpisy
- Šifrované e-mailové zprávy
## S/MIME
- Kryptografické zabezpečení pro e-maily
    - Autentizace (podpis)
    - Integrita zpráv
    - Zabezpečení dat (šifrování)

## OTR
- Šifrování pro instant messaging
- Používá symetrickou šifru
- Zabezpečuje
    - Autentizaci
    - Šifrování
    - Dopředná bezpečnost - starší zprávy budou stále zašifrované

</div></div>
____

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/maturitni-otazky/pocitacove-site-a-kybernetika/kryptografie/#elektronicky-podpis" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



# Elektronický podpis
- nahrazují klasický vlastnoruční podpis, respektive ověřený podpis. 
- Je připojen k datové schránce

![elektronický podpis.png](/img/user/Images/elektronick%C3%BD%20podpis.png)
___

</div></div>


# TLS

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/kybernetika/tls/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

<div class="markdown-embed-title">

# TLS

</div>



-> *Transport Layer Security*
- používá různé šifry a šifrovací sady, které definují konkrétní algoritmy pro šifrování, autentizaci, výměnu klíčů a integritu dat
- kryptografický protokol sloužící k zabezpečení komunikace v počítačových sítích
- TLS je nástupcem [[SSL\|SSL]]
## Hlavní účely
### Šifrování
- Zabezpečují data přenášená mezi klientem (např. webovým prohlížečem) a serverem tak, že jsou nečitelná pro třetí strany
### Autentizace
- Zajišťují, že obě strany komunikace (klient a server) jsou skutečně tím, kým tvrdí, že jsou
- dosahuje toho pomocí digitálních certifikátů, které ověřují identitu serveru (a někdy i klienta)
### Integrita dat
- Zajišťují, že data nebyla během přenosu změněna nebo poškozena
- Používají se hashovací funkce, které ověřují integritu přenášených dat

</div></div>

___
# SOC

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/kybernetika/soc/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> 

</div></div>


</div></div>
