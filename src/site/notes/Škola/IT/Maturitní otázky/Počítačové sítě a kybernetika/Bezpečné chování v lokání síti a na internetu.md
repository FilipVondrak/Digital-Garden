---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Bezpečné chování v lokání síti a na internetu/","created":"2023-12-14T18:23:52.676+01:00","updated":"2024-05-01T22:33:57.740+02:00"}
---

# Co je to lokální síť

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


# Bezpečné chování v lokální sítí
## Dodržovat firemní politiku

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





> [!Info]
Dokument, soubor pravidel pro všechny uživatele v organizaci
=> tyto pravidla se vztahují spíše pro firmy, organizace nebo větší sítě

- Obsahuje:
	- Doporučení 
	- zákazy 
	- postupy v různých situacích
- Rozděluje zaměstnance do určitých skupin -> určení práv v síti
- Určuje zálohu hesel a jejich aktualizace
# Pravidla pro účty
- ADMIN -> nejvyšší práva v síti, ke své práci by neměl využívat admin účet
- USER  -> pravidla jak vytvořit heslo a uživatelské jméno: příjmení + iniciál
# Fyzická bezpečnost
- Zabezpečení budovy, vstupů a místností -> klíč, čip, biometrika
- Ochrana techniky
	- kamerový systém

</div></div>


# Co je to internet

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/internet/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- zařízení mimo lokální síť
- **WAN** - Wide area network
- tvořen [routery](Router.md), [servery](Server.md)
- obrovská síť propojených zařízení bez centrálního bodu
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


___
# Bezpečné chování na internetu
- Mezi základní věci, co by měl každý uživatel internetu mít/dodržovat patří:
## Antimalware

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Identifikuje a odstranění většinu malwaru
- Nutné pravidelné aktualizace kvůli aktuální virové databázi
- Je to software, který se stará o ochranu před malwarem
- porovnává kód programů ==se svojí databází== virů
- Novější verze mají AI, která rozpoznává nové malwary
## Funkce anti malwaru
### Kontrola
- kontrola souborů před viry
### Nalezení škodlivého kódu
- hledání a mazání malwaru
### Heuristická analýza
- pokus detekovat dosud neznámé viry a varianty již známých virů 
### Sandbox
- izolace programu, aby se otestovalo jeho chování v systému
- např. pokud si nejsme jistí či aplikace obsahuje malware, tak ji můžeme spustit v sandboxu a hlídat její chování
### Whitelist
- povolení pouze určitých aplikací
### Blacklist
- zakázání určitých aplikací

</div></div>

## Pravidelně updatovaný software
- Pravidelné aktualizace softwaru nám zaručují opravy bezpečnostních děr
- Kontrolovat nastavení FIREWALLu
- Je nebezpečné používat starší verze softwaru
## Webová bezpečnost
- Navštěvovat jen zabezpečené stránky ([[Škola/IT/HTTPS\|HTTPS]])
- na nezabezpečených ([[Škola/IT/HTTP\|HTTP]]) už vůbec nezadávat žádné informace, jejich přenos ==není zabezpečený ==
- Nesdílet osobní nebo citlivé údaje **nikde**
- ==Neotvírat podezřelé odkazy==
- Nestahovat podezřelé přílohu mailu a neznámé aplikace
- Vyvarovat se stahování nelegálních softwarů - obsahují mnoho malwaru
- Pravidelně mazat Cookies
## Autentizace 
- Mít silné heslo 
	- alespoň 8 znaků
	- aby obsahovalo čísla, písmena i znaky
	- Frázové heslo => snadno zapamatovatelná fráze => "NeníT0P0c3stný?{sposdk}"
- Pravidelně měnit, aktualizovat hesla
- Nepoužívat stejná hesla na jiných platformách
- Používat dvoufázové ověření 
## Zálohování
- Zálohujeme důležitá data
- nejlépe použijeme několik možností zálohy
- zálohovat lze celý systém
- způsoby zálohy
	- Lokálně na disk
	- Na cloudu

## Dodatečná ochrana na internetu
### Používání VPN

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/vpn/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Virtual Private Network**

- "skryje" váš internet traffic (internetový provoz)
- šifruje vaše data, takže je nikdo nemůže vidět, ani váš poskytovatel internetu nebo někdo na veřejné Wi-Fi síti
- Poskytovatel VPN ovšem pořád data vidí, je proto důležité vybrat kvalitního poskytovatele, který data nebude prodávat ani jinak šířit
- Je také možné použít VPN pro připojení 2 počítačů z různých sítí na jednu stejnou LAN

</div></div>

### Používat TOR

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



-> **The Onion Router**

- je ==bezplatný a open-source== software, který umožňuje anonymní komunikaci na internetu
- váš internetový provoz přesměrovává přes síť dobrovolnických serverů po celém světě
- Nikdo z jednotlivých serverů nevidí celou trasu ani obsah vašich dat.

## Výhody TORu
### Zvýšení vašeho soukromí online
- Ztěžuje sledování vaší internetové aktivity
### Pomáhá obcházet centuru
- Můžete jej použít k přístupu na webové stránky, které jsou ve vaší zemi blokované
- V zemích s vysokou cenzurou lze využít TOR k přístupu ke zprávám ze zbytku světa

## Nevýhody TORu
### Je velmi pomalý
- Přesměrování provozu přes síť serverů velmi zpomaluje rychlost
- Otevření i jednoduchého webu může trvat velmi dlouho
### Využívá se pro nelegální aktivity
- Anonymita Toru je lákavá pro ty, kteří chtějí podnikat online nezákonné činnosti
### Není 100% bezpečný
- Stále existují způsoby, jak vás potenciálně sledovat, pokud někdo má dost velké schopnosti

![Pasted image 20240501221600.jpg](/img/user/Images/Pasted%20image%2020240501221600.jpg)

</div></div>


## Virtuální počítač
- Je to software, díky kterému je možné běžet druhý operační systém oddělený od vašeho počítače
- pokud by se útočník nebo malware dostal do virtuálního počítače, tak je velmi lehké ho smazat a znovu vrátit do původního stavu
- Po spuštění virtuálního počítače je potřeba dost velká výpočetní síla; ne každý počítač dokáže spustit dva operační systémy naráz
