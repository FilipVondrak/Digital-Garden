---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Revitalizace sítě po napadení sítě/","created":"2023-12-14T18:25:01.841+01:00","updated":"2024-04-28T21:34:34.835+02:00"}
---

# Počítačová síť

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Propojení dvou a více zařízení za účelem vzájemné komunikace, výměny dat a HW prostředků

</div></div>

# Co je to kybernetický útok?

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/kyberneticky-utok/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software #Malware

- Úmyslné jednání útočníka v [kyberprostoru](Kyberprostor.md)
- Hlavní motivací je většinou zisk (informací, prostředků, dat)
- Jednotlivec nebo skupina
- **Dělí se na:**
    - **Pasivní**
        - Skenování portů, keylogger
    - **Aktivní**
        - DDoS, Man in the middle
        - Útok na síť a zisk citlivých informací
    - **Vnitřní**
        - Zaměstnanci/uživatelé systému napadnou systém
            - Nevědomě nebo omylem
            - Vědomě kvůli pomstě, špionáži
    - **Vnější**
        - Útok z vnějšku sítě
    - **Fyzický**
        - Vloupání do budovy a krádež dokumentů, HW
    - **Síťový**
        - Napadení sítě a krádež či zneužití aktiv

## Typy útoků
### Zero day attack
### DDOS


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
