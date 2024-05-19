---
{"dg-publish":true,"permalink":"/Osobní/Programování/Patterny/MessangerPattern/","created":"2024-05-17T16:39:14.850+02:00","updated":"2024-05-17T18:35:31.684+02:00"}
---

- česky -> Přepravka
- slouží pro přenos dat z jednoho určitého typu
- třída přepravky má stejné atributy jako třída, ze které bude přenášet informace 
- je to objekt určený k uložení skupiny údajů "pod jednu střechu" a jejich společnému transportu

> [!tip] Použití
> Pokud mám třídu s privátními atributy a chci přečíst tyto hodnoty z jiné třídy, tak je možné použít přepravku. Přepravka přečte privátní atributy a  uloží si je k sobě jako konstanty, které nelze změnit. Ostatní třídy poté mohou přepravku číst ale nikov měnit tyto hodnoty.

> [!info]
> Přepravka je zbytečná. Učí se pouze ve škole.