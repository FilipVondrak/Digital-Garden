---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Konstruktory/","created":"2023-12-19T09:12:11.009+01:00","updated":"2024-03-24T22:19:19.811+01:00"}
---

#Maturitní_otázka #IT #Programování 
# Třídy 

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- vytvoří si operátorem **new**, který zavolá konstruktor třídy 
- je abstraktním modelem
- používá se k definování objektů s tímto modelem
- obsahují **atributy** a **metody**, které definují chování objektu

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
