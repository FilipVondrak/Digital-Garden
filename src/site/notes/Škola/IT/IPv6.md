---
{"dg-publish":true,"permalink":"/Škola/IT/IPv6/","tags":["Protokol","IT"],"created":"2024-05-06T15:00:04.354+02:00","updated":"2024-05-06T20:21:27.867+02:00"}
---

## Co je IPv6
- aktuálně nejnovější verze internetového protokolu
- má 8 hextetů po 16 bitech
- má 128 bitů
- používá šestnáctkovou/hexadecimální soustavu
- jednotlivé hextety jsou odděleny **:**
	- pokud jsou 2 dvojtečky po sobě (Př. **::**), tak to znamená, že je hextet naplněn nulami, lze použít pouze jednou v IP adrese
		- Plná adresa -> 2001:0db8:0000:0000:0000:0000:0000:7334
		- Zkrácená adresa -> 2001:db8::7334
## Druhy 
![Pasted image 20240506195156.png](/img/user/Images/Pasted%20image%2020240506195156.png)
### Unicast adresy
- individuální adresy
- jeden uzel, jedno vybrané zařízení
#### Global unicast adresy
- globální individuální adresy
- jednoznačná identifikace zařízení v celém internetu
- veřejné IPv6 unikátní v celém internetu
##### Části global unicast adresy
###### Prefix
- První část adresy
- určuje síť, ke které zařízení patří
- 48/56/64 bitů
###### Subnet ID
- určuje podsíť, ke které zařízení patří v rámci globálního prefixu
- 16/8/0 bitů
###### Host ID (ID rozhraní)
- identifikuje konkrétní zařízení v síti
- zbývající část adresy
#### Local unicast adresy (ULA)
- mají **host ID** a mohou mít **subnet ID**, pokud je to nutné pro rozlišení podsítě v jedné síti
- Prefix tvoří **ULA prefix** a **ID subnetu (volitelně)**
- Unikátní lokální adresy
- individuální privátní adresy i pro více sítí
- jsou určeny pro privátní adresování v rámci sítě bez nutnosti globální registrace
- začínají sekvencí **fc00**
- Používají se pro:
	- privátní adresování v sítích, které nemají přístup k globálně registrovaným adresám
	- vnitřní komunikace v rámci velkých firem
#### Link-local adresy
- mají **host ID** ale nemají **subnet ID** ani **prefix**
- automaticky vygenerované adresy používané v rámci lokální sítě
- Individuální privátní adresy jen pro danou síť
- nejsou routovány; nemají přístup k routerům
- automaticky se generují na základě MAC adresy
- jsou méně bezpečné, jelikož je snadné je vygenerovat
- začínají sekvencí **fe80::**
- Používají se pro:
	- Automatická konfigurace adres - **SLAAC**
	- Sousedské objevování - NDP
	- lokální komunikace
### Multicast adresy
- Nemají **host ID** ani **subnet ID**
- Prefix tvoří ==rezervovaný multicastový prefix==, který identifikuje skupinu multicastových adres
- adresy určené pro skupinovou komunikaci
- nahrazuje broadcast, který se nachází u [[Škola/IT/IPv4\|IPv4]]
- začínají sekvencí **ff::**
### Anycast adresy
- Nemají **host ID** ani **subnet ID**
- Prefix tvoří ==rezervovaný anycastový prefix==, který identifikuje skupinu anycastových adres
- adresy určené pro ==komunikaci s nejbližším dostupným zařízením== z dané skupiny
- běžně se používají pro servery s replikovanými daty, aby uživatelé byli automaticky směrováni k nejbližšímu dostupnému serveru
- začínají sekvencí **ff::a**