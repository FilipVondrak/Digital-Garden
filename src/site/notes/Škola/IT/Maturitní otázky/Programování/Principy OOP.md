---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Principy OOP/","created":"2024-03-29T16:56:12.651+01:00","updated":"2024-03-29T16:39:47.993+01:00"}
---

#Maturitní_otázka #IT #Programování 
# Třída

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- vytvoří si operátorem **new**, který zavolá konstruktor třídy 
- je abstraktním modelem
- používá se k definování objektů s tímto modelem
- obsahují **atributy** a **metody**, které definují chování objektu

</div></div>

# Skládání
# Dědění
- určuje vztah mezi rodičovskou třídou a naší třídou
# Zapouzdření
# Delegování
# Polymorfizmus
- metody definované v základní třídě mohou být přepsány (pomocí keywordu **override**) v odvozených třídách
- při volání přepsaných metod se použije implementace specifická pro odvozenou třídu

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