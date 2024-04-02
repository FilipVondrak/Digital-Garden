---
{"dg-publish":true,"permalink":"/Škola/IT/DNS/","created":"2024-03-18T20:53:14.123+01:00","updated":"2024-03-14T21:04:42.507+01:00"}
---

#IT #Software #SPOSDK #Maturitní_otázka 
-> Domain name services
- **port 53**
- převádí doménová jména na IP adresy (např. www.amazon.com převede na 192.0.2.44)
	- Doménová jména jsou čitelná pro lidi
	- IP adresy jsou čitelné pro zařízení

# Struktura
- . - kořen
- top level domain - .com, .cz, .edu 
- second level domain - google.com
- subdomain - photos.google.com 
![Pasted image 20240314210031.png](/img/user/Images/Pasted%20image%2020240314210031.png)
# DNS záznamy
- **A** - IPv4
- **CNAME** - Canonical Name - domény s níž souvisí subdomény (takže doména - spošdk.cz, subdomény - jidelna, moodle ..)
- **AAAA** - IPv6
- **MX** - poštovní server
- **TXT** - libovolný text (používá se např. pro ověření vlastnictví)