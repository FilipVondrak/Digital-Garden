---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Úvod do kybernetické bezpečnosti/","created":"2023-12-14T18:23:42.725+01:00","updated":"2024-05-14T20:09:05.283+02:00"}
---

#IT #Maturitní_otázka 
**Zakladatel:** [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Norbert Wiener\|Norbert Wiener]]
**Vznik názvu:** v roce 1948 z řeckého slova κυβερνητικός [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/kybernētikós\|kybernētikós]]
**Zabývá se procesy** - postup(navazuje na sebe) - přenos informací

> [!tldr]
>  věda, která se zabývá obecnými principy řízení (procesy) a přenosu informací ve strojích, živých organismech a společenstvích
# Aktiva

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/aktiva/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- něco, co je pro mě důležité, snažíme se je chránit
- Majetek, důležité pro určitý objekt
## Typy aktiv
### Primární 
- linka, nemocnice-důvěra, vědomosti
- aktiva, která mají pro provoz organizace zásadní hodnotu
### Podpůrná
- lidi, škola-žáci, informace
- aktiva, která zajišťují správné fungování primárních aktiv
### Technická
- síť, server, PC
## Dělení aktiv
### Hmotné
- stroje, suroviny, fyzické sítě
- technické vybavení, prostředky, systému ve kterých jsou umístěny informační systémy primárních a podpůrných aktiv
### Nehmotné
- znalosti, služby, [[Škola/IT/Data\|Data]] a [[Škola/IT/Informace\|Informace]]

</div></div>


# Důležité termíny 
### Feedback 
- zhodnocení něčeho
### Zpětná vazba 
- změna, v reakci na feedback (př. Uživatel mojí aplikace dá feedback o tom že nefunguje nějaká funkce, já jí spravím - zpětná vazba)
- výstup nějakého systému ovlivňuje zpětně jeho vstup
### Riziko
- možnost, že hrozba využije zranitelnosti (může, ale nemusí)
### Bezpečnostní událost 
- Může způsobit narušení bezpečnosti informací v informačních systémech, služeb popř. bezpečnosti a integritu, nezpůsobí velké škody
### Bezpečnostní incident
- Narušení bezpečnosti informací v informačních systémech nebo narušení bezpečnosti služeb
### Model 
- má napodobit chování něčeho, v menším měřítku např. model budovy, v kyb příklad model útoku

# Kyberprostor

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/kyberprostor/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




=> **nehmotný svět vytvořený vzájemným propojením počítačových, informačních a komunikačních systémů**

- Poskytuje prostředí, kde je možná komunikace napříč celým světem
- Prostor, kde je možné vytvářet, uchovávat, využívat a vzájemně si vyměňovat informace

# Ochrana kyberprostoru
- S rostoucím dosahem internetu vznikla nutnost pravidel a regulace kyberprostoru na úrovni státu, která se projevila v České republice zákonem. Dále v Evropské unii směrnicí.
- O zabezpečení kyberprostoru se v česku starají [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/CERT a CSIRT týmy a jejich využití\|CERT a CSIRT týmy]]
# Kyberkriminalita
- S kyberprostorem se ale úzce váže kyberkriminalita
- S příchodem AI je kriminalita dostupnější a rozšířenější i pro ty méně nadané kriminálníky

</div></div>


# Hoax

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



=> **záměrně vytvořený podvod, vydávající se za pravdu**
- Mohou to tedy být:
	 - falešná zpráva
	 - propaganda
	 - mystifikace
	 - poplašná zpráva

## Jak rozpoznat hoax?
- **Zdroj zprávy**
	- pokud se jedná o známí a důvěryhodný web, zpráva je pravděpodobně dobrá
	- zkontrolovat [[Škola/IT/Informace\|informaci]] z více zdrojů
- **Zkontrolujte datum**
	- Někdy se šíří staré zprávy jako aktuální
- **Obrázky a videa**
	- Nevypadá fotka upravená/vygenerovaná?

</div></div>


# Kybernetická hrozba

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- ==potencionální příčina kyb. bezpečnostní události/incidentu jejímž výsledkem může (ale nemusí) být poškození aktiva==
- získání cenných informací
- několik škodlivých částí(obejít bezpečnostní opatření organizace)
- průzkum zdrojů informace
## Hrozby - dělení
### Dle zdroje
- Vnitřní - zaměstnanec, technická vada, někdo něco ukradne…
- Vnější útoky - hackeři, živelné pohromy…
### Dle úmyslu
- Náhodné hrozby - výpadek proudu..
- Neúmyslné hrozby - smazání souboru, prozrazení informací
- Úmyslné hrozby - úmyslné poškození, krádež, útoky, …

</div></div>

# Malware a útoky

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


# Informace

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/informace/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- nějaký údaj
- může se měnit a číst
- má svůj životní cyklus

![](https://lh7-us.googleusercontent.com/bcgZZIbPRXZbF-1JFXTrkwxea2T7mc225zTLGI2nYyGbnyLVavdfuYENf9L-luqLNlxjR1UQGkiKIpsc5jACbyrWzGVFx8JzzXWA3UBiLknmbKELl8FifhsxnafYpiVl6YEe_C8Gs7iW4-3Uuh-kQkQ)

</div></div>
