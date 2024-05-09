---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/SQL databáze/","tags":["Maturitní_otázka","IT","Programování"],"created":"2023-12-19T09:11:59.160+01:00","updated":"2024-05-09T17:05:38.404+02:00"}
---

# Co jsou SQL (relační) databáze
- jsou nejpoužívanější ze všech typů databází
- pro identifikování jednotlivých záznamů se používá primární klíč, nejčastěji ve formě ID
- všechny data jsou v podobě tabulek
- v tabulce se data zapisují do sloupců a řádků
- první řádek je předloha, jak mají být data zapsána a v jakých datových typech
- tabulky mohou být navzájem propojené **foreign klíčem**
![Pasted image 20240509161447.png](/img/user/Images/Pasted%20image%2020240509161447.png)
# Jazyk SQL
- SQL je standardní jazyk pro práci s relačními databázemi
- byl vyvinut v 70. letech 20. století firmou IBM
## Syntaxe SQL jazyka
- má jednoduchou syntaxi, což usnadňuje 
- základná klíčová slova jsou:
	- **SELECT** -> používá se k výběru dat z databáze 
	- **INSERT** -> slouží k vkládání nových záznamů do databáze
	- **UPDATE** -> aktualizuje a upraví existující záznamy v databázi
	- **DELETE** -> smaže záznamy z databáze
- pro pokročilé příkazy se používají tato klíčová slova:
	- **WHERE** -> podmínka při provedení dotazu
	- **ORDER BY**
	- **GROUP BY**
	- **HAVING**
	- **JOIN** -> slouží k propojení dat z různých tabulek na základě parametrů
	- **INDEX** -> vytvoří indexy tabulek a zrychluje tím provádění dotazů
	- **TRANSACTION** -> umožňuje provádět souborné operace, které buď proběhnout všechny úspěšně, nebo žádná neprojde
> [!Showcase]- Ukázka jednoduchého SQL požadavku
> Následující požadavek přidá do tabulky Products_table novou položku
>```SQL
> INSERT INTO Products_table (brand_name, cost) VALUES (‘A’,’499’);
>```
# Vztahy mezi tabulkami
### 1 ku 1 (one-to-one)
- tento vztah znamená, že jeden záznam v tabulce je spojen maximálně s jedním dalším záznamem z jiné tabulky
- v praxi se používá málo kdy, jelikož se většinou dají data spojit do 1 tabulky
- občas se používá k oddělení zvláštních dat

> [!Tip] Příklad použití
> Vztah mezi osobou a řidičským průkazem.
> Každá osoba může mít pouze jeden řidičský průkaz a každý řidičský průkaz může být přiřazen pouze jedné osobě.

> [!Showcase] Příklad provedení
> U adresy se použije foreign key, který se propojí s primárním klíčem u studenta
> 
student: student_id, first_name, last_name, address_id
address: address_id, address, city, zipcode, student_id
### 1 ku n (one-to-many)
- je nejběžnější
- jeden záznam v tabulce (zvané rodičovská tabulka) může být spojen s mnoha záznamy v druhé tabulce (zvaná dětská tabulka)
- Typickým způsobem propojení těchto tabulek je použití primárního klíče z rodičovské tabulky jako foreign key v dětské tabulce

> [!Tip] Příklad použití
> Vztah mezi kategorií a produkty v e-shopu.
> Jedna kategorie může obsahovat mnoho produktů, ale každý produkt může být přiřazen pouze jedné kategorii.

> [!Showcase] Příklad provedení
> U tříd se použije foreign key, který se propojí s primárním klíčem u učitele
> 
teachers: teacher_id, first_name, last_name # "jedna" strana
classes:  class_id, class_name, teacher_id  # "mnoho" stran

### n ku n (many-to-many)
- Pro tento typ vztahu se přímo nevyužívají foreign keys v tabulkách
- vytváří se pomocná (spojovací/propojovací) tabulka, která obsahuje vazby mezi oběma původními tabulkami
- Tato pomocná tabulka má obvykle dva foreign key, které odkazují na primární klíče původních tabulek

> [!Tip] Příklad použití
> Vztah mezi studenty a kurzy.
> Jeden student může být přihlášen k mnoha kurzům a jeden kurz může mít mnoho studentů.

> [!Showcase] Příklad provedení
> Použijeme propojovací tabulku student_classes, která propojí studenty a třídy
> 
student: student_id, first_name, last_name
classes: class_id, name, teacher_id
student_classes: class_id, student_id     # propojovací tabulka
# Hrozby 
## SQL injection
- typ útoku na webové aplikace
- je prováděn vložením SQL kódu do vstupních polí webových formulářů nebo URL adres
- Tímto způsobem útočník může ovlivnit chování databáze a získat neoprávněný přístup k citlivým datům, nebo dokonce poškodit nebo smazat data v databázi