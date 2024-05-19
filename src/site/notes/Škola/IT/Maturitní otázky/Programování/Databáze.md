---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Databáze/","tags":["Maturitní_otázka","IT","Programování"],"created":"2023-12-19T09:11:50.151+01:00","updated":"2024-05-16T13:44:36.346+02:00"}
---

# Základní pojmy
> [!Tip]
> Je důležité rozlišovat mezi **databází** a **databázovým strojem** 
### Databáze
- Organizovaná sbírka dat, která je uložena a spravována databázovým strojem
- většinou přípona souboru .db
- soubor, kde už jsou vloženy data v elektronické podobě
- předchůdcem jsou papírové kartotéky
### Databázový stroj
- nástroj pro shromažďování a uspořádávání dat
- Software, který umožňuje uživatelům vytvářet, spravovat a používat databáze
- Běžné databázové systémy zahrnují:
	- SQLite
	- MySQL 
	- PostgreSQL 
	- Oracle Database 
	- Microsoft SQL Server
### [[Škola/IT/Data\|Data]]
- Samotná fakta a [[Škola/IT/Informace\|informace]], které jsou v databázi uloženy
- mohou být:
	- Strukturovaná - čísla, texty, datumy
	- nestrukturovaná - obrázky
	- polostrukturovaná - [[XAML\|XAML]], [[JSON\|JSON]]
### Atribut
- Vlastnost nebo charakteristika záznamu v databázi
### Datový typ
- Určuje typ dat, které může být uloženo v atributu
#### Číselné datové typy
- INT
- TINYINT
- BIGINT
- FLOAT
- REAL
#### Časové datové typy
- DATE
- TIME
- DATETIME
#### Textové datové typy
- CHAR
- VARCHAR
- TEXT
#### Další datové typy
- NVARCHAR
- BINARY
- XML
- TABLE
### Primární klíč
- Unikátní identifikátor každého záznamu v tabulce
- většinou je to ID
- nesmí se opakovat v jedné tabulce 
### Dotazy
- Příkaz, které se používají k vyhledávání a práci s daty
# Co jsou databáze
- je to organizovaná sbírka dat
- umožňuje efektivní ukládání, vyhledávání a manipulaci s velkým množstvím dat
- používají se v široké škále aplikací, od webových stránek a e-commerce systémů až po bankovní systémy a nemocniční záznamy
## Typy databází
### SQL Databáze (Relační)

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/maturitni-otazky/programovani/sql-databaze/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




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

</div></div>

### NoSQL databáze (Nerelační)
- netabulkové databáze
![Pasted image 20240511225002.png](/img/user/Images/Pasted%20image%2020240511225002.png)
#### Key-value databáze
- nejlehčí forma NoSQL databáze
- každá položka má svůj klíč, například ID, a svoji hodnotu
- hodnota může být pole dat
- mohl by to být například nákupní košík, kde každá položka v košíku bude zapsány v poli dat 
- **přirovnání:** v C# by to mohl být Dictionary<TKey, TValue>
- **Databázové stroje používající tento princip:** Redis, Memcached
#### Dokumentová databáze
- ukládá data do dokumentů
- může být užitečné při práci s polo-strukturovanými daty
- typicky ukládáno v **JSON** nebo **XML** dokumentech
- **Databázové stroje používající tento princip:** MongoDB
#### Vektorová databáze
- ideální pro vyhledávání podle podobnosti
- efektivní s více dimenzionálními daty
- zvládají velké data-sety
- data jsou ukládány jako matematické reprezentace
- používají se pro umělou inteligenci
![Pasted image 20240511225205.png](/img/user/Images/Pasted%20image%2020240511225205.png)
## K čemu slouží databáze
- Ukládání a správa strukturovaných dat
- Efektivní přístup k datům pro různé aplikace
- Zachování integrity a konzistence dat
- Zajištění dostupnosti dat
- Sdílení dat mezi uživateli a systémy
## Umístění databází
- **Lokální** 
	- Databáze je umístěna na stejném serveru jako aplikace
	- může nabízet lepší výkon
- **Vzdálená** 
	- Databáze je umístěna na jiném serveru než aplikace
	- často hostována na cloudu
# Normalizace
- Proces uspořádání dat v databázi tak, aby se minimalizovala redundance a zlepšila se integrita dat
- **Eliminace redundance** -> Ukládání dat pouze jednou v databázi
- Prevence nesprávných nebo nesmyslných dat