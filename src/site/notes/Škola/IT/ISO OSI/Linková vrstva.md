---
{"dg-publish":true,"permalink":"/Škola/IT/ISO OSI/Linková vrstva/","created":"2024-02-22T18:02:23.970+01:00","updated":"2024-05-05T19:41:10.372+02:00"}
---

-> **Data Link Layer** (DLL)
## Co je linková vrstva
- známá také jako spojová vrstva nebo vrstva datového spoje
- Je to bezpečná, opravuje chyby
- Kóduje a dekóduje data
- považuje se za nejkomplexnější vrstvu [[Škola/IT/ISO OSI\|ISO OSI]]
## Průběh dat
1. Linková vrstva přijme data ze [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvy]] ve formě packetů
2. Rozdělí packety do rámců
3. Přidá do na začátek a konec speciální bity pro opravu chyb a adresaci
4. Pošle rámce bit-po-bitu do [[Škola/IT/ISO OSI/Fyzická vrstva\|fyzické vrstvy]]
![Pasted image 20240505140420.png](/img/user/Images/Pasted%20image%2020240505140420.png)
## Podvrstvy
### Logical Link Control (LLC)
- stará se o flow control
- je zodpovědná za poskytování chybových zpráv a potvrzení
- Používá ji například protokol NetBIOS Frames
- Většina protokolů ji nepoužívají, místo ní se o flow control a error management stará protokol [[Škola/IT/Protokoly/TCP\|TCP]] na [[Škola/IT/ISO OSI/Transportní vrstva\|transportní vrstvě]] 
### Media Access Control (MAC)
- stará se o interakce zařízení
- adresuje rámce
- ovládá přístup k fyzickým médiím
## Hlavní funkce
### Vytváření rámců
#### Na straně odesílatele
1. Přijme packety ze [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvy]] a přidá k nim speciální bity pro opravu chyb a adresaci
2. Postupně pak předá bit po bitu do [[Škola/IT/ISO OSI/Fyzická vrstva\|fyzické vrstvy]]
#### Na straně příjemce
1. Linková vrstva si vezme bity z [[Škola/IT/ISO OSI/Fyzická vrstva\|fyzické vrstvy]] a zorganizuje je do rámce
2. Zpracuje rámec
3. Pošle ho do [[Škola/IT/ISO OSI/Síťová vrstva\|síťové vrstvy]]
### Zajištění spolehlivé komunikace
- zajišťovat spolehlivou komunikaci mezi dvěma nebo více uzly v jednom datovém spoji
	- **Typy datových spojů**
		- Dvoubodový
			- sériová linka spojující 2 počítače
		- Mnohabodový
			- Lokální (LAN) sítě
### Fyzické adresování
 - přidá k datům MAC adresy odesílatele a příjemce
 - MAC je unikátní fyzická adresa, která je přiřazená zařízení při výrobě
### Řízení přístupu k MAC
### Detekce chyb
- Odpovědnost linkové vrstvy je detekce a oprava chyb při přenosu
- Používá tyto techniky
	- [Pro detekci](https://www.geeksforgeeks.org/error-detection-in-computer-networks/)
	- [Pro opravu](https://www.geeksforgeeks.org/hamming-code-in-computer-network/)
- Přidává do dat bity pro detekci chyb
- Přidává spolehlivost fyzické vrstvě přidáním mechanismu pro přeposlání poškozených a ztracených rámců
### Ovládá řízení toku dat
- Pokud je rychlost odesílatele rychlejší než příjemce, tak se mohou ztratit některé rámce
- linková vrstva synchronizuje rychlost mezi příjemcem a odesílatelem
### Fragmentace a defragmentace
## Zapouzdření
-> **Rámec (Frame)**
![Pasted image 20240505153242.png](/img/user/Images/Pasted%20image%2020240505153242.png)
## Hardware
- [[Škola/IT/Hardware/L2 switch\|L2 switch]]
- [[Bridge\|Bridge]]