---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Webové prezentace ve formátu HTML5/","created":"2023-12-19T09:11:06.366+01:00","updated":"2024-03-13T18:19:14.869+01:00"}
---

#Maturitní_otázka #IT #Programování 

- Tvoření stránek:
	- Text editor, IDE
	- Ve Wordu convertnutím

___
# Typy stránek
## Statické 
- ==Neměnné==
- bez interakce, jen k zobrazení
- pouze server-side skripty
- Např samotné html soubory

## Dynamické
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- ==jsou interaktivní==
- používají jak server-side skripty tak i klient-side skripty
- Dynamické webové stránky se liš od statických stránek tím, že se jejich obsah **mění** v závislosti na uživateli, akci nebo události.
- Různé frameworky jako třeba ASP.NET, React, Nuxt
- Většinou používají k práci i databáze 
- Zpracovává se ==zároveň na serveru a u klienta==
	- Klientské skripty - JS
	- Serverové skripty - PHP, ASP.NET, Java

</div></div>

# Používané jazyky
- **Server-side**
	- PHP
	- ASP.NET
	- JAVA
- **Klient-side**
	- CSS / HTML
	- JavaScript
	- TypeScript

___
# Struktura webové stránky
```html
<html> 
	<head> 
		<title>
			//Jméno stránky
		</title>

		<meta> 
			// odkazy na css sheety, kódování (UTF-8,..)
		</meta>
	</head>

	<body>
		//to co  se zobrazuje uživateli
	</body>
</html>
```

___
# CSS - kaskádové styly
- Fonty, barvy, rozložení
- nachází se ve vlastním souboru .css nebo v \<head>
- responsivita
# HTML tagy
- `<i> </i>` -> kurzíva
- `<strong> </strong>` -> tučně
- `<img src="adresa obrázku (může být url nebo lokální)" alt="popisek obrázku"/>` -> vložení obrázku 
- `<u> </u>` -> podtržení

# Optimalizace [[Škola/IT/Maturitní otázky/Programování/SEO\|SEO]]
- Klíčová slova
- Navýšit počet návštěvníků
- Odkazy z ostatních webů
- Sitemap - struktura webu v xhtml souboru (sitemap.xhtml)