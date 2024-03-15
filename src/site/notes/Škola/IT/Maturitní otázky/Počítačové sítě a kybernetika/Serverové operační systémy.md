---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Serverové operační systémy/","created":"2023-12-14T18:39:20.984+01:00","updated":"2024-03-14T21:10:21.252+01:00"}
---

#IT #Maturitní_otázka #Software #SPOSDK 
# Co je to operační systém

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

# Funkce serverového operačního systému
## Active Directory

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/active-directory/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software 
## Active Directory
- virtuální obraz firmy/lokální sítě
- Linux alternativa je Samba
### Použití 
- řídí a spravuje doménu
- ==Práva a oprávnění==
### Struktura 
- Organizační jednotky 
	- uživatel, skupina, 
	- sdílená složka 
	- tiskárna / počítače

</div></div>

___
## DHCP

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/dhcp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software #Protokol
-> Dynamic Host Configuration Protocol
## Využití
- dynamická konfigurace síťového rozhraní
## Výhody oproti statickým IP adresám
- **Automatické přidělování IP adres**
	- Nemusíte ručně nastavovat IP adresu na každém zařízení, což šetří čas a minimalizuje chyby
- **Dynamické přidělování**
	- IP adresy jsou přidělovány pouze po dobu, kdy je zařízení zapnuté a připojené k síti. Tím se šetří vzácné IP adresy, což je důležité zejména u velkých sítí.
- **Centrální správa**
	- Konfiguraci sítě lze snadno spravovat na jednom místě - na serveru DHCP
## Princip
1. Po připojení zařízení k síti vyšle klient na server DHCP zprávu s dotazem na IP adresu
2. Server DHCP odpoví nabídkou volné IP adresy z jeho fondu
3. Klient si tuto nabídku vyžádá a server mu zašle kromě IP adresy i další důležité informace, jako je maska podsítě, výchozí brána a DNS servery
4. Zařízení pak může na základě získaných informací komunikovat v síti
![](https://lh7-us.googleusercontent.com/Z2Uf8LIQXLvDlb7l9dF50MLf-kXp1SvQKkzoyUxV7QhtpFEgCVgWWnrLU1rX_KyWQPnuPN3yEitrd2FPgiJwENPYUlOgRbn38N6E6Cy-4liZ8URA5hlEvUmDn4pL9tzxIHpYlHyNn5YhBQMUQCCq29o)


</div></div>

___
## DNS

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/dns/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#IT #Software #SPOSDK #Maturitní_otázka 
-> Domain name services
- **port 53**
- převádí doménová jména na IP adresy (např. www.amazon.com převede na 192.0.2.44)
	- Doménová jména jsou čitelná pro lidi
	- IP adresy jsou čitelné pro zařízení

# Struktura
- . - kořen
- top level domain - .com, .cz, .edu 
- second level domain - google.com
- subdomain - photos.google.com 
![Pasted image 20240314210031.png](/img/user/Images/Pasted%20image%2020240314210031.png)
# DNS záznamy
- **A** - IPv4
- **CNAME** - Canonical Name - domény s níž souvisí subdomény (takže doména - spošdk.cz, subdomény - jidelna, moodle ..)
- **AAAA** - IPv6
- **MX** - poštovní server
- **TXT** - libovolný text (používá se např. pro ověření vlastnictví)

</div></div>

___
## Souborový server (FTP)
- Sdílení dat v síti
- Mapování
- Oprávnění složek a sdílení
___
## Aplikační sever
- je určen k instalaci, provozu a hostování aplikací a souvisejících služeb pro koncové uživatele
- Může na něm běžet např.
	- Kerio
	- Xamp
	- AltusVario
___
## Mail server
- Zajišťuje přepravu elektronické pošty v síti
- Postfix, Sendmail, Microsoft Exchange server
___
## Web Sever
- Poskytuje klientům webový obsah
- Funguje v internetu, ale může fungovat i v LAN
- **Apache**
    - Open-source
    - nejvíce používaný
- **Nginx**
    - Open-source
    - Zaměření na vysoký výkon
    - Unix-like systémy
- **IIS**
    - Proprietární
    - Microsoft
    - Pro ASP .NET