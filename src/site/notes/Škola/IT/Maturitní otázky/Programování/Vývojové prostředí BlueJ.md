---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Vývojové prostředí BlueJ/","tags":["Maturitní_otázka","IT","Programování"],"created":"2023-12-19T09:15:51.269+01:00","updated":"2024-05-17T18:58:22.010+02:00"}
---

# Co je BlueJ
- je to integrované vývojové prostředí (IDE)
- je speciálně navržené pro výuku programování v jazyce Java
- Vzniklo na University of Kent ve Velké Británii
- je určeno především pro začátečníky v programování
## Hlavní vlastnosti
### Jednoduché rozhraní
- BlueJ má jednoduché a intuitivní rozhraní
- je navrženo tak, aby bylo snadno srozumitelné pro nováčky
### Vizualizace tříd a objektů
- umožňuje vizualizaci tříd a objektů prostřednictvím diagramů tříd
- pomáhá studentům lépe pochopit vztahy mezi objekty a třídami
### Snadná správa projektů
- Umožňuje snadnou správu menších projektů
- je ideální pro výukové účely a pro začátečníky
## Popis možných tříd
### Standardní třída
### Interfejs (rozhraní)
- Rozhraní (interface) v jazyce Java, které deklaruje metody, ale neimplementuje je
- pro definici kontraktů, které musí implementovat třídy, které tento interfejs implementují
### Test jednotky
- Třída určená pro psaní jednotkových testů
- pro testování jednotlivých částí kódu (metod, tříd) pro ověření, že fungují správně
### Výčtový typ (Enum)
- Speciální třída, která reprezentuje skupinu konstant (enumeraci)
- Definice pojmenovaných hodnot, které mohou být použity jako konstanty, např. dny v týdnu, směry, apod
### Record
- Zkrácený způsob definice datové třídy v jazyce Java
- má neměnitelné pole (atributy)
- pro vytváření jednoduchých datových struktur
- automaticky generovanými metodami, jako jsou gettery, equals, hashCode a toString
### Emptyclass
- Prázdná třída bez jakéhokoli obsahu
- můžete naplnit vlastními definicemi
### Mainclass
- vstupním bodem programu
- Třída obsahující hlavní metodu (`public static void main(String[] args)`)
- Definice hlavní třídy, která bude spuštěna jako první při běhu programu
# Tvorba tříd 
# Statické / nestatické

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/metody-c-sharp/#staticke-nestaticke" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



# Statické/Nestatické
## Statické
- Statické členy (metody a atributy) **nejsou** vázány na konkrétní instanci třídy
- Existují pouze v rámci třídy a jsou přístupné bez nutnosti vytvářet instanci
- Jsou nutné např. k patternu [[Osobní/Programování/Patterny/Singleton\|Singleton]]
## Nestatické
- vždy musíme vytvořit instanci
- Nestatické členy (metody a atributy) **jsou** vázány na konkrétní instanci třídy
- Pro přístup k nim je nutné nejprve vytvořit instanci třídy
___

</div></div>

# Vztahy mezi třídami
- pokud chceme vytvořit vztah mezi třídami a nechceme ho psát kódově, tak můžeme použít tlačítko s šipkou, toto tlačítko automaticky určí vztah
![Pasted image 20240517185410.png](/img/user/Images/Pasted%20image%2020240517185410.png)
## Dědění
- v BlueJ je dědění znázorněno plnou šipkou mezi dvěma třídami
- šipka míří směrem ze třídy, která dědí, do třídy, ze které dědí
![Pasted image 20240517185506.png](/img/user/Images/Pasted%20image%2020240517185506.png)
## Implementace
- v BlueJ je implementace znázorněna čárkovanou šipkou
- šipka míří směrem ze třídy, která implementuje, do interfacu, který implementuje
![Pasted image 20240517185543.png](/img/user/Images/Pasted%20image%2020240517185543.png)
## Vytvoření instance
- pokud třída vytváří instanci jiné třídy
- čárkovaná šipka míří směrem ze třídy, která vytváří instanci, do třídy, které instanci vytváří
![Pasted image 20240517185820.png](/img/user/Images/Pasted%20image%2020240517185820.png)
# Tvorba dokumentace
## V BlueJ
1. Dvojklikem otevřeme kód třídy
2. Vpravo nahoře přepneme režim z Implementace na Dokumentace
![Pasted image 20240517143948.png](/img/user/Images/Pasted%20image%2020240517143948.png)
## V prohlížeči
1. V BlueJ klineme vlevo nahoře na "Nástroje"
2. poté klikneme na "Dokumentace projektu"
3. vytvořená dokumentace se nám otevře v prohlížeči
![Pasted image 20240517144440.png](/img/user/Images/Pasted%20image%2020240517144440.png)
# Volání statických a nestatických metod
# Zobrazení nabídky
`CTRL` + `SPACE` -> otevře nabídku metod a vlastností
# Užití příkazového panelu
- Příkazový panel se nachází vpravo dole
- Můžeme do něj zadávat jednotlivé příkazy
![Pasted image 20240517185057.png|650](/img/user/Images/Pasted%20image%2020240517185057.png)
# Jednosměrný uzlový seznam
## Uzel
- pamatuje si svoji hodnotu a tu následující
- Má následující metody:
	- **Konstruktor**
		- vkládáme sem hodnotu uzlu
	- **setDalsiUzel**
	- **getDalsiUzel**
	- **getHodnota**
## Seznam
- má uložený první a poslední uzel
- má atributu `pocetUzlu`
- Má následující metody
	- **Konstruktor**
		- nastaví počet uzlů na 0
	- **getPocetUzlu**
	- **GetPrvni**
	- **GetPosledni**
	- **add**
		- vkládá hodnotu na konec
	- **smazPosledni**
	- **SmazPrvni**