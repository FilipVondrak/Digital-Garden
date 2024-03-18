---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Využívání CSS v kombinaci s HTML/","created":"2023-12-19T09:11:16.298+01:00","updated":"2024-03-18T21:50:58.788+01:00"}
---

#Maturitní_otázka #IT #Programování 

## Úvod
- HTML a CSS jsou dva základní jazyky, které se používají k tvorbě webových stránek
- ==HTML definuje strukturu== a obsah stránky, zatímco ==CSS určuje její vzhled==
- Tyto dva jazyky se vzájemně doplňují, samostatně nemohou pořádně fungovat
- CSS umožňuje přidávat do webové stránky interaktivní prvky, jako jsou tlačítka a animace
## CSS

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


# HTML

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



## HTML tagy
- Používá **párové** tagy
- `<i> </i>` -> kurzíva
- `<strong> </strong>` -> tučně
- `<img src="adresa obrázku (může být url nebo lokální)" alt="popisek obrázku"/>` -> vložení obrázku 
- `<u> </u>` -> podtržení

</div></div>
