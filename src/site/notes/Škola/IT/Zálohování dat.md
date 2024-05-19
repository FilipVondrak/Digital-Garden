---
{"dg-publish":true,"permalink":"/Škola/IT/Zálohování dat/","created":"2024-05-19T17:57:21.568+02:00","updated":"2024-05-19T18:25:33.100+02:00"}
---

# Co je zálohování dat
- je to další uložení kopie na zabezpečené místo
# Typy zálohování
### Plné zálohování
### Inkrementální
### Diferenciální
### Zrcadlové 
### Zrcadlové
### Klonování disků
### Archivace
# Raid
### Raid 0
### Raid 1
### Raid 2
### Raid 3
### Raid 4
# Kam zálohovat dat
## Cloud
- vzdálené úložiště, na které přistupujeme přes internet
### Zabezpečení dat na cloudu
- na cloud posílat jen jen předem šifrovaná data
- používat [[Škola/IT/Protokoly/HTTPS\|HTTPS]] -> bezpečný přenos dat
- dělat pravidelné zálohy
- použít [[Škola/IT/VPN\|VPN]]
### Nejbezpečnější cloud - vlastní cloud
- v lokální síti
- víme, kde se data nachází
- **Důležité:** 
	- mít hodně zabezpečené úložiště
	- šifrování dat na disku
## Zabezpečení dat na lokálním počítači
- Šifrování na disku
- Dělat pravidelné zálohy
- **Fyzické zabezpečení**:
	- zámek
	- ocelové lanko - zabezpečí počítač proti odnesení, nejde přeříznout
- **Software pro šifrování dat** - na windowsech např. ==bitlocker==
- **Software pro zálohu dat** 
	- cobian backup
		- automatické ukládání
		- raidové pole
		- na externí disk / cloud
- **Souborové systémy umožňující šifrování** - NTFS, xFAT