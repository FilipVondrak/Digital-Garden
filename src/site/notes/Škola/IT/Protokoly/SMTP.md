---
{"dg-publish":true,"permalink":"/Škola/IT/Protokoly/SMTP/","created":"2023-12-14T18:50:56.265+01:00","updated":"2024-05-04T21:18:45.348+02:00"}
---

-> Simple Mail Transfer Protocol
## Co je SMTP 
- Technický standard pro posílání emailu přes síť
- slouží pro doručování, ne pro odebírání pošty
> [!Tip]- IRL přirovnání
> Poštovní služba doručí poštu do schránky, ale příjemce si musí pro zásilku do schránky dojít
## Porty
- SMTP - **25**
- SMTP (šifrované SMTP s SSL, už je zastaralé) - **465**
- SMTP (šifrované SMTP s TLS, nyní defaultní port) - **587**
## Jak funguje
- SMTP definuje proces pro výměnu dat mezi klientem a mailovým serverem
1. SMTP otevření připojení
	- První krok je ==otevření [[Škola/IT/Protokoly/TCP\|TCP]] připojení== mezi klientem a serverem
	- Zahájení procesu posílaní emailu posláním "Hello" SMTP příkazu (HELO, EHLO)
2. Přenos dat emailu
	- klient pošle sérii příkazů zároveň s daty emailu:
		- **email hlavička**
			- odesílatel a příjemce
			- destinace
			- adresy serverů, porty, protokol
			- čas a datum
			- předmět
			- název počítače a IP adresy, info o OS
		- **email tělo**
			- kontent emailu
			- ==může být plain text nebo HTML==
		- **email footer**
			- Přílohy
			- Podpis
3. MTA
	- spustí se MTA a zkontroluje doménu příjemce
	- pokud se doména liší od odesílatele, tak se podá dotaz DNS aby našel doménu příjemce
4. Zavření spojení
	- Klient oznámí serveru jakmile je přenos dat kompletní a server uzavře spojení
- obvykle není tento první emailový server poslední destinace emailu, ale server opakuje tento SMTP proces a pošle email dalšímu serveru dokud se nedostane email serveru příjemce
## SMTP příkazy
- **HELO/EHLO**
	- Zahajují SMTP připojení
	- HELO je základní verze a EHLO je specializovaný typ SMTP
- **MAIL FROM**
	- řekne emailovému serveru kdo posílá email
- **RCPT TO**
	- poslouchá příjemce emailu
	- klient pošle tento příkaz několikrát pokud má email více příjemců
- **DATA**
	- nachází se před kontentem emailu
- **RSET**
	- resetuje připojení
	- odstraní všechny dříve odeslané informace bez ukončení připojení
	- použije se v případě, že klient pošle špatné informace
- **QUIT**
	- ukončí připojení