---
{"dg-publish":true,"permalink":"/Škola/IT/ISO OSI/Transportní vrstva/","created":"2024-05-05T19:37:33.458+02:00","updated":"2024-05-05T20:41:17.250+02:00"}
---

-> **Transport Layer**
## Co je transportní vrstva
- je to 4. vrstva [[Škola/IT/ISO OSI\|ISO OSI]] modelu
- přidává porty zdroje a destinace do headeru segmentu
## Hlavní funkce
- poskytuje potvrzení o doručení
- pokud je v datech chyba, tak je pošle znova
### Segmentace
- při odesílání přijme data z [[Relační vrstva\|relační vrstvy]] a rozdělí je do několika menších segmentů
### Složení dat
- transportní vrstva u příjemce příjímá rozdělená data a skládá je zpět
### Service Point Addressing
- aby se data doručily do správné destinace, tak se transportní vrstva stará o přidávání portů
- data se doručí správnému procesu
## Postup vytvoření segmentů
### Na straně odesílatele
1. Přijme formátovaná data z vyšších vrstev
2. Provede segmentaci
3. Přidá kontrolu průběhu a chyb, aby se zajistil bezproblémový přenos dat
4. Přidá porty zdroje a destinace do headeru
5. Pošle segment [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvě]]
### Na straně příjemce
1. transportní vrstva přečte porty
2. provede sekvencování a složí segmentovaná data
3. pošle data určité aplikaci
## Protokoly na transportní vrstvě
### TCP - Transmission Control Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/tcp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- spolehlivý, spojovaný protokol  
![Pasted image 20240505202256.png](/img/user/Images/Pasted%20image%2020240505202256.png)
## Využití
 - web. Stránky, 
 - emaily, 
 - služby, kde se nesmí ztratit data 
## Výhody
- má detekci a opravu chyb
	- Pokud od příjemce neobdrží zprávu, že data přišla v pořádku, tak je pošle znova
## Nevýhody
-  je pomalý

</div></div>

### UDP - User Datagram Protocol

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/protokoly/udp/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




- nespolehlivý a nespojovaný protokol
	- Nemá jak zkontrolovat, zda data dorazili k příjemci
## Využití
- videa
	- video se načte rychle a nevadí, pokud pár pixelů ve snímku chybí 
- Microsoft DHCP server
## Výhody
- předává aplikaci přímí přístup k datagram delivery službě
- má minimální 
## Nevýhody
- je rychlý

</div></div>

## Zapouzdření
-> **Segment**
- Obsahuje
	- IP příjemce
	- IP odesílatele
	- Porty
	- Data