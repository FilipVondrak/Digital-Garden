---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Vývojové prostředí BlueJ/","created":"2023-12-19T09:15:51.269+01:00","updated":"2024-03-26T12:03:10.670+01:00"}
---

#Maturitní_otázka #IT #Programování
# Tvorba tříd 
# Vztahy mezi třídami 
# Tvorba dokumentace 
# Volání statických a nestatických metod
# Užití příkazového panelu. 
# Jednosměrný uzlový seznam. 
# Návrhové vzory 
## Utility 
## Singleton + tovární metoda

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

## Enum