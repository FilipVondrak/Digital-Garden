---
{"dg-publish":true,"permalink":"/Škola/IT/Programování/Konstruktor třídy C-Sharp/","created":"2024-03-19T15:18:06.932+01:00","updated":"2024-05-11T19:44:14.407+02:00"}
---

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