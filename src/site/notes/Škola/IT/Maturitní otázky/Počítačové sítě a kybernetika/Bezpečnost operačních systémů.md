---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Bezpečnost operačních systémů/","created":"2023-12-14T18:39:26.818+01:00","updated":"2024-04-28T21:34:34.806+02:00"}
---

#IT #Software #Maturitní_otázka #SPOSDK 
## Co je to OS

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/operacni-system/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software #SPOSDK #Maturitní_otázka 
- **Operační systém** (OS) - základní programové vybavení PC
- **Holý počítač** - PC bez os
- Funguje jako rozhraní mezi HW a uživatelem

___
## Funkce OS
### Hlavní funkce
- Ovládání počítače
	- Spouštění aplikací, zapisování textu
	- Umožňuje komunikaci s PC pomocí [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Periferní zařízení\|periferií]]
- Abstrakce [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Hardware\|hardwaru]]
	- Ovládání [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Hardware\|HW]] pomocí OS
	- Např. - změna jasu/hlasitosti
- Správa prostředků
	- Přidělování RAM, disku, procesoru, priorit
### Ostatní funkce
- [[Škola/IT/Hardware/Procesor#Multitasking\|Multitasking]]
- [[Škola/IT/Hardware/Procesor#Multi Threading\|MultiThreading]]
- [[Škola/IT/Hardware/Procesor#Hyper Threading\|Hyper Threading]]
___
## Rozhraní
### **CLI**

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/cli/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> Command line interface

- ==pouze text==, minimální grafika 
- příkazy a argumenty v textovém formátu
- skládá z řádku, do které se zadávají příkazy
- Je náročnější na používání -> vyžaduje znalost příkazů a syntaxe
- Umožňuje rychlé a efektivní provádění úloh, zvláště složitých a opakovaných.

## Příklady
- Terminál v Linuxu
- Příkazový řádek ve Windows


</div></div>

### **GUI**

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/gui/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> Graphical user interface

- Uživatel interaguje s ikonami, tlačítky, menu a dalšími grafickými prvky
- Je **intuitivní** a **snadné** na použítí -> ==vyžaduje minimální znalost== příkazů
- vhodné pro běžné úlohy, ale méně flexibilní pro složitější operace

## Příklady
- Desktopové rozhraní ve Windows
- macOS
- mobilní operační systémy - např. Android, iOS

</div></div>

___
## Obsah OS
### Kernel
- ==Jádro operačního systému==
- Poskytuje nejzákladnější úroveň kontroly HW
	- spravuje přístup k paměti
	- nastavuje provozní stavy procesoru
	- stará se o ukládání dat
### Ovladače
- SW umožňující ovládání HW zařízení
- Poskytuje příkazy pro ovládání HW
- Poskytují abstrakci pro HW

</div></div>

___
## Co je to malware

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/malware/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> zkratka anglického výrazu pro škodlivý software – „malicious software“
-  ==jde o veškerý software, který byl vytvořen se škodlivým záměrem==
- obsahuje celou řadu různých kategorií škodlivého kódu
- škodlivý program se často sám chová tak, aby vám zabránil ve svém odinstalování

___
## Šíření Malwaru
- nejčastěji se šíří přes internet a e-mail
- do zařízení se dostává prostřednictvím:
	- napadených webových stránek 
	- zkušebních verzí her 
	- hudebních souborů 
	- panelů nástrojů 
	- různých programů
	- bezplatných služeb či jakýchkoli stažených dat
	- připojení neznámých USB disků nebo CD
___
## Druhy Malwaru
### Virus
- dokáže se kopírovat a šířit do dalších počítačů
- upravuje legitimní hostitelské soubory nebo programy a spouští svůj kód
- spustí se když uživatel spustí infikovaný program
- dříve byl používán pouze jako vtip
### Trojan
- maskuje se za věrohodný soubor nebo program
- často je škodlivý kód přidaný k normálnímu programu a ==je v něm schovaný==
### Spyware
- tajně sbírá informace o uživateli a jeho zařízení
- data následně odesílá kyberzločinci
### Adware
- Adware je typ bezplatného softwaru, jehož vývoj je podporován reklamou
- Většina adware programů pouze obtěžuje uživatele vyskakovacími okny, ale ==nepředstavuje významné riziko==
### Cryptojacker
- nakažené zařízení tajně těží kryptoměny a posílá je hackerovi
### Worm
- dokáže se sám kopírovat a šířit bez vědomí uživatele
- není závislý na hostitelském souboru
### Rootkit
- program navržený tak, aby mohl bez vašeho vědomí ==získat na vašem počítači přístupová práva administrátora==
- Odhalení rootkitu je velice náročné
- Rootkity se samy o sobě nedokáží šířit
### Ransomware
- odepírá uživateli přístup k jeho zařízením nebo datům 
- šifruje všechny soubory v PC
- chce výkupné za odšifrování
### Keylogger
- dokáže zaznamenat všechny znaky, které napíšete na klávesnici
- zloději mohou procházet veškeré informace, které jste na ==svém počítači napsali, včetně hesel, čísel platebních karet, adres, osobních a emailových zpráv== i zadaných webových stránek
- keylogger je typ spywaru
### Backdoor
- umožňuje útočníkovi připojit se bez autorizace a vědomosti majitele
- obchází normální zabezpečení, což umožňuje útočníkovi nebýt detekován
___
## Známky nakažení malwarem
- zpomalený počítač
- ==neznáme procesy== běžící na pozadí
- časté pády systému
- vyskakovací okna
- podivné chování ve vašem internetovém prohlížeči
-  ==vyšší spotřeba paměti== nebo mobilních dat
___
## Odstranění malwaru
### Automaticky
- malware pomůže odstranit bezpečnostní program
- možnost nastavit automatické skenování a aktualizace, díky kterým budete chráněni před nejnovějšími hrozbami i v budoucnu.
### Manuálně
- je podstatně složitější
- zkuste spustit zařízení v nouzovém režimu a odebrat aplikaci, která podle vás způsobuje nestandardní chování

___
## Chránění před nakažením malwarem
- Používejte účinný antivirový a antimalwarový software
- Neotvírejte emailové přílohy od neznámých nebo neočekávaných odesilatelů
- ==pravidelné aktualizace== operačního systému
- Pravidelně zálohovat svoje [[Škola/IT/Data\|data]]
- Používání zdravého rozumu
	- 

</div></div>

___
## Prevence napadení
### Pravidelné aktualizace
- Absolutně **klíčový** prvek bezpečnosti
- Aktualizace celého OS i aplikací
- Aktualizace ==opravuje bezpečností díry== v předešlých verzích OS a zlepšují chod SW
### Antivirus/Antimalware

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

### Firewall

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

### Bezpečnostní politika

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
## Fyzická bezpečnost

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/fyzicka-bezpecnost/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




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

</div></div>

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

### VPN

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/vpn/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




-> **Virtual Private Network**

- "skryje" váš internet traffic (internetový provoz)
- šifruje vaše data, takže je nikdo nemůže vidět, ani váš poskytovatel internetu nebo někdo na veřejné Wi-Fi síti
- Poskytovatel VPN ovšem pořád data vidí, je proto důležité vybrat kvalitního poskytovatele, který data nebude prodávat ani jinak šířit
- Je také možné použít VPN pro připojení 2 počítačů z různých sítí na jednu stejnou LAN

</div></div>
