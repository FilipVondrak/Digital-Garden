---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Návrhové vzory - Interface, Servant, Generické třídy, Messenger/","created":"2024-03-29T15:59:06.649+01:00","updated":"2024-03-29T16:01:23.769+01:00"}
---

#IT #Maturitní_otázka #Programování #SPOSDK 
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

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">





</div></div>

# Servant
![[ServantPattern\|ServantPattern]]
# Messenger
![[MessangerPattern\|MessangerPattern]]