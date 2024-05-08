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

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/sifrovani/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# Způsoby šifrování dat
- **Podle Implementace**
	- [Softwarově](Softwarové%20šifrování.md)
	- [Hardwarově](Hardwarové%20šifrování.md)
- **Podle šifry**
	- [[Škola/IT/Symetrické šifrování\|Symetrické šifrování]]
	- [[Škola/IT/Asymetrické šifrování\|Asymetrické šifrování]]

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


</div></div>
