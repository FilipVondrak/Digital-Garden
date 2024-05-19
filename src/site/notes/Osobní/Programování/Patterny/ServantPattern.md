---
{"dg-publish":true,"permalink":"/Osobní/Programování/Patterny/ServantPattern/","tags":["IT","Programování","SPOSDK","Java"],"created":"2024-03-30T20:12:00.300+01:00","updated":"2024-05-17T18:36:47.835+02:00"}
---

- vzor servant definuje objekt, který slouží k nabídnutí určité funkce skupině tříd, aniž by byla tato funkce definována v každé z nich. 
- Servant je třída, jejíž instance (nebo dokonce jen třída) poskytuje metody, které se starají o požadovanou službu, přičemž objekty, pro které (nebo s nimiž) servant něco dělá, jsou brány jako parametry
- první parametr je datového typu interface
- nepracuje sám, ale komunikuje s obsluhovanými objekty