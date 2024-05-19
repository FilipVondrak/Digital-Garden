---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Návrhové vzory - Interface, Servant, Generické třídy, Messenger/","tags":["IT","Maturitní_otázka","Programování","SPOSDK"],"created":"2024-03-29T15:59:06.649+01:00","updated":"2024-05-17T18:34:48.155+02:00"}
---

# K čemu slouží návrhové vzory
- jsou souborem nástrojů pro ==řešení běžných problémů== při návrhu softwaru
- slouží jako společný jazyk pro ==ulehčení práce== vývojářů, aby nemuseli dokola vymýšlet stejná řešení
- pomáhají týmu vývojářů ==lépe komunikovat==
- Každý vzor je jako plánek, který můžete upravit tak, abyste vyřešili konkrétní návrhový problém ve vašem kódu
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

# Messenger (Přepravka)

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
