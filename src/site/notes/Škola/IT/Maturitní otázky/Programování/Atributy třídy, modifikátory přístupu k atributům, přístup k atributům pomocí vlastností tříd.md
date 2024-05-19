---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Atributy třídy, modifikátory přístupu k atributům, přístup k atributům pomocí vlastností tříd/","tags":["Maturitní_otázka","IT","Programování"],"created":"2023-12-19T09:12:08.124+01:00","updated":"2024-05-16T16:36:08.269+02:00"}
---

# Třída

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/trida-c-sharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- vytvoří si operátorem **new**, který zavolá konstruktor třídy 
- je abstraktním modelem
- je šablona, která definuje vlastnosti, metody a chování pro sadu podobných objektů
- existuje pouze v programovém kódu
- Slouží jako stavební blok pro modelování reálných objektů a jejich interakcí
- používá se k definování objektů s tímto modelem
- obsahují **atributy** a **metody**, které definují chování objektu

</div></div>

# Konstruktor

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/konstruktor-tridy-c-sharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- Nastavuje hodnoty atributům
- je to speciální metoda, která proběhne při vytvoření třídy
- až na výjimky je vždy public
- ==Jmenuje se stejně jako třída==
- často inicializuje komponenty
- ==nemá návratový datový typ==
# Bezparametrický konstruktor
- je defaultní po vytvoření třídy
- nebere žádné parametry, jen spustí kód v něm
> [!Showcase] Ukázka kódu - podpis bezparametrického konstruktoru
> ```Csharp
> public Form1( )
> ```
# Konstruktor s parametrem
- bere jakékoliv množství parametrů
- parametry jsou napsány v závorce za jménem funkce
- je nutné napsat typ proměnné (např. string nebo int)
> [!Showcase] Ukázka kódu - podpis konstruktoru s parametrem
> ```Csharp
> public Form1(string text, int číslo)
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

# Atribut

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/atributy-c-sharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





> [!warning] Pozor
> V češtině se říká atributa jiné věci než v angličtině.
> V češtině je atributy globální proměná, ale v angličtině jsou to metadata.

- Proměnná, konstanta
- je deklarovaná na úrovni třídy
- jedná se o globální proměnou
- má modifikátory přístupu
	- private
	- public
	- static
- Používá **Gettery** a **Settery** pro přístup k atributům

</div></div>

# Metody

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/metody-c-sharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




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
# Modifikátory přístupu

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/modifikatory-pristupu-c-sharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Private
- Modifikátor `private` určuje, že člen (atribut nebo metoda) je přístupný **pouze** v rámci třídy, ve které je definován.
## Public
- Modifikátor `public` určuje, že člen je ==přístupný z libovolného kódu==, který má přístup k instanci třídy.
## Protected
- Modifikátor `protected` určuje, že člen je přístupný pouze v rámci třídy ==a z tříd odvozených/zděděných==
## Internal
- Modifikátor `internal` určuje, že člen je přístupný ze stejné assembly

</div></div>


</div></div>

___
# Přístup k atributům pomocí vlastností tříd
- používají se **gettery** a **settery**
- slouží k schování atributy
## Ukázka kódu
### C\#
```CS
public class SaleItem
{
    string _name;
    decimal _cost;

    public SaleItem(string name, decimal cost)
    {
        _name = name;
        _cost = cost;
    }

    public string Name
    {
        get => _name;
        set => _name = value;
    }

    public decimal Price
    {
        get => _cost;
        set => _cost = value;
    }
}
```
pokud v getterech a setterech **není** jiná logika než načítání/přiřazení hodnoty, tak je možné použít automaticky implementované vlastnosti
```CS
public class SaleItem
{
    public string Name
    { get; set; }

    public decimal Price
    { get; set; }
}
```
### Java
```Java
public class Student {  
  private String name;  
  private int age;  
  
  public void setName(String name) {  
      this.name = name;  
  }  
  
  public String getName() {  
      return name;  
  }  
  
  public void setAge(int age) {  
      this.age = age;  
  }  
  
  public int getAge() {  
      return age;  
  }  
}
```
