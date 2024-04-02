---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Návrhové vzory - Utility, Singleton + tovární metoda, Enum/","created":"2024-03-29T16:56:08.915+01:00","updated":"2024-03-29T15:59:46.433+01:00"}
---

# K čemu slouží návrhové vzory
- jsou souborem nástrojů pro ==řešení běžných problémů== při návrhu softwaru
- slouží jako společný jazyk pro ==ulehčení práce== vývojářů, aby nemuseli dokola vymýšlet stejná řešení
- pomáhají týmu vývojářů ==lépe komunikovat==
- Každý vzor je jako plánek, který můžete upravit tak, abyste vyřešili konkrétní návrhový problém ve vašem kódu
# Utility

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/patterny/utility-pattern/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- vzor utility/helper je užitečný pro vytvoření neinicializovatelné třídy
- obvykle pomáhá udržet nejrůznější nesouvisející metody na jednom místě
- měly by být ==všechny metody deklarované ve třídě statické==
-  jediným způsobem, jak zajistit neinstantnost, je deklarovat konstruktor jako **private**

> [!Showcase]- Ukázka implementace utility vzoru v Javě
>```Java
>public class Utility {
>   private Utility(){
>
>   }
  > 
>   public static Boolean compareSomething(){
>      // ...
>      return false;
>   }
>
>   public static void shuffleTheList(List\<String> list){
      // ...
   }
>
>   public static void doSomething(){
>      // ...
>   }
>}
>```

</div></div>

# Singleton

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
>    public static Singleton Instance { get => _instance ??=new UserPreferences(); }  
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

# Tovární metoda

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/patterny/factory-pattern/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- Poskytuje rozhraní pro vytváření objektů v nadtřídě, ale umožňuje podtřídám měnit typ objektů, které budou vytvořeny.
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
package com.mano.patternsdemo;
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

# Enum

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/osobni/programovani/enum/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- je to **speciální** "třída", která ==reprezentuje skupinu konstant== (neměnných)
- pro vytvoření enumu, stačí použít **keyword** enum

## Ukázka
### vytvoření enumu
```csharp
enum Level 
{
  Low,
  Medium,
  High
}
```
### použití enumu 
```csharp
Level myVar = Level.Medium;

switch (myVar)
{
  case Level.Low:
    System.out.println("Low level");
    break;
  case Level.Medium:
    System.out.println("Medium level");
    break;
  case Level.High:
    System.out.println("High level");
    break;
}
```

</div></div>
