---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Principy OOP/","tags":["Maturitní_otázka","IT","Programování"],"created":"2023-12-19T09:12:06.045+01:00","updated":"2024-05-11T21:09:11.106+02:00"}
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

# Objekt

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/objekt-programovani/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- je to již vytvořená instance třídy
- je to fyzická entita v paměti, která existuje v běžícím programu
- Konkrétní výskyt definovaný pomocí třídy
- Umožňuje interakci s programem a reaguje na události
![Pasted image 20240508225042.png](/img/user/Images/Pasted%20image%2020240508225042.png)

</div></div>

# Rozdíl mezi třídou a objektem
>[!tip] Příklad
>Představte si ==třídu jako návrh domu== a o==bjekt jako skutečný postavený dům==. Třída **definuje** všechny detaily plánu (počet pokojů, okna, dveře), zatímco dům je **fyzická** struktura s konkrétními rozměry a materiály. Každý dům (objekt) postavený podle plánu (třídy) bude mít stejné základní vlastnosti, ale může se lišit v detailech
## Abstrakce vs. Konkrétnost
- Třída je abstraktní koncept
- objekt je konkrétní instance s definovanými hodnotami
## Šablona vs. Entita
- Třída slouží jako šablona pro vytváření objektů
- objekt je fyzická entita v paměti
## Definice vs. Implementace
- Třída definuje vlastnosti a metody
- objekt uchovává hodnoty a umožňuje interakci s metodami
# Výhody OOP
- **Modularita** 
	- Kód je rozdělen do menších, lépe zvládnutelných a opakovaně použitelných modulů
- **Snadná údržba**
	- Změny v implementaci objektů lze provést bez ovlivnění jiných částí systému
- **Srozumitelnost**
	- Kód je snáze pochopitelný a čitelný díky jasnému rozdělení zodpovědností mezi objekty
- **Opakované použití**
	- Dědičnost a polymorfismus usnadňují opakované použití kódu a snižují redundanci
- **Rozšířitelnost**
	- Systémy navržené v OOP se snadněji rozšiřují o nové funkce a funkcionality
# Základní principy
## Skládání
- výsledkem je znovupoužitelný kód
- představuje ==použití instance jedné třídy v definici druhé třídy==
- je to udržování odkazů na jiné objekty
- třída obsahuje instanci jiné třídy jako jedno ze svých datových členů
- umožňuje vytvářet složitější objekty tím, že kombinuje jednodušší objekty dohromady
> [!Showcase]- Ukázka implementace skládání
>```CS
>using System;
>
>class Engine 
>{     
>	public void Start()     
>	{         
>		Console.WriteLine("motor se zapnul");	
>	}      
>	
>	public void Stop()     
>	{         
>		Console.WriteLine("motor se vypnul");     
>	} 
>}  
>
>// třída auto, která se skládá z motoru 
>class Car 
>{     
>	// skládání: třída auto používá motor
>	private Engine engine;
>	
>	public Car()     
>	{         
>		engine = new Engine(); // vytvoření instance motoru     
>	}      
>	
>	public void StartCar()     
>	{         
>		engine.Start(); // delegování akce Start na instanci motoru    	
>	}      
>	
>	public void StopCar()     
>	{         
>		engine.Stop(); // delegování akce Stop na instanci motoru     	
>	} 	
>}  
>
>class Program 
>{     
>	static void Main(string[] args)     
>	{         
>		Car myCar = new Car(); // vytvoření instance auta         
>		
>		// použití metod auta      
>		myCar.StartCar();         
>		myCar.StopCar();     
>	} 
>}
>```

## Dědění
- určuje vztah mezi rodičovskou třídou a naší třídou
- umožňuje novým ==objektům zdědit vlastnosti a chování z existujících objektů==
- Podporuje opakované použití kódu
> [!Showcase]- Ukázka implementace dědění a opakovánní kódu
>```CS
>class Program  
>{  
>    class ParentClass  
>    {  
>        protected string name;  
>        public ParentClass()  
>        {            
>		   this.name = "ParentClass";  
>        }        
>       
>        public void PrintName()  
>        {            
>	        Console.WriteLine(this.name);  
>        }    
>    }    
>  
>    class childClass : ParentClass  
>    {  
>    // třída childClass zdědila od ParentClass atributu name a metodu PrintName()
>        public childClass()  
>        {            
>	    this.name = "childClass";        
>	    }   
>	}
>	  
>    static void Main(string[] args)  
>    {        
>	    var parent = new ParentClass();  
>        var child = new childClass();  
>      
>        parent.PrintName();  
>        child.PrintName();  
>    }
>}
>```

## Zapouzdření
- ==Skrývá implementační detaily==
- umožňuje přístup k jeho vlastnostem a metodám pouze prostřednictvím definovaných rozhraní
- zajišťuje modularitu a bezpečnost kódu
> [!Showcase]- Ukázka implementace zapouzdření
>```CS
>class Program  
>{  
>    class UkazkaZapouzdreni  
>    {  
>        // atribut _cislo je privatni a tak chranime pristup, ze
>        // ostatni tridy nemohou primo menit nebo cist jeho hodnotu   
>		private int _cislo;  
>        
>        // verejna vlastnost Cislo, ktera umoznuje cist a zapisovat 
>        // do privatniho atributu _cislo  
>        // nove hodnoty se nastavuji pouze pokud jsou mensi nebo rovny 10
>        // a tim je zabezpeceno, ze hodnota bude vzdy mensi nebo rovna 10 
>        public int Cislo  
>        {  
>            get { return _cislo; }  
>            set  
>            {  
>                if(value<=10)  
>                    _cislo = value;  
>            }        
>        }    
>      
>    }    
>    
>    static void Main(string[] args)  
>    {        
>	    UkazkaZapouzdreni ukazka = new UkazkaZapouzdreni();  
>        ukazka.Cislo = 5;  
>        Console.WriteLine(ukazka.Cislo); // vysledek -> 5  
>        ukazka.Cislo = 15;  
>        Console.WriteLine(ukazka.Cislo); // vysledek -> 5  
>    }  
>}
>```

## Delegování
- V C# se delegování často implementuje pomocí konstruktů nazývaných **delegáty**
- **Delegát** je typ, který reprezentuje reference na metody s kompatibilním podpisem (návratový typ a parametry)
- delegáti se často používají v asynchronním programování
- nejčastěji se používají pro obsluhu událostí (eventů)
- k jednomu delegátovi lze přiřadit několik metod
- delegát ==je proměnná pro metody==
> [!Showcase]- Ukázka implementace delegáta 
>```CS
>namespace TestDelegování;  
>public delegate void MujDelegat();  
 > 
>class Program  
>{  
>    class TridaA  
>    {  
>        public void MetodaA()  
>        {            
> 	       Console.WriteLine("MetodaA");  
>        }        
>    }    
>    
>    class TridaB  
>    {  
>        public void MetodaB()  
>        {            
> 	       Console.WriteLine("MetodaB");  
>        }    
>    }   
>    
>    static void Main(string[] args)  
>    {        
> 	   TridaA a = new TridaA();  
>        TridaB b = new TridaB();  
> 
>        MujDelegat delegat = a.MetodaA;  
>        delegat += b.MetodaB;  
>        delegat.Invoke();  
>    }
>}
>```

## Polymorfizmus
### Compile-Time polymorfizmus
-> kompilátor identifikuje která metoda je zavolaná v době kompilace
- [[Škola/IT/Programování/Konstruktor třídy C-Sharp#Přetížení konstruktoru\|přetížení konstruktoru]] nebo metody (**method overloading**)
- přetížení operátoru (**operator overloading**)
> [!Showcase]- Ukázka přetížení operátoru `+`
> Příklad 1:
>```CS
>int x = 7;
>int y = 5;
>
>int sum = x + y;
>Console.WriteLine(sum);
>// Výsledek: 12
>```
>
>Příklad 2:
>```CS
>string firstString = "Harry";
>string secondString = "Styles";
>
>string concatenatedString = firstString + secondString;
>Console.WriteLine(concatenatedString);
>// Výsledek: HarryStyles
>```
>
>V *příkladu 1* se operátor `+` použil k sečtení dvou čísel, ale v *příkladu 2* se použil ke spojení tvou řetězců do jednoho.
### Run-Time polymorfizmus
-> metoda, která je volána, je určena za běhu, nikoli při kompilaci
- pokud se při dědění stejná metoda nachází jak v parent třídě i child třídě, tak se zavolá metoda z child třídy -> tomu se říká **method overriding**
- metody definované v základní třídě mohou být přepsány (pomocí keywordu **override**) v odvozených třídách
- při volání přepsaných metod se použije implementace specifická pro odvozenou třídu
> [!Showcase]- Ukázka implementace Run-time polymorfizmu
>```CS
>class Animal
>{
>    public virtual void Speak()
>    {
>        Console.WriteLine("Animal speaks");
>    }
>}
>
>class Dog : Animal
>{
>    public override void Speak()
>    {
>        Console.WriteLine("Dog barks");
>    }
>}
>
>class Cat : Animal
>{
>    public override void Speak()
>    {
>        Console.WriteLine("Cat meows");
>    }
>}
>
>class Program
>{
>    static void Main()
>    {
>        // Díky polymorfismu se dá lehce zavolat metoda Speak
>        // na instanci Animal u zděděných tříd Dog a Cat
>        Animal[] animals = new Animal[] { new Dog(), new Cat() };
>        foreach (Animal animal in animals)
>        {
>            animal.Speak();
>        }
>    }
>}
>```
## Abstrakce
- hlavním cílem je schovat složitost tím, že před uživatelem skryje nepotřebné detaily
- Pomáhá nám pracovat s objekty, aniž bychom museli rozumět všem jejich vnitřním mechanismům