---
{"dg-publish":true,"permalink":"/Škola/IT/Protokoly/HTTP/","created":"2023-12-14T18:50:59.704+01:00","updated":"2024-05-19T20:25:15.089+02:00"}
---

## Co je HTTP
- je internetový protokol určený pro komunikaci s WWW servery
- Slouží pro přenos hypertextových dokumentů ve formátu HTML, XML, i jiných typů souborů
- Pro zabezpečení HTTP se často používá [[Škola/IT/Protokoly/TLS\|Škola/IT/Protokoly/TLS]] spojení nad TCP -> **HTTPS**
## Porty HTTPS
- HTTP -> **80**
- HTTPS -> **443**
## Fungování protokolu
- Protokol funguje způsobem ==dotaz-odpověď==
- Uživatel pošle serveru dotaz ve formě textu (označení dokumentu, informace o prohlížeči, …)
- Server pošle odpověď (zda se dokument podařilo najít, typ dokumentu, …)
## Metody
### Nejčastější metody
#### GET
- Požadavek na uvedený objekt se zasláním případných dat (proměnné prohlížeče, session id, …)
- ==Výchozí metoda== při požadavku na zobrazení hypertextových stránek
- ==Celkově nejpoužívanější==
#### POST
- ==Odesílá uživatelská data== na server
- Data může odesílat i metoda GET, metoda POST se však používá pro příliš velký objem dat, nebo pokud není vhodné přenášená data zobrazit jako součást [[URL\|URL]]
	- víc než 512 bajtů, což je velikost požadavku GET
- data předávaná metodou POST jsou obsažena v HTTP požadavku
#### DELETE
- ==Smaže uvedený objekt ze serveru==
- Je zapotřebí jistých oprávnění
### Ostatní metody
#### PUT
- Nahraje data na server
- Nepoužívá se (náhrada = FTP)
#### HEAD
- Poskytne metadata (velikost, typ, datum změny)
- Podobná metodě get, akorát neposkytne data
#### CONNECT
- Spojí se s uvedeným objektem přes uvedený port
- Používá se při průchodu skrze proxy pro ustanovení kanálu SSL
#### OPTIONS
- Dotaz na server, jaké podporuje metody.
#### TRACE
- Odešle kopii obdrženého požadavku zpět odesílateli
- klient může zjistit, co na požadavku mění nebo přidávají servery, kterými požadavek prochází.