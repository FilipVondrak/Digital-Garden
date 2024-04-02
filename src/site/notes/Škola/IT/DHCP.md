---
{"dg-publish":true,"permalink":"/Škola/IT/DHCP/","created":"2024-03-14T18:45:24.167+01:00","updated":"2024-03-14T18:51:07.843+01:00"}
---

#IT #Software #Protokol
-> Dynamic Host Configuration Protocol
## Využití
- dynamická konfigurace síťového rozhraní
## Výhody oproti statickým IP adresám
- **Automatické přidělování IP adres**
	- Nemusíte ručně nastavovat IP adresu na každém zařízení, což šetří čas a minimalizuje chyby
- **Dynamické přidělování**
	- IP adresy jsou přidělovány pouze po dobu, kdy je zařízení zapnuté a připojené k síti. Tím se šetří vzácné IP adresy, což je důležité zejména u velkých sítí.
- **Centrální správa**
	- Konfiguraci sítě lze snadno spravovat na jednom místě - na serveru DHCP
## Princip
1. Po připojení zařízení k síti vyšle klient na server DHCP zprávu s dotazem na IP adresu
2. Server DHCP odpoví nabídkou volné IP adresy z jeho fondu
3. Klient si tuto nabídku vyžádá a server mu zašle kromě IP adresy i další důležité informace, jako je maska podsítě, výchozí brána a DNS servery
4. Zařízení pak může na základě získaných informací komunikovat v síti
![](https://lh7-us.googleusercontent.com/Z2Uf8LIQXLvDlb7l9dF50MLf-kXp1SvQKkzoyUxV7QhtpFEgCVgWWnrLU1rX_KyWQPnuPN3yEitrd2FPgiJwENPYUlOgRbn38N6E6Cy-4liZ8URA5hlEvUmDn4pL9tzxIHpYlHyNn5YhBQMUQCCq29o)
