---
{"dg-publish":true,"permalink":"/Škola/IT/Maturitní otázky/Programování/Softwarová a hardwarová výbava robota/","tags":["Maturitní_otázka","IT","Programování","Robotika"],"created":"2023-12-19T09:11:28.580+01:00","updated":"2024-05-06T09:16:59.528+02:00"}
---

## Definice robota
- definice plně automatická linka
	- mnoho robotů, kteří pracují spolu na jednom výrobku
## Typy robotů
## Důležité definice
- **Threshold** - Prahová hodnota, zvyšujeme rychlost robota tak, aby fungoval dostatečně rychle a nevyráběl až moc vadných kusů
## Hardware robota
- základní deska a přídavné řídící desky
- 
### Pohony
- Bezpečnostní prvky
- v praxi se používají kombinace
	- Např. pneumatický a elektrický, elektrický a hydraulický
#### Elektrický
- malý robot
- převážně robotické ruce
- robot nemá takovou sílu
#### Pneumatický
- ovládání pomocí vzduchu
- vzduch je hodně stlačitelný -> horší odezva od robota 
- robot nemá takovou sílu
#### Hydraulický
- jako pohon je použit speciální hydraulický olej
- kapaliny jsou těžko stlačitelné -> dobrá odezva
- tlak v kapalině se rychle šíří
### Servo motor

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



- zná pozici svého natočení
- lze nastavit o kolik stupňů se otočí a kam
- lze nastavit rychlost otočení

</div></div>

### Vakuová pumpa
### Čidlo
- je to snímací zařízení, které je schopné ovládat další prvky
- Nejobecnější termín pro zařízení, které reaguje na fyzikální veličinu
### Detektor
- je to zařízení, které hlídá přítomnost určitého jevu
- Např. detektor tlaku, 
### Senzor
- Přeměňuje fyzikální veličiny na elektrický signál
- Např. senzor tlaku
### Snímač
- převádí světlo na elektrický signál
- hodně podobné senzoru, ale nefunguje stejně
### Hlídač 
- světelné brány
- hlídají vstup k robotu, nebo hlídají závady
- klidový stav
- Např. světýlko, které svítí, když se zavírá brána
### Hlásič
- kontroluje nějaký stav, pokud ho najde tak hlásí
- Např. hlásič požáru, 
## Software Robota
- roboti mají svůj [[Firmware\|Firmware]]
- K programování robota potřebujeme:
	- robota
	- počítač
	- Software - IDE
### Způsoby programování
#### Psaní kódu
- psaní programu v IDE
- často se používá [[Škola/IT/Programování/Programovací jazyky/Python\|Python]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/skola/it/maturitni-otazky/programovani/zakladni-pojmy-v-oblasti-robotiky/#programovani-robotu-a-io-t" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



# Programování robotů a IoT
- existuje neskutečně moc jazyků, které se dají použít pro naprogramování robota, mezi nejpoužívanější se řadí
	- [[Škola/IT/Programování/Programovací jazyky/Python\|Python]] 
		- Je vhodný pro širokou škálu IoT projektů, od jednoduchých senzorových aplikací až po komplexní systémy
		- Je velmi lehký se naučit
	- [[Škola/IT/Programování/Programovací jazyky/Java\|Java]]
		- Je vhodný pro IoT projekty, které vyžadují vysokou úroveň zabezpečení a spolehlivosti
	- [[Škola/IT/Programování/Programovací jazyky/C\|C]]/[[Škola/IT/Programování/Programovací jazyky/C++\|C++]]
		- Jsou vhodné pro IoT projekty, které vyžadují vysokou rychlost a výkon

</div></div>

#### Pomocí souřadnic
- vezmeme robotickou ruku a natáhneme ji na určité místo, ruka si poté uloží souřadnice
#### Pomocí bloků
- Na způsob scratche
