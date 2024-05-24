---
{"dg-publish":true,"permalink":"/Škola/IT/Programování/InterfaceCsharp/","tags":["IT","Programování","C-Sharp"],"created":"2024-03-25T22:28:08.815+01:00","updated":"2024-05-20T13:11:01.133+02:00"}
---

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
>// Interface
>interface IAnimal 
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