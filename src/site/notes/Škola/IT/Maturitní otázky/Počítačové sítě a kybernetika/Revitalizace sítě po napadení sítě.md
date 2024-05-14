---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Revitalizace sítě po napadení sítě/","created":"2023-12-14T18:25:01.841+01:00","updated":"2024-04-28T21:34:34.835+02:00"}
---

# Počítačová síť

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Propojení dvou a více zařízení za účelem:
	- vzájemné komunikace
	- výměny dat 
	- sdílení HW prostředků

</div></div>

# Co je to kybernetický útok?

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/kyberneticky-utok/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- Úmyslné jednání útočníka v [kyberprostoru](Kyberprostor.md)
- Hlavní motivací je většinou zisk (informací, prostředků, dat)
- Jednotlivec nebo skupina
## Dělení
### Podle aktivity
#### Pasivní
- Skenování portů, keylogger
#### Aktivní    
- DDoS, Man in the middle
- Útok na síť a zisk citlivých informací
### Zdroje útoku
#### Vnitřní
- Zaměstnanci/uživatelé systému napadnou systém
    - Nevědomě nebo omylem
    - Vědomě kvůli pomstě, špionáži
- vynášení dat
#### Vnější
- Útok z vnějšku sítě

### Typu útoku
#### Fyzický
- Vloupání do budovy a krádež dokumentů nebo/a HW
- fyzické poškození
#### Síťový
- Napadení sítě a krádež či zneužití aktiv

## Typy útoků
### Zero day attack
### DDOS
- nepoškození Aktiva
- server nereaguje na požadavky uživatele
### SQL Injection


</div></div>


___
# Revitalizace sítě
1. oddělit zdravou část sítě od poškozené
2. zkontrolovat jestli tam útočník někde nemá zadní vrátka a diagnostikovat hrozbu
3. obnova: (vysvětlit jednotlivé napadení)
	- **po viru**
		- Smazat ho, sken antimalwerem
		- případně bod obnovy
	- **po trojském koni**
		- smazat ho a celou aplikaci
		- škodlivý kod skrytý v aplikaci, která vypadá užitečně, množí se
	- **po ransomwaru**
		- tovární nastavení / obnova ze zálohy
4. najít díry a ošetřit je (zjistit jak se tam útočník dostal)

___
# Také vysvětlit

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/firemni-politika/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





> [!Info]
Dokument, soubor pravidel pro všechny uživatele v organizaci
=> tyto pravidla se vztahují spíše pro firmy, organizace nebo větší sítě

- Elektronický nebo tištěný dokument -> 1 velká směrnice, obsahuje další směrnice
- Rozděluje zaměstnance do určitých skupin -> určení práv v síti
- Určuje zálohu hesel a jejich aktualizace
- za všechno v síti odpovídá ředitel organizace
# Co obsahuje
- potřebnou složitost hesel zaměstnanců
- pravidla na stahování softwaru
- Bezpečné chování zaměstnance -> Doporučení a zákazy, které by uživatel měl respektovat
- postupy v různých situacích
- práva určitých skupin zaměstnanců
- 
# Pravidla pro účty
## ADMIN 
- nejvyšší práva v síti
- ke své práci by neměl využívat admin účet, pokud to není zapotřebí
- Hesla ke všemu v síti mít zálohované
	- např. v obálce zamčené v trezoru
### Enterprise Admin
- práva SYSTEM
### Domain Admin
- Odpovídá za vše, ale ředitel je zodpovědný za něj
- nastavuje síť
	- funkčnost
	- konfigurace
## USER  
- pravidla jak vytvořit heslo a uživatelské jméno -> např. příjmení + iniciál
- pouze oprávnění, která potřebuje k práci

___
# Fyzická bezpečnost
- Zabezpečení budovy, vstupů a místností -> klíč, čip, biometrika
## Ochrana techniky
- kamerový systém
- Rackové skříně
	- Zamknout
	- Kovová páska/lanko
	- Dát je do výšky, aby nebyli lehce přístupné
	- přidělat napevno, aby je nebylo možné odnést
## Servery
- zabezpečený přístup
- nezveřejňovat umístění serverovny
## Klientské stanice
- Na pevno přidělané
- Notebooky do dokovací stanice se zámkem -> Kensington lock
## Kabeláž
- Zabudovat do zdi
- V liště
## Energie
- chránit napájení
- mít záložní zdroj energie
___
# Softwarová bezpečnost
## Firewall

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/firewall/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





> [!TIP]
> Zjednodušeně si funkci můžeme představit jako **stráže vstupu do pevnosti**, které podle příkazů rozhodují o tom, **koho pustí dovnitř a ven**
> 

- je to bezpečnostní systém
- **zkoumá** a **omezuje** síťový provoz ==na základě předdefinovaných nebo dynamických pravidel== a politik
- může být jak ==software tak i hardwarové zařízení==
- filtruje příchozí a odchozí komunikaci mezi důvěryhodnou a nedůvěryhodnou sítí
- chrání zařízení, jež jsou zapojena za ní, před různými typy útoků, včetně těch, které umožní útočníkovi převzít kontrolu na zařízením
- může ==zablokovat škodlivou nebo nechtěnou odchozí komunikaci== způsobenou činností [[Škola/IT/Malware\|malwaru]]
	- Například v případě, kdy se infikovaný počítač snaží připojit do botnetové sítě nebo na řídící server pod kontrolou útočníka.

## Druhy firewallu
### Síťový
- samostatné hardwarové řešení pro ochranu počítačové sítě
- je prvním filtrem příchozí komunikace
### Personální
- realizován na koncových stanicích (počítačích)
- většinou jako součást bezpečnostního řešení

> [!info]- Fun Fact
> První komerční firewall vyvinula na konci osmdesátých let společnost Digital Equipment Corporation (DEC).
> Technologie nabyla na významu s masivním rozšířením internetu a překotným vývojem nových digitálních hrozeb.


</div></div>

## Monitorovací systémy
- Pravidelné kontroly a aktualizace
### SIEM

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/siem/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> *Security Information and Event Management*
- kombinuje security information management (*SIM*) a security event management (*SEM*) do jednoho
- analyzuje s zpracovává logy z infrastruktury firmy
- používá analytika, strojové učení a algoritmus na rozpoznávání podle pravidel k identifikaci [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Úvod do kybernetické bezpečnosti#Kybernetická hrozba\|hrozeb]]
- poskytuje real-time upozornění
- hlavní účel je centralizované a detailní zabezpečení
- Je profesionální
- Drahý
- má automatizované metody

</div></div>

### LogManagement

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/log-management/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- levný
- oblíbený firmami

</div></div>

## VPN

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/vpn/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Virtual Private Network**

- "skryje" váš internet traffic (internetový provoz)
- šifruje vaše data, takže je nikdo nemůže vidět, ani váš poskytovatel internetu nebo někdo na veřejné Wi-Fi síti
- Poskytovatel VPN ovšem pořád data vidí, je proto důležité vybrat kvalitního poskytovatele, který data nebude prodávat ani jinak šířit
- Je také možné použít VPN pro připojení 2 počítačů z různých sítí na jednu stejnou LAN

</div></div>

## Šifrování dat

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


</div></div>


___
# Postup kybernetického útoku

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




1.  **Observace**
	- Snaha objevit slabiny
	- probíhá z venku
2.  **Analýza sítě**
	- Lokalizace aktiv
	- probíhá uvnitř
3.  **Příprava útoku**
	- Příprava programů(exploitů) a dalšího nářadí pro provedení útoku
4.  **Samotný útok**
	- Napadení sítě, vniknutí do budovy
5.  **Mazání stop**
	- Mazání logů, kamerových záznamů, otření otisků prstů

</div></div>
