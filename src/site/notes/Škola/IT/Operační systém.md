---
{"dg-publish":true,"permalink":"/Škola/IT/Operační systém/","created":"1980-01-01T00:00:00.000+01:00","updated":"2024-03-18T08:54:44.477+01:00"}
---

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