---
{"dg-publish":true,"permalink":"/Škola/IT/IPv4/","tags":["Protokol","IT"],"created":"2024-05-06T12:26:30.709+02:00","updated":"2024-05-06T21:06:30.391+02:00"}
---

## Co je IPv4 
- obsahuje ==4 oktety== (desítková soustava) po 8 bitech (binární)
- oktet má hodnotu 0-255
- je ==32 bitová==
- jednotlivé oktety jsou odděleny tečkou - **.**
- příklad IPv4 adresy -> 192.168.0.1 
- **localhost** -> 127.0.0.1
### Privátní IP
- lokální (LAN) síť
- IP adresy se opakují v různých oddělených privátních sítích
### Veřejná IP
- Unikátní na celém světě
- Neopakuje se nikde
- Dostupnost služeb, odkudkoliv na světě
## Maska sítě
- speciální IP adresa
- Rozděluje IP adresu na NET ID a HOST ID
	- maskuje levou část
	- Neměnná: 1 = NET ID 
	- Měnná: 0 = HOST ID 
	- popř SUBNET ID
- 4 oktety, 0-255
- zapisuje se za IP adresu -> říká se jí **prefix**
	- Např. 10.19.0.0 **/16**
- Třídy A, B, C
	- A -> /8
	- B -> /16
	- C -> /24

| Třída | Rozsah veřejných IP adres | Rozsah privátních adres       | Prefix    |
| ----- | :------------------------ | ----------------------------- | --------- |
| A     | 1.0.0.0 - 127.0.0.0       | 10.0.0.0 - 10.255.255.255     | /8 - /15  |
| B     | 128.0.0.0 - 191.255.0.0   | 172.16.0.0 - 172.31.255.255   | /16 - /23 |
| C     | 192.0.0.0 - 223.255.255.0 | 192.168.0.0 - 192.168.255.255 | /24 - 31  |

## Adresa sítě
- Adresa sítě určuje skupinu zařízení v rámci dané sítě
## Broadcast
- Broadcast adresa v IPv4 slouží k odesílání paketů všem zařízením v dané síti najednou
- je to poslední adresa v (pod)síti
## Počítání IPv4
- potřebujeme minimálně 2 bity pro podsítě, jinak budeme mít jednu velkou síť