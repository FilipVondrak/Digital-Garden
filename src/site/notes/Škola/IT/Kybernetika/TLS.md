---
{"dg-publish":true,"permalink":"/Škola/IT/Kybernetika/TLS/","created":"2024-05-19T20:25:11.187+02:00","updated":"2024-05-19T20:40:02.704+02:00"}
---

-> *Transport Layer Security*
- používá různé šifry a šifrovací sady, které definují konkrétní algoritmy pro šifrování, autentizaci, výměnu klíčů a integritu dat
- kryptografický protokol sloužící k zabezpečení komunikace v počítačových sítích
- TLS je nástupcem [[SSL\|SSL]]
## Hlavní účely
### Šifrování
- Zabezpečují data přenášená mezi klientem (např. webovým prohlížečem) a serverem tak, že jsou nečitelná pro třetí strany
### Autentizace
- Zajišťují, že obě strany komunikace (klient a server) jsou skutečně tím, kým tvrdí, že jsou
- dosahuje toho pomocí digitálních certifikátů, které ověřují identitu serveru (a někdy i klienta)
### Integrita dat
- Zajišťují, že data nebyla během přenosu změněna nebo poškozena
- Používají se hashovací funkce, které ověřují integritu přenášených dat