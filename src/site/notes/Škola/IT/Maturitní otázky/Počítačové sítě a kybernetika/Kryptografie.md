---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Kryptografie/"}
---

#IT #Maturitní_otázka
- Nauka o metodách ==utajování smyslu zpráv převodem do podoby, která je čitelná jen se speciální znalostí==.
- Zabývá se algoritmem pro ==šifrování a dešifrování==
- o šifrování se stará 4. [vrstva](ISO%20OSI.md) 
- elektronický podpis - nahrazují klasický vlastnoruční podpis, respektive ověřený podpis. Je připojen k datové schránce
- Např. **ceasarova** šifra
- **Použití:**
	- všude
	- komunikace
	- šifrované služby
	- elektronické podpisy
	- zabezpečení mobilů
	- šifrování dat na disku
	- certifikáty
# Druhy šifrování
## Podle toho, co šifruje
- Hardwarově
	- ==probíhá v čipu(TPM)==
	- hardwarově zašifrovaný disk je **nepřenositelný** do jiného zařízení
- Softwarově
	- ==probíhá v softwaru se speciálním programem==
	- zašifrování a dešifrování použiju stejný program
## Podle způsobu šifry
- Symetricky
	- Šifruje se a dešifruje se stejným klíčem
- Asymetricky
	- Šifruje se veřejným klíčem a dešifruje se privátním klíčem

# Steganografie
- **Podobor** kryptografie
- zabývající se utajením komunikace prostřednictvím ukrytí zprávy
- Např. neviditelný inkoust, vyrývání zprávy do dřevěné tabulky, která se zalije voskem apod
- nahrazena kryptografií po 2. světové válce
- zpráva ==zůstává ve stejné podobě== na rozdíl od kryptografie

# Hashování
- na rozdíl od šifrování se nedá vrátit zpět do původní podoby
- funguje jako fingerprint souboru/textu
- převod vstupních [dat](Data.md) do (relativně) malého čísla
- ==jakékoliv množství vstupních dat poskytuje stejně dlouhý výstup (otisk)==
- **Použití**
	- rychlejšímu prohledávání tabulky
	- hledání malware antivirovým programem
	- vytváření a ověřování elektronického podpisu
	- zajištění integrity dat
	- ochrana uložených hesel
- 