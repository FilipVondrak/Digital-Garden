---
{"dg-publish":true,"permalink":"/Škola/IT/Šifrování/","tags":["IT"],"created":"2024-02-07T19:36:26.728+01:00","updated":"2024-05-24T18:18:05.438+02:00"}
---

# Co je to šifrování
- převod dat do nečitelné podoby pro lidi, kteří nemají klíč/neví jak je vrátit zpět
- dají se opačným postupem vrátit do původní podoby
- šifrování se děje na 6. vrstvě [[Škola/IT/ISO OSI\|ISO OSI]]
# Způsoby šifrování dat
- **Podle Implementace**
	- [Softwarově](Softwarové%20šifrování.md)
	- [Hardwarově](Hardwarové%20šifrování.md)
- **Podle šifry**
	- [[Škola/IT/Symetrické šifrování\|Symetrické šifrování]]
	- [[Škola/IT/Asymetrické šifrování\|Asymetrické šifrování]]
# Jak softwarově šifrovat 
### Bitlocker

# End-to-end šifrování
- Přenos dat ochráněn proti odposlechu
- Šifrování po celé cestě dat
    - Od klienta na server i ze serveru na dalšího klienta a od klienta ke klientovi
    - Může odposlouchávat dále, ale jen šifrované data
## OpenPGP
- End-to-end pro e-mail
- Digitální podpisy
- Šifrované e-mailové zprávy
## S/MIME
- Kryptografické zabezpečení pro e-maily
    - Autentizace (podpis)
    - Integrita zpráv
    - Zabezpečení dat (šifrování)

## OTR
- Šifrování pro instant messaging
- Používá symetrickou šifru
- Zabezpečuje
    - Autentizaci
    - Šifrování
    - Dopředná bezpečnost - starší zprávy budou stále zašifrované