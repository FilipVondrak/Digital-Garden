---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Zabezpečení dat proti zneužití/","created":"1980-01-01T00:00:00.000+01:00","updated":"2024-03-18T08:54:51.055+01:00"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/data/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- zdroj z něhož se tvoří informace (aktiva)
- nutnost chránit před zneužitím
# Typy dat:
- **Digitální** 
	- zapsané v počítači, 
	- uložené na disku/flešce
	- tvořeny z jedniček a nul
- **Fyzické**
	- zapsané na papíře
# Co to jsou data? (rozdíl mezi daty a informacemi):

## Data
- Data nemají na rozdíl od informací životní cyklus,
- Informace jsou již ==zpracovaná data==,
- ==Data jsou vždy pravdivá==, informace být nemusí
## Informace

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- nějaký údaj
- může se měnit a číst
- má svůj životní cyklus

![](https://lh7-us.googleusercontent.com/bcgZZIbPRXZbF-1JFXTrkwxea2T7mc225zTLGI2nYyGbnyLVavdfuYENf9L-luqLNlxjR1UQGkiKIpsc5jACbyrWzGVFx8JzzXWA3UBiLknmbKELl8FifhsxnafYpiVl6YEe_C8Gs7iW4-3Uuh-kQkQ)

</div></div>


</div></div>


**Co je to bezpečnost** - Bezpečnost znamená dodržování pravidel, [směrnic](Směrnice.md), zákonů, atd..
**Co je to zneužití** - Poškození integrity dat, porušení směrnic.
**Data mining (osint)** - těžba informací a dat z veřejně dostupných zdrojů


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

# Zabezpečení dat na cloudu
- na cloud posílat jen jen předem šifrovaná data
- používat [[Škola/IT/HTTPS\|HTTPS]] -> bezpečný přenos dat
- dělat pravidelné zálohy
- použít [[Škola/IT/VPN\|VPN]]
## Nejbezpečnější cloud - vlastní cloud
- v lokální síti
- víme, kde se data nachází
- **Důležité:** 
	- mít hodně zabezpečené úložiště
	- šifrování dat na disku
# Zabezpečení dat na lokálním počítači
- Šifrování na disku
- Dělat pravidelné zálohy
- **Fyzické zabezpečení**:
	- zámek
	- ocelové lanko - zabezpečí počítač proti odnesení, nejde přeříznout
- **Software pro šifrování dat** - na windowsech např. ==bitlocker==
- **Software pro zálohu dat** 
	- cobian backup
		- automatické ukládání
		- raidové pole
		- na externí disk / cloud
- **Souborové systémy umožňující šifrování** - NTFS, xFAT