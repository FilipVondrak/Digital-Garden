---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Dynamické webové stránky/","created":"2023-12-19T09:11:20.394+01:00","updated":"2024-03-31T17:44:49.896+02:00"}
---

#Maturitní_otázka #IT #Programování 


> [!INFO] Webová stránka
> Je to elektronický dokument, který je přístupný přes internet.
> Jsou zobrazeny ve webovém prohlížeči.
> Obsahuje: text, obrázky odkazy a další prvky

## Dynamické webové stránky

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/dynamicka-webova-stranka/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- ==jsou interaktivní== - jejich obsah se mění v závislosti na uživateli, akci nebo události
	- např. se dá na stránku přihlásit a stránka ukáže data uživatele
- používají jak server-side skripty tak i klient-side skripty
- Nelze otevřít jen pomocí prohlížeče – neumí pracovat s PHP a ASP.NET bez pomoci serveru
	- zpracovává se zároveň na serveru a u klienta
- Dynamické webové stránky se liší od statických stránek tím, že se jejich obsah **mění** v závislosti na uživateli, akci nebo události.
- Různé frameworky jako třeba ASP.NET, React, Nuxt
- Většinou ==používají k práci i databáze==
- Zpracovává se ==zároveň na serveru a u klienta==
	- **Klientské skripty** 
		- [[Škola/IT/Programování/Programovací jazyky/JavaScript\|JavaScript]]
	- **Serverové skripty** 
		- [[PHP\|PHP]]
		- [[ASP.NET\|ASP.NET]] 
		- [[Škola/IT/Programování/Programovací jazyky/Java\|Java]]
		- [[Škola/IT/Programování/Programovací jazyky/C-Sharp\|C-Sharp]]

![ds_process_complete.png.img.png](/img/user/Images/ds_process_complete.png.img.png)

</div></div>

___
## Statické webové stránky
- obvykle ==soubor s html kódem== a tagy
- ==nejsou zpracovávané na serveru==
- Dostupné přes server http (webový server)
- Celý vzhled stránky má na starosti prohlížeč - css, html tagy, javascript
- nemusí být na první pohled rozpoznatelný od dynamické stránky

### Výhody
- plný dohled nad html kódem
- jsou nenáročné na hosting
### Nevýhody
- praktické užití je složitější, pokud máme na webu více obsahu nebo jej často měníme - změny se musí provádět přímo v HTML kódu
- stránky mohou působit zastarale
___
## ASP MVC
-> **Model View Controller**
- [[Škola/IT/Programování/Programovací jazyky/C-Sharp\|C#]]
- Vzhled je oddělen od logiky
- struktura projektu: složky Models, Views a Controllers

> [!NOTE]- Business vs Application logika
> #### Business logika:
> - Věrný zákazník získá 10% slevu na všechny nákupy.
> - Objednávky je nutné objednat 24 hodin předem před doručením
> #### Application logika:
> - Online objednávkový systém automaticky uplatňuje 10% slevu na objednávky uživatelů, kteří jsou na základě svých přihlašovacích údajů identifikováni jako "věrní zákazníci"
> - Systém zabrání uživatelům objednávat produkty s datem dodání kratším než 24 hodin.
### Model
- ==Reprezentuje data aplikace a **business** logiku==
	- např. zaměstnanci, produkty, objednávky
- Je to třída/soubor tříd, co mají za úkol vracet data
- vůbec netuší, kdo ji využívá
### View
- ==zobrazení dat uživateli==
- přípona souboru **.cshtml**
- stránka vytvořená pomocí HTML tagů (+CSS)
- Razor syntax pro komunikaci s modelem – Razor markup + C# + HTML
- Netuší, kde bere data
### Controller
- ==Propojuje – Rozhoduje, který model a view se použije==
- Zpracovává HTTP požadavky od uživatele
- ==obsahuje aplikační logiku==

___
## Servery pro dynamické stránky
### Apache 
- pro PHP
- open-source
- cross-platform
### ASP
### IIS 
- součástí **Windows** -> je nutno zapnout

> [!WARNING]- Otázka u maturity -> co se stane když zapnem IIS
> 1. Vytvoří se složka na disku (C:) – Program Files – IIS – Microsoft Web Deploy
> 2. zavoláme server jménem a to, co je ve složce Web se defaultně spustí