---
{"dg-publish":true,"permalink":"/Škola/IT/Protokoly/FTP/","created":"2023-12-14T18:50:39.857+01:00","updated":"2024-05-04T20:01:55.817+02:00"}
---

## Co je FTP
- Slouží pro přenos souborů mezi z jednoho počítače na jiný
- nejstarší protokol pro přenos v síti
- používá **[[Škola/IT/Protokoly/TCP\|TCP]]**
- ==zabezpečené FTP používá [[SSL\|SSL]]== -> **FTPS** 
## Využití
- Přenos velkých dat
- možno poslat několik souborů naráz
- stahování ISO souborů
## Porty pro FPT
- FPT -> **21**
- FPTS -> **990**
## Jak použít
1. Přes prohlížeč
	- s prohlížečem není potřeba žádný speciální software pro stahování souborů ze serveru
2. FTP GUI klient
	- použití third-party aplikací může ulehčit uživateli odesílání souborů a připojování k serveru
		- **FTP aplikace**
			- Klienti
				- Prohlížeč
				- Windows File Explorer
				- TotalCommander
			- Servery
				- FileZilla
				- Caesar FTP
				- Cerberus FTP
1. Command-line FTP
	- většina velkých operačních systémů už mají zabudovaný 
## Jak funguje
- funguje tak, že se otevřou dvě spojení, která propojí počítače snažící se vzájemně komunikovat
- Jedno spojení je určeno pro příkazy a odpovědi, které se posílají mezi dvěma klienty
	- **Příkazy**
		- send
		- get
		- change directory
		- transfer
- druhý kanál zajišťuje přenos dat
	- **režimy přenosu dat**
		- block
			- rozděluje data do bloků
		- stream
			- umožňuje FTP spravovat informace v řetězci dat bez jakýchkoli hranic mezi nimi
		- compressed
			- používá algoritmus Lepmep-Ziv na kompresování dat