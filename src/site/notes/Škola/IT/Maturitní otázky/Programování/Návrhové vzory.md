---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Návrhové vzory/","created":"2023-12-19T09:15:02.441+01:00","updated":"2024-05-17T18:24:55.553+02:00"}
---

#Maturitní_otázka #IT #Programování 

# Interface

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/interface-csharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- další způsob jak dosáhnout abstrakce
- je to ==kompletně abstraktní==
- může obsahovat pouze abstraktní metody a vlastnosti s prázdným tělem -> má ==pouze podpisy metod a vlastností==

> [!Showcase]- Ukázka interfacu
> ```Csharp
>// interface
>interface Animal 
>{
>  void animalSound(); // interface metoda (nemá tělo)
>  void run(); // interface metoda (nemá tělo)
>}
>```

- ==musí být implementovány== (stejným způsobem jako zdědění)  

> [!Showcase]- Ukázka implementace interfacu
> ```Csharp
// Interface
interface IAnimal 
>{
>  void animalSound(); // interface metoda (nemá tělo)
>}
>
>// třída Pig "implementuje" IAnimal interface
>class Pig : IAnimal 
>{
>  public void animalSound() 
>  {
>    // zde doplní tělo metody animalSound()
>    Console.WriteLine("The pig says: wee wee");
>  }
>}
>```

- slouží hlavně pro vývojáře, aby nezapomněli implementovat určité metody nebo vlastnosti
- pokud třída implementuje interface ale neobsahuje metody/vlastnosti interfacu, tak kód nepůjde spustit
- je možné implementovat několik interfaců v jedné třídě

</div></div>

# Generické třídy

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/maturitni-otazky/programovani/generic-class/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- pracuješ s datovým typem, který není ve třídě předem určen
- používá se například v Listech, jelikož předem nevím jestli budeme mít list s čísly nebo stringy
- třída může pracovat s jakýmkoliv datovým typem
- před název datového typu se přidává typ

</div></div>

# Servant

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/patterny/servant-pattern/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- vzor servant definuje objekt, který slouží k nabídnutí určité funkce skupině tříd, aniž by byla tato funkce definována v každé z nich. 
- Servant je třída, jejíž instance (nebo dokonce jen třída) poskytuje metody, které se starají o požadovanou službu, přičemž objekty, pro které (nebo s nimiž) servant něco dělá, jsou brány jako parametry
- první parametr je datového typu interface
- nepracuje sám, ale komunikuje s obsluhovanými objekty

</div></div>

# Messenger

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/patterny/messanger-pattern/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- česky -> Přepravka
- slouží pro přenos dat z jednoho určitého typu
- třída přepravky má stejné atributy jako třída, ze které bude přenášet informace 
- je to objekt určený k uložení skupiny údajů "pod jednu střechu" a jejich společnému transportu

> [!tip] Použití
> Pokud mám třídu s privátními atributy a chci přečíst tyto hodnoty z jiné třídy, tak je možné použít přepravku. Přepravka přečte privátní atributy a  uloží si je k sobě jako konstanty, které nelze změnit. Ostatní třídy poté mohou přepravku číst ale nikov měnit tyto hodnoty.

> [!info]
> Přepravka je zbytečná. Učí se pouze ve škole.

</div></div>

## Tovární metoda

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/patterny/factory-method/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




> [!Warning] Definice podle Šmída
> Podle Šmída je definice -> jediná  

- statická metoda vracející instanci daného typu
- nemusí vracet vlastní instanci, ale instanci jiné třídy
- slouží jako náhražka konstruktoru
- Myšlenka spočívá v použití interfacu pro vytvoření objektu, ale nakonec se podtřída rozhodne, kterou třídu instancovat

![Pasted image 20240329153655.png](/img/user/Images/Pasted%20image%2020240329153655.png)

> [!Showcase]- ukázka implementace tovární metody v C#
> ```CSharp
>// Product
>public abstract class Vehicle
>{
>    public abstract string GetVehicleType();
>}
>
>// ConcreteProduct
>public class Truck : Vehicle
>{
>    public override string GetVehicleType()
>    {
>        return "Truck";
>    }
>}
>
>// ConcreteProduct
>public class Ship : Vehicle
>{
>    public override string GetVehicleType()
>    {
>        return "Ship";
>    }
>}
>
>// Creator
>public abstract class VehicleFactory
>{
>    public abstract Vehicle CreateVehicle();
>}
>
>// ConcreteCreator
>public class TruckFactory : VehicleFactory
>{
>    public override Vehicle CreateVehicle()
>    {
>        return new Truck();
>    }
>}
>
>// ConcreteCreator
>public class ShipFactory : VehicleFactory
>{
>    public override Vehicle CreateVehicle()
>    {
>        return new Ship();
>    }
>}
>
>class Program
>{
>    static void Main(string[] args)
>    {
>        // Vytvoření Truck pomocí TruckFactory
>        VehicleFactory truckFactory = new TruckFactory();
>        Vehicle truck = truckFactory.CreateVehicle();
>        Console.WriteLine(truck.GetVehicleType()); // Vypíše: Truck
>
>        // Vytvoření Ship pomocí ShipFactory
>        VehicleFactory shipFactory = new ShipFactory();
>        Vehicle ship = shipFactory.CreateVehicle();
>        Console.WriteLine(ship.GetVehicleType()); // Vypíše: Ship
>    }
>}
>```

> [!Showcase]- ukázka implementace tovární metody v Javě
>```Java
>package com.mano.patternsdemo;
>
>public interface Employee {
>   double earnings();
>}
>
>package com.mano.patternsdemo;
>public class SalariedEmployee implements Employee {
>   private double basic;
>   private double ta;
>   private double da;
>   public SalariedEmployee(double basic,
>         double ta, double da){
>      this.basic = basic;
>      this.ta = ta;
>      this.da = da;
>   }
>
>   @Override
>   public double earnings() {
>      return basic+(basic*ta)+(basic*da);
>   }
>}
>
>package com.mano.patternsdemo;
>
>public class HourlyEmployee implements Employee {
>   private double hoursWorked;
>   private double payPerHour;
>   public HourlyEmployee(double hoursWorked,
>         double payPerHour){
>      this.hoursWorked = hoursWorked;
>      this.payPerHour = payPerHour;
>   }
 > 
>   @Override
>   public double earnings() {
>      return hoursWorked*payPerHour;
>   }
>}
>
>package com.mano.patternsdemo;
>import java.util.Scanner;
>public class EmployeeFactory {
>   public enum EmployeeType {HOURLY, SALARIED};
>   public Employee recruit(EmployeeType employeeType){
>         Employee emp;
>      Scanner scanner = newScanner(System.in);
>      switch(employeeType){
>         case HOURLY:
>            System.out.println("Enter Hours:");
>            double h = scanner.nextDouble();
>            System.out.println("Enter pay per hour:");
>            double p = scanner.nextDouble();
>            emp = new HourlyEmployee(h,p);
>            break;
>         case SALARIED:
>            System.out.println("Enter Basic:");
>            double basic = scanner.nextDouble();
>            System.out.println("Enter TA:");
>            double ta = scanner.nextDouble();
>            System.out.println("Enter DA:");
>            double da = scanner.nextDouble();
>            emp = new SalariedEmployee(basic,ta,da);
>            break;
>         default:
>            emp = null;
>            break;
>      }
>      return emp;
>   }
>}
>
>package com.mano.patternsdemo;
>public class Main {
>   public static void main(String[] args) {
>      EmployeeFactory employeeFactory = new EmployeeFactory();
>      Employee emp1 = employeeFactory.recruit(EmployeeFactory
>         .EmployeeType.HOURLY);
>      Employee emp2 = employeeFactory.recruit(EmployeeFactory
>         .EmployeeType.SALARIED);
>      System.out.println("emp1 earns $"+emp1.earnings());
>      System.out.println("emp2 earns $"+emp2.earnings());
>   }
>}
>```


</div></div>

## Builder

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- umožňuje vytvářet ==složité objekty krok za krokem==
- umožňuje vytvářet různé typy a reprezentace objektu pomocí stejného konstrukčního kódu
- Vzor Builder je v jazyce C# dobře známý. Je užitečný zejména tehdy, když potřebujete vytvořit objekt s mnoha možnostmi konfigurace.


> [!Info]- Jaký problém řeší builder pattern?
> Představte si složitý objekt, který vyžaduje pracnou postupnou inicializaci mnoha polí a vnořených objektů. Takový inicializační kód je obvykle pohřben uvnitř monstrózního konstruktoru se spoustou parametrů.
>
>Ve většině případů bude většina parametrů nepoužitá, takže volání konstruktoru bude dost ošklivé. Například jen zlomek domů má bazény, takže parametry týkající se bazénů budou v devíti příkladech z deseti nepoužité.
>
>Vzor builder organizuje konstrukci objektu do sady kroků (`buildWalls`, `buildDoor` atd.). Chcete-li vytvořit objekt, provedete sérii těchto kroků na objektu builder.
>
>Důležité je, že nemusíte volat všechny kroky. Můžete volat pouze ty kroky, které jsou nezbytné pro vytvoření konkrétní konfigurace objektu

![Pasted image 20240325181605.png](/img/user/Images/Pasted%20image%2020240325181605.png)

## Builder s directorem
- Přidání directora je další krok patternu builder
- Třída director ==definuje pořadí, v jakém se mají provádět== jednotlivé kroky stavby, zatímco třída ==builder zajišťuje implementaci== těchto kroků.
- ==Použít třídu Director **není** pro pattern builder nutné==
![Pasted image 20240325213325.png](/img/user/Images/Pasted%20image%2020240325213325.png)

> [!Showcase]- Ukázka kódu využívajícího pattern builder i s directorem
>```CSharp
>using System;
>using System.Collections.Generic;
>
>namespace RefactoringGuru.DesignPatterns.Builder.Conceptual
>{
>    public interface IBuilder
>    {
>        void BuildPartA();
>        void BuildPartB();
>        void BuildPartC();
>    }
>
>    public class ConcreteBuilder : IBuilder
>    {
>        private Product _product = new Product();
>
>        public ConcreteBuilder()
>        {
>            this.Reset();
>        }
>
>        public void Reset()
>        {
>            this._product = new Product();
>        }
>
>        public void BuildPartA()
>        {
>            this._product.Add("PartA1");
>        }
>
>        public void BuildPartB()
>        {
>            this._product.Add("PartB1");
>        }
>
>        public void BuildPartC()
>        {
>            this._product.Add("PartC1");
>        }
>      
>        public Product GetProduct()
>        {
>            Product result = this._product;
>            this.Reset();
>            return result;
>        }
>    }
>
>    public class Product
>    {
>        private List\<object> _parts = new List\<object>();
>        public void Add(string part)
>        {
>            this._parts.Add(part);
>        }
>
>        public string ListParts()
>        {
>            string str = string.Empty;
>            for (int i = 0; i < this._parts.Count; i++)
>            {
>                str += this._parts[i] + ", ";
>            }
>            str = str.Remove(str.Length - 2); // removing last ",c"
>            return "Product parts: " + str + "\n";
>        }
>    }
>
>    public class Director
>    {
>        private IBuilder _builder;
>        public IBuilder Builder
>        {
>            set { _builder = value; }
>        }
>
>        // Director dokáže rychle dělat několik nejčasteji používaných kombinací pomocí stejných kroků
>        public void BuildMinimalViableProduct()
>        {
>            this._builder.BuildPartA();
>        }
>
>        public void BuildFullFeaturedProduct()
>        {
>            this._builder.BuildPartA();
>            this._builder.BuildPartB();
>            this._builder.BuildPartC();
>        }
>    }
  >  
>    class Program
>    {
>        static void Main(string[] args)
>        {
>            var director = new Director();
>            var builder = new ConcreteBuilder();
>            director.Builder = builder;
>
>            Console.WriteLine("Standard basic product:");
>            director.BuildMinimalViableProduct();
>            Console.WriteLine(builder.GetProduct().ListParts());
  >          
>            Console.WriteLine("Standard full featured product:");
>            director.BuildFullFeaturedProduct();
>            Console.WriteLine(builder.GetProduct().ListParts());
>
>            // Builder pattern dokáže vytvářet i vlastní produkty bez directora
>            Console.WriteLine("Custom product:");
>            builder.BuildPartA();
>            builder.BuildPartC();
>            Console.Write(builder.GetProduct().ListParts());
>        }
>    }
>}
>```

</div></div>

## Singleton

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/patterny/singleton/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- Díky singletonu lze vytvořit **pouze** jednu instanci z třídy
- Lze přistupovat ke stejné instanci třídy z jakékoliv části kódu
- Při vytvoření další instance dostane uživatel stejnou instanci se stejnými daty
- Instance je vytvořena v moment, kdy je poprvé zapotřebí

![Pasted image 20240325181205.png](/img/user/Images/Pasted%20image%2020240325181205.png)

> [!Tip] Využití
> Vzor Singleton použijte, pokud by třída v programu měla mít pouze jednu instanci dostupnou všem klientům; například jeden databázový objekt sdílený různými částmi programu

> [!Showcase]- Ukázka implementace singletonu v C#
>```CSharp
>// jednoduchý singleton
>public class Singleton  
>{  
>    private static Singleton? _instance;  
>    public static Singleton Instance { get => _instance ??=new Singleton(); }  
>}
>
>// Thread-safe singleton
>class Singleton
>    {
>	    // konstruktor singletonu
>       private Singleton() 
>        { 
>        
>        }
>        
>        // do této atributy se ukládá singleton
>        private static Singleton _instance;
>        
>        // lock, který se stará o to, aby se k singletonu 
>        // přistupovali vždy jen z jednoho vlákna
>        private static readonly object _lock = new object();
>        
>        // metoda GetInstance vrací 
>        public static Singleton GetInstance()
>        {
>            if (_instance == null)
>            {
>                lock (_lock)
>                {
>                    if (_instance == null)
>                    {
>                        _instance = new Singleton();
>                    }
>                }
>            }
>            return _instance;
>        }
>    }
>```

</div></div>

## Decorator
![[DecoratorCSharp\|DecoratorCSharp]]