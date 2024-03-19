---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Atributy třídy, modifikátory přístupu k atributům, přístup k atributům pomocí vlastností tříd/","created":"2023-12-19T09:12:08.124+01:00","updated":"2024-03-19T15:25:32.104+01:00"}
---

#Maturitní_otázka #IT #Programování 
# Třída

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- může být abstraktní
- vytvoří si operátorem **new**, který zavolá konstruktor třídy 
- základní vlastnost třídy
	- atributy

</div></div>


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
> public Form1(string text)
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

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



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

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



# Procedura
- Nevrací žádné data
- má v zápisu keyword **void**
- provede úkol a skončí
# Funkce
- vrací data
- má ==v zápisu datový typ==, který se má vrátit
- musí obsahovat slovo **return**
- na rozdíl od procedury se jinak volá

</div></div>
