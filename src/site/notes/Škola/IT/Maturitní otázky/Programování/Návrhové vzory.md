---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Návrhové vzory/","created":"2023-12-19T09:15:02.441+01:00","updated":"2024-03-25T22:27:45.356+01:00"}
---

#Maturitní_otázka #IT #Programování 
# K čemu slouží návrhové vzory
- jsou souborem nástrojů pro ==řešení běžných problémů== při návrhu softwaru
- slouží jako společný jazyk pro ==ulehčení práce== vývojářů, aby nemuseli dokola vymýšlet stejná řešení
- pomáhají týmu vývojářů ==lépe komunikovat==
- Každý vzor je jako plánek, který můžete upravit tak, abyste vyřešili konkrétní návrhový problém ve vašem kódu
# Interface

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



#IT #Programování #C-Sharp 
- další způsob jak dosáhnout abstrakce
- je to ==kompletně abstraktní==
- může obsahovat pouze abstraktní metody a vlastnosti s prázdným tělem -> má ==pouze podpisy metod a vlastností==

> [!Showcase] Ukázka interfacu
> ```Csharp
>// interface
>interface Animal 
>{
>  void animalSound(); // interface metoda (nemá tělo)
>  void run(); // interface metoda (nemá tělo)
>}
>```

- ==musí být implementovány== (stejným způsobem jako zdědění)  

> [!Showcase] Ukázka implementace interfacu
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
![[GenericClassCsharp\|GenericClassCsharp]]
# Návrhové vzory
## Servant
![[ServantPattern\|ServantPattern]]
## Messenger
![[MessangerPattern\|MessangerPattern]]
## Factory

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





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

## Ukázka provedení builderu i s directorem

```CSharp
using System;
using System.Collections.Generic;

namespace RefactoringGuru.DesignPatterns.Builder.Conceptual
{
    public interface IBuilder
    {
        void BuildPartA();
        void BuildPartB();
        void BuildPartC();
    }

    public class ConcreteBuilder : IBuilder
    {
        private Product _product = new Product();

        public ConcreteBuilder()
        {
            this.Reset();
        }

        public void Reset()
        {
            this._product = new Product();
        }

        public void BuildPartA()
        {
            this._product.Add("PartA1");
        }

        public void BuildPartB()
        {
            this._product.Add("PartB1");
        }

        public void BuildPartC()
        {
            this._product.Add("PartC1");
        }
        
        public Product GetProduct()
        {
            Product result = this._product;
            this.Reset();
            return result;
        }
    }

    public class Product
    {
        private List<object> _parts = new List<object>();
        public void Add(string part)
        {
            this._parts.Add(part);
        }

        public string ListParts()
        {
            string str = string.Empty;
            for (int i = 0; i < this._parts.Count; i++)
            {
                str += this._parts[i] + ", ";
            }
            str = str.Remove(str.Length - 2); // removing last ",c"
            return "Product parts: " + str + "\n";
        }
    }

    public class Director
    {
        private IBuilder _builder;
        public IBuilder Builder
        {
            set { _builder = value; }
        }

        // Director dokáže rychle dělat několik nejčasteji používaných kombinací pomocí stejných kroků
        public void BuildMinimalViableProduct()
        {
            this._builder.BuildPartA();
        }

        public void BuildFullFeaturedProduct()
        {
            this._builder.BuildPartA();
            this._builder.BuildPartB();
            this._builder.BuildPartC();
        }
    }
    
    class Program
    {
        static void Main(string[] args)
        {
            var director = new Director();
            var builder = new ConcreteBuilder();
            director.Builder = builder;

            Console.WriteLine("Standard basic product:");
            director.BuildMinimalViableProduct();
            Console.WriteLine(builder.GetProduct().ListParts());
            
            Console.WriteLine("Standard full featured product:");
            director.BuildFullFeaturedProduct();
            Console.WriteLine(builder.GetProduct().ListParts());

            // Builder pattern dokáže vytvářet i vlastní produkty bez directora
            Console.WriteLine("Custom product:");
            builder.BuildPartA();
            builder.BuildPartC();
            Console.Write(builder.GetProduct().ListParts());
        }
    }
}
```

</div></div>

## Singleton

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




- Díky singletonu lze vytvořit **pouze** jednu instanci z třídy
- Lze přistupovat ke stejné instanci třídy z jakékoliv části kódu
- Při vytvoření další instance dostane uživatel stejnou instanci se stejnými daty
- Instance je vytvořena v moment, kdy je poprvé zapotřebí

![Pasted image 20240325181205.png](/img/user/Images/Pasted%20image%2020240325181205.png)

> [!Tip] Využití
> Vzor Singleton použijte, pokud by třída v programu měla mít pouze jednu instanci dostupnou všem klientům; například jeden databázový objekt sdílený různými částmi programu

> [!Showcase]- Ukázka:
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
