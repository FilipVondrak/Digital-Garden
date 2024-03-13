---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Využívání CSS v kombinaci s HTML/"}
---

#Maturitní_otázka #IT #Programování 

- HTML a CSS jsou dva základní jazyky, které se používají k tvorbě webových stránek
- ==HTML definuje strukturu== a obsah stránky, zatímco ==CSS určuje její vzhled==
- Tyto dva jazyky se vzájemně doplňují, samostatně nemohou pořádně fungovat
- CSS umožňuje přidávat do webové stránky interaktivní prvky, jako jsou tlačítka a animace
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

# Syntaxe
- Selektor { vlastnost: hodnota; }
## Třída 
- je možné dát tyto styly **více** prvkům naráz
- **Zapsání kódu** -> .trida { color: black; }
## ID
- lze přiřadit **pouze 1** prvku
- podle ID se dá prvek najít v [javascriptu](JavaScript)
- **Zapsání kódu** -> \#id { color: black; } 

# Využití CSS
- díky CSS se dá upravit vše od tvaru a barvy divu po animace
-  Každý element v html má několik vrstev
**![](https://lh7-us.googleusercontent.com/a-d9qqUSaOTCsyCeIHhsh5v3d_0BYXpQgfuog-Nfml8yuGIEfQoj8lYLJ5OPwJYYJNLWHPhgcHd5MmXUhwN28XpvrdeswAx2V691ERhcINBDDim5FlrFxWc9xLJE_EvszEjANlFlj14i_QNLtw_dCxk)**
- 