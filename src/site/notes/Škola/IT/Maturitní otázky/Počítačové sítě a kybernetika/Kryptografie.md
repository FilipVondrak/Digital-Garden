---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Kryptografie/","created":"2023-12-14T18:24:26.512+01:00","updated":"2024-03-25T16:16:25.662+01:00"}
---

#IT #Maturitní_otázka

> [!info] 
>  kryptografie je věda, která se zabývá konstrukcí matematických metod, sloužících k zajišťování bezpečnosti dat

> [!tldr]-
> Citlivá data mohou být díky kryptografii bezpečně přenášena prostřednictvím telekomunikačních sítí bez hrozby neoprávněného zachycení a rozluštění obsahu dat.
> 

- Nauka o metodách ==utajování smyslu zpráv převodem do podoby, která je čitelná jen se speciální znalostí==.
- Zabývá se algoritmem pro ==šifrování a dešifrování==
- Např. **ceasarova** šifra
- **Použití:**
	- všude
	- komunikace
	- šifrované služby
	- elektronické podpisy
	- zabezpečení mobilů
	- šifrování dat na disku
	- certifikáty
___
# Druhy šifrování
## Podle toho, co šifruje
### Hardwarově
- ==probíhá v čipu(TPM)==
- hardwarově zašifrovaný disk je **nepřenositelný** do jiného zařízení
### Softwarově
- ==probíhá v softwaru se speciálním programem==
- zašifrování a dešifrování použiju stejný program
## Podle způsobu šifry
### Symetricky
- Šifruje se a dešifruje se stejným klíčem
### Asymetricky
- Šifruje se veřejným klíčem a dešifruje se privátním klíčem
## Podle fungování šifry
### Transpoziční šifra
- posouvá písmena s pomocí klíče
> [!example]- Ukázka
> klíč: DADE  
slovo k zašifrování: SLOVO  
určíme pozice klíče => D je na 4. pozici v abecedě, A je na 1., D opět na 4. a E na 5.  
poté posuneme písmena o počet pozicí z klíče  
S posuneme o 4 pozice dopředu => W  
L => M |
### Substituční

___
# Steganografie
- **Podobor** kryptografie
- zabývající se utajením komunikace prostřednictvím ukrytí zprávy
- Např. neviditelný inkoust, vyrývání zprávy do dřevěné tabulky, která se zalije voskem apod
- nahrazena kryptografií po 2. světové válce
- zpráva ==zůstává ve stejné podobě== na rozdíl od kryptografie

___
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

___
# Elektronický podpis
- nahrazují klasický vlastnoruční podpis, respektive ověřený podpis. 
- Je připojen k datové schránce
![elektronický podpis.png](/img/user/Images/elektronick%C3%BD%20podpis.png)

___
# Kódování
- proces převodu dat do formátu, který může být snadno **ukládán** nebo **přenášen**
- ==není bezpečný== jako šifrování, ==není těžké převést data do původní podoby==
## Použití
### Ukládání dat 
- Komprese dat se používá k úspoře úložného prostoru
### Multimediální data
- používá se ke snížení velikosti multimediálních souborů, jako jsou obrázky, zvukové soubory a video soubory

___
# Paritní bit