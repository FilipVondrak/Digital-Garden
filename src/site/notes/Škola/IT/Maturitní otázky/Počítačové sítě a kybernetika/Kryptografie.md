---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Kryptografie/","tags":["IT","Maturitní_otázka"],"created":"2023-12-14T18:24:26.512+01:00","updated":"2024-05-23T14:12:26.716+02:00"}
---

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
- odesílatel i příjemce musí mít ten klíč
- Např.:
	- Morseovka 
	- Caesarova 
	- Enigma
### Asymetricky
- 2 různé klíče - jeden privátní a jeden veřejný
- Fungování
	- 1 veřejný – šifruje
		- Osoba má na IG v biu veřejný klíč, pomocí tohoto klíče já zašifruji data a pošlu mu je
	- 1 privátní – dešifruje
		- Osoba data rozšifruje svým privátním klíčem
## Podle fungování šifry
### Transpoziční šifra
- posouvá písmena s pomocí klíče
### Substituční
- 
> [!example]- Ukázka
> klíč: DADE  
slovo k zašifrování: SLOVO  
určíme pozice klíče => D je na 4. pozici v abecedě, A je na 1., D opět na 4. a E na 5.  
poté posuneme písmena o počet pozicí z klíče  
S posuneme o 4 pozice dopředu => W  
L => M |
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