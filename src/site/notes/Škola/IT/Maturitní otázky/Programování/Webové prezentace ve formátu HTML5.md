---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Webové prezentace ve formátu HTML5/","created":"2023-12-19T09:11:06.366+01:00","updated":"2024-03-18T21:49:12.351+01:00"}
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

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



#IT 
- Fonty, barvy, rozložení
- nachází se ve vlastním souboru .css nebo v \<head>

___
## Kaskádové styly
- dnes ve verzi 3
### Selektory
- **Syntaxe** - Selektor { vlastnost: hodnota; }
#### Třída 
- je možné dát tyto styly **více** prvkům naráz
- **Zapsání kódu** -> .trida { color: black; }
#### ID
- lze přiřadit **pouze 1** prvku
- podle ID se dá prvek najít v [javascriptu](JavaScript)
- **Zapsání kódu** -> \#id { color: black; } 
___
## Nejdůležitější tagy
- **Width** - mění šířku prvku
- **Height** - mění výšku prvku
- **Color** - používá se RGBA
- **Nejpoužívanější jednotky** - pixely (px), procenta (%), view height (vh), view width (vw)
### Box model
- **Margin** - Posunutí prvku od prvku ve kterém je vložený
- **Border** - hranice prvku, je okolo kontentu v prvku
- **Padding** - odsazení kontentu od borderu, je to vnitřní odsazení

> [!Info]- Odsazování
> např. marginu nebo paddingu se zapisuje ve stylu:
> ``` HTML
> <div style="margin=0,0,0,0"> </div>
> ```
> první číslo je odsazení zleva
> druhé osazení z vrchu
> třetí je odsazení zprava
> čtvrté je odsazení ze spodu

![](https://lh7-us.googleusercontent.com/a-d9qqUSaOTCsyCeIHhsh5v3d_0BYXpQgfuog-Nfml8yuGIEfQoj8lYLJ5OPwJYYJNLWHPhgcHd5MmXUhwN28XpvrdeswAx2V691ERhcINBDDim5FlrFxWc9xLJE_EvszEjANlFlj14i_QNLtw_dCxk)
___
## Layout 
- Grid
- Flex
- Float
___
# Využití CSS
- Díky CSS se dá upravit vše od tvaru a barvy divu po animace
- Každý element v html má několik vrstev
___
## Responzivita

___
# Použití CSS
- Možno zapsat do externího stylesheet souboru (soubor s koncovkou .css), a do html souboru se pouze dá odkaz na styly
> [!example]+ Ukázka kódu
>```HTML
><html> 
>	<head> 
>		<title>
>			//Jméno stránky
>		</title>
>
>		<meta> 
>			// kódování (UTF-8,..), atd.
>		</meta>
>
>		<link rel="stylesheet" href="stylesheet.css">
>	</head>
>	<body>
>		//to co  se zobrazuje uživateli
>	</body>
> </html>
> ```
- Do hlavičky HTML souboru
> [!example]+ Ukázka kódu
>```HTML
><html> 
>	<head> 
>		<title>
>			//Jméno stránky
>		</title>
>
>		<meta> 
>			// kódování (UTF-8,..), atd.
>		</meta>
>
>		<style>
>			// zde se zapíší styly v následujícím formátu
>			.styl{
>			
>			}
>		</style>
>	</head>
>	<body>
>		//to co  se zobrazuje uživateli
>	</body>
> </html>
> ```
- rovnou v HTML tagu
> [!example]+ Ukázka kódu
>```HTML
><html> 
>	<head> 
>		<title>
>			//Jméno stránky
>		</title>
>
>		<meta> 
>			// kódování (UTF-8,..), atd.
>		</meta>
>
>	</head>
>	<body>
>		<div style="font:arial">
>		</div>
>	</body>
> </html>
> ```

</div></div>

# HTML tagy

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



## HTML tagy
- Používá **párové** tagy
- `<i> </i>` -> kurzíva
- `<strong> </strong>` -> tučně
- `<img src="adresa obrázku (může být url nebo lokální)" alt="popisek obrázku"/>` -> vložení obrázku 
- `<u> </u>` -> podtržení

</div></div>

# Optimalizace SEO

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">

# SEO

</div>


- Klíčová slova
- Navýšit počet návštěvníků
- Odkazy z ostatních webů
- Sitemap - struktura webu v xhtml souboru (sitemap.xhtml)

</div></div>

# JavaScript

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovaci-jazyky/java-script/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">






</div></div>


# Hypertext
