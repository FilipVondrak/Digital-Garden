---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Jazyk CSharp/","tags":["Maturitní_otázka","IT","Programování","Software","C-Sharp"],"created":"2023-12-19T09:14:44.484+01:00","updated":"2024-05-16T14:51:53.840+02:00"}
---

# Jazyk CSharp
- je to ==objektivně orientovaný programovací== jazyk (OOP)
- je typově bezpečný
- jazyk byl vytvořen roku 2000 firmou Microsoft
- je navržen pro .NET Framework, platformu pro vývoj softwaru pro Windows
- C# je relativně snadno se naučitelný jazyk s moderní syntaxí a velkou škálou funkcí
- jedná se ==high-level programovací jazyk==, což znamená že jazyk má vysokou míru abstrakce a oddělení se přímo od [[Škola/IT/Maturitní otázky/Počítačové sítě a kybernetika/Hardware\|hardwaru]]; High-level jazyky jsou jednodušší pro psaní kódu než low-level jazyky
- jedná se o velmi rychlý jazyk
![Pasted image 20240510143156.png](/img/user/Images/Pasted%20image%2020240510143156.png)
# Použití CSharpu
- je vhodný pro širokou škálu aplikací
- samotný jazyk je cross-platform, což znamená že se dá použít pro většinu operačních systému od Windows po linux a android
- je vhodný jak pro desktopové aplikace (např. hry nebo jiný software) až po webové aplikace
# Základní struktury a principy 
## Principy
- jako objektově orientovaný jazyk má c# tyto základní principy
	- [[Škola/IT/Maturitní otázky/Programování/Principy OOP#Dědění\|dědičnost]]
	- [[Škola/IT/Maturitní otázky/Programování/Principy OOP#Polymorfizmus\|polymorfismus]]
	- [[Škola/IT/Maturitní otázky/Programování/Principy OOP#Objekt\|objekty]] a [[Škola/IT/Maturitní otázky/Programování/Principy OOP#Třída\|třídy]]
## Struktury
- Namespace -> Jmenný prostor
- Třída `Console` (knihovní třída)
	- Má definované statické metody -> nevytváříme instanci
		- Funkce `Readline()`
		- Procedura `WriteLine()`
### Cykly
### Datové typy
**int** - celočíselný datový typ, pro čísla od -2147483648 do 2147483647
**long** - celočíselný datový typ, delší než int pro čísla v rozmezí od -9223372036854775808 do 9223372036854775807
**float** - číselný typ s podporou pro desetinná čísla, přesnost až na 6 desetinných míst
**Double** - číselný typ s podporou pro desetinná čísla, přesnost až na 15 desetinných míst
**char** - datový typ pro znaky, slouží pro ukládání pouze 1 znaku (např. 'B')
**bool** - booleovský datový typ, ukladá pouze hodnoty "True" a "False" (pravda a nepravda)
**string** - datový typ pro ukládání textu
### Proměnné
- používají se pro pojmenování oblastí v paměti, které ukládají data
- deklarují se pomocí klíčového slova `var`, `int`, `double`, `string` atd., následovaného názvem proměnné
- inicializují se operátorem `=`
```CS
int cislo = 10; 
double desetinneCislo = 3.14; 
string jmeno = "Jan";
```
# Události tříd
- slouží k signalizaci, že se v objektu třídy odehrála určitá událost
- Objekty, které chtějí reagovat na událost, se musí přihlásit k odběru události
# Přidání reference na obslužnou metodu
- Reference na obslužnou metodu se přidává pomocí operátoru `+=` a odebírá se pomocí operátoru `-=`
- Obslužná metoda je metoda, která se spustí, když se vyvolá událost
```CS
tlacitko.Click += ObsluznaMetoda;
```
# Tvorba obslužných metod
- Obslužné metody se definují jako běžné metody
- ==musí mít stejný podpis jako metoda vyvolaná událostí==

> [!Showcase]- Jednoduchá ukázka použití event handleru a obslužné metody
>```CS
>namespace TestEventu;  
 > 
>class Program  
>{  
>    static void Main(string[] args)  
>    {        
>	    Tlacitko tlacitko = new Tlacitko();  
>        tlacitko.Klik += ObsluznaMetoda;  
>        Console.WriteLine("Stiskněte tlačítko...");  
>        Console.ReadLine();  
>        tlacitko.Zmackni();  
>    }  
>    static void ObsluznaMetoda(object sender, EventArgs e)  
>    {        
>	    Console.WriteLine("Tlačítko bylo stisknuto!");  
>    }}  
>
>class Tlacitko  
>{  
>    public event EventHandler<\EventArgs\> Klik;  
>    public void Zmackni()  
>    {        
>	    if (Klik != null)  
>        {            
>	        Klik(this, EventArgs.Empty);  
>        }    
>    }        
>}
>```
