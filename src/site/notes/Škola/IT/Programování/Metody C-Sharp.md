---
{"dg-publish":true,"permalink":"/Škola/IT/Programování/Metody C-Sharp/","tags":["IT","Programování","SPOSDK","Maturitní_otázka"],"created":"2024-03-19T15:21:52.976+01:00","updated":"2024-05-11T19:41:00.168+02:00"}
---

- podprogram, který pracuje s daty/atributy
- je blok kódu, který je samostatně spustitelný a plní specifickou úlohu
- Může pracovat s daty a atributy 
- lze ho opakovaně volat z jiných částí programu

___
# Dělení metod
## Procedura
- Nevrací žádné data - návratový typ **void**
- provede úkol a skončí
## Funkce
- vrací data
- **musí** mít ==v zápisu datový typ==, který se má vrátit
- **musí** obsahovat keyword **return**
- na rozdíl od procedury se jinak volá
___
# Návratový typ
- Návratový typ určuje, jaký typ dat funkce vrátí.
- Běžné typy zahrnují `int`, `double`, `string` a `bool`
- lze taky použít vlastní návratové typy

___
# Parametry
- Parametry jsou vstupní data, která se předávají funkci při jejím volání
- Parametry se uvádějí v závorkách za názvem funkce.
- Každý parametr má svůj typ a název

___
# Statické/Nestatické
## Statické
- Statické členy (metody a atributy) **nejsou** vázány na konkrétní instanci třídy
- Existují pouze v rámci třídy a jsou přístupné bez nutnosti vytvářet instanci
- Jsou nutné např. k patternu [[Osobní/Programování/Patterny/Singleton\|Singleton]]
## Nestatické
- vždy musíme vytvořit instanci
- Nestatické členy (metody a atributy) **jsou** vázány na konkrétní instanci třídy
- Pro přístup k nim je nutné nejprve vytvořit instanci třídy
___
# Modifikátory přístupu

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/programovani/modifikatory-pristupu-c-sharp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Private
- Modifikátor `private` určuje, že člen (atribut nebo metoda) je přístupný **pouze** v rámci třídy, ve které je definován.
## Public
- Modifikátor `public` určuje, že člen je ==přístupný z libovolného kódu==, který má přístup k instanci třídy.
## Protected
- Modifikátor `protected` určuje, že člen je přístupný pouze v rámci třídy ==a z tříd odvozených/zděděných==
## Internal
- Modifikátor `internal` určuje, že člen je přístupný ze stejné assembly

</div></div>
