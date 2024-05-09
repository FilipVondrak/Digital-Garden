---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Principy OOP/","tags":["Maturitní_otázka","IT","Programování"],"created":"2023-12-19T09:12:06.045+01:00","updated":"2024-05-08T23:52:57.538+02:00"}
---

# Třída

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- vytvoří si operátorem **new**, který zavolá konstruktor třídy 
- je abstraktním modelem
- používá se k definování objektů s tímto modelem
- obsahují **atributy** a **metody**, které definují chování objektu

</div></div>

# Objekt

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



![Pasted image 20240508225042.png](/img/user/Images/Pasted%20image%2020240508225042.png)

</div></div>

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
## Dědění
- určuje vztah mezi rodičovskou třídou a naší třídou
- umožňuje novým objektům zdědit vlastnosti a chování z existujících objektů
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
- ==je to proměnná pro metody==
> [!Showcase] Ukázka implementace delegáta 
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
- metody definované v základní třídě mohou být přepsány (pomocí keywordu **override**) v odvozených třídách
- při volání přepsaných metod se použije implementace specifická pro odvozenou třídu
- umožňuje objektům reagovat na stejné zprávy (metody) různými způsoby v závislosti na jejich typu

> [!Showcase]- Ukázka implementace polymorfizmu
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
