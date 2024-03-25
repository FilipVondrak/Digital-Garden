---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Metody tříd/","created":"2023-12-19T09:12:13.238+01:00","updated":"2024-03-24T22:13:10.228+01:00"}
---

#Maturitní_otázka #IT #Programování 
# Konstruktor

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- Nastavuje hodnoty atributům
- je to speciální metoda, která proběhne při vytvoření třídy
- až na výjimky je vždy public
- ==Jmenuje se stejně jako třída==
- často inicializuje komponenty
- ==nemá návratový datový typ==
# Bezparametrický konstruktor
- je defaultní po vytvoření třídy
- nebere žádné parametry, jen spustí kód v něm
# Konstruktor s parametrem
- bere jakékoliv množství parametrů
- parametry jsou napsány v závorce za jménem funkce
- je nutné napsat typ proměnné (např. string nebo int)

> [!Showcase] Ukázka kódu - podpis bezparametrického konstruktoru
> ```Csharp
> public Form1( )
> ```
# Přetížení konstruktoru
- vytvoření více konstruktorů s jinými parametry

> [!Showcase]- Ukázka kódu - přetížený konstruktor
>1. konstruktor je bezparametrický
>2. konstruktor je s parametrem text typem string
>```CSharp
> public partial class Form1 : Form
>{
>    public Form1()
>    {
>        InitializeComponent();
>    }
>
>    public Form1(string text)
>    {
>        // tohle je přetížený konstruktor, který přijímá
>        // text v parametru a nastaví ho jako text tlačítka
>        button1.Text = text;
>        InitializeComponent();
>    }
>}
>```

</div></div>

# Metody

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



#IT #Programování #SPOSDK #Maturitní_otázka

- podprogram, který pracuje s daty/atributy
- je blok kódu, který je samostatně spustitelný a plní specifickou úlohu
- Může pracovat s daty a atributy 
- lze ho opakovaně volat z jiných částí programu

___
# Dělení metod
## Procedura
- Nevrací žádné data - návratový typ **void**
- provede úkol a skončí
## Funkce
- vrací data
- **musí** mít ==v zápisu datový typ==, který se má vrátit
- **musí** obsahovat keyword **return**
- na rozdíl od procedury se jinak volá
___
# Návratový typ
- Návratový typ určuje, jaký typ dat funkce vrátí.
- Běžné typy zahrnují `int`, `double`, `string` a `bool`
- lze taky použít vlastní návratové typy

___
# Parametry
- Parametry jsou vstupní data, která se předávají funkci při jejím volání
- Parametry se uvádějí v závorkách za názvem funkce.
- Každý parametr má svůj typ a název

___
# Modifikátory přístupu

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



#IT #Programování #C-Sharp
## Private
- Modifikátor `private` určuje, že člen (atribut nebo metoda) je přístupný **pouze** v rámci třídy, ve které je definován.
## Public
- Modifikátor `public` určuje, že člen je ==přístupný z libovolného kódu==, který má přístup k instanci třídy.
## Protected
- Modifikátor `protected` určuje, že člen je přístupný pouze v rámci třídy ==a z tříd odvozených/zděděných==
## Internal
- Modifikátor `internal` určuje, že člen je přístupný ze stejné assembly

</div></div>


___
# Statické/Nestatické
## Statické
- Statické členy (metody a atributy) **nejsou** vázány na konkrétní instanci třídy
- Existují pouze v rámci třídy a jsou přístupné bez nutnosti vytvářet instanci
- Jsou nutné např. k patternu [[Osobní/Programování/Patterny/Singleton\|Singleton]]
## Nestatické
- vždy musíme vytvořit instanci
- Nestatické členy (metody a atributy) **jsou** vázány na konkrétní instanci třídy
- Pro přístup k nim je nutné nejprve vytvořit instanci třídy

</div></div>

