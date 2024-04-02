---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Bezpečná komunikace/","created":"2024-03-18T20:54:39.491+01:00","updated":"2024-03-14T18:06:14.951+01:00"}
---

- Jsou zachovány CIA (Confidentiality, Integrity, and Availability) principy
    - **Důvěrnost**
        - Do komunikace nevstupuje žádní neoprávněná třetí strana
    - **Integrita**
        - Nedochází k neoprávněné úpravě [[Škola/IT/Data\|dat]]
    - **Dostupnost**
        - Data i systémy jsou dostupné
- Komunikující strany si musí být jisté, že nejsou odposloucháváni nebo narušeni

___
# Způsoby narušení komunikace
### Man in the middle

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Komunikace je odposlouchávána třetí stranou
- Není nutné být uprostřed na fyzické cestě (komunikace se dá přesměrovat)
- **Jak se bránit?**
    - Koncové šifrování komunikace

</div></div>

### Phishing

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Někdo cizí se vydává za příjemce zprávy
- Falešné stránky, které vypadají jak ty pravé (Internetové bankovnictví, sociální sítě)
- Šíří se e-maily
- **Jak se bránit?**
    - Kontrolovat certifikáty stránky
    - Kontrolovat název domény
    - Kontrolovat odesilatele e-mailu

</div></div>

### Fyzická krádež korespondence

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




- Odcizení dopisu/dat pro určitou osobu na přenosovém médiu
- **Jak se bránit?**
    - Fyzické zabezpečení - zamknout do stolu/trezoru
    - Používat [[Škola/IT/Šifrování\|Šifrování]]/zabezpečení - šifrovat data na flashce a mít na ní biometriku

</div></div>

___
# Zabezpečení komunikace
- Využití [kryptografie](Šifrování.md) - šifrování (ot.5)
- Užití digitálních certifikátů a podpisů
    - ověření komunikujících subjektů
- Dodržovat [obecnou bezpečnost na sítí](Bezpečné%20chování%20v%20lokání%20síti%20a%20na%20internetu.md) (ot.2)

___

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
