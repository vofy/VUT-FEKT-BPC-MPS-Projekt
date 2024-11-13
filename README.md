# BPC-MPS - Závěrečný projekt

[Celý text práce](https://github.com/vofy/VUT-FEKT-BPC-MPS-Projekt/blob/main/Projekt.pdf)

## Zadání práce
- Získejte z Internetu nebo jiným způsobem model SPICE a katalogový list („datasheet“)
napěťové reference REF-02 firmy Analog Devices.
- Součástku stručně popište – funkce, parametry, výčet možných aplikací.
- S integrovaným obvodem sestavte zdroj symetrického referenčního napětí ±2,5V podle
doporučeného zapojení uvedeného v katalogovém listu. Popište co nejdetailněji funkci
zapojení.
- Změřte závislost obou výstupních napětí naprázdno na vstupním napájecím napětí zdroje.
Z grafu odečtěte dolní hranici napájecího napětí pro správnou funkci reference.
- Změřte závislosti obou výstupních napětí na teplotě v rozsahu od –50 do +125 stupňů
Celsia. Porovnejte s katalogovými údaji.
- Proveďte další experiment dle vlastního uvážení.

## Výsledky práce

### Závislost výstupního napětí naprázdno na vstupním napětí

Na obrázku 1 můžeme vidět závislost výstupního napětí na vstupním napětí reference. Z těchto dat můžeme určit dolní mez napájecího napětí pro správnou funkci reference. Tato mez se nachází při napětí 6,5 V. Z této hodnoty pak můžeme vypočítat dropout napětí U<sub>DO</sub>=U<sub>IN</sub>−U<sub>OUT</sub> = 6,5 − 2,5 = 4,0 V.

![Obrázek 1](https://github.com/user-attachments/assets/20197aaa-bee0-4fe8-a0f0-5dfbee4c0106)

_Obrázek 1: Závislost výstupního napětí naprázdno na vstupním napětí \[4\]_

### Závislost výstupního napětí na teplotě

Z obrázku 2 je patrné, že ačkoliv vlivem teploty dochází ke změně napětí na výstupu, je tato změna minimální. Podle proměřeného intervalu dochází ke změně o 7 ppm/°C v kladné úrovni a v záporné o −8 ppm/°C.

![Obrázek 2](https://github.com/user-attachments/assets/cdf31867-45db-4944-a86c-2960438dfb3f)

_Obrázek 2: Závislost výstupního napětí na teplotě \[4\]_

### Zatěžovací charakteristika napěťové reference

Na obrázek 3 jsou vyneseny zatěžovací charakteristiky napěťové reference. Z obrázku je patrné, že napěťová reference se chová jako tvrdý napěťový zdroj až do proudu 12,65 mA pro kladnou úroveň napětí a 12,70 mA pro zápornou.

![Obrázek 3](https://github.com/user-attachments/assets/9b7e1bc4-ab89-4757-8706-454ff06e2d4d)

_Obrázek 3: Závislost výstupního napětí na teplotě \[4\]_

## Závěr
Při vypracování této úlohy jsme při porovnání odsimulovaných hodnot a charakteristik s těmi v technickém listu zjistili, že modely součástek jsou pouze aproximací těch skutečných.  Například závislost výstupního napětí na teplotě je křivka, která při nižších teplotách stoupá a při vyšších klesá. Ovšem námi odsimulovaná závislost je lineární. Ale i přes skutečnost, že jde pouze o aproximace, jsou simulace cenným nástrojem při návrhu elektronických obvodů. Některé hodnoty z technického listu jsou porovnány s těmi odsimulovanými níže – viz tabulka 1.

### Porovnání hodnot
_Tabulka 1: Porovnání hodnot z technického listu s hodnotami odsimulovanými \[1\]\[4\]_
| Parametr | Symbol | Technický list | Simulace | Jednotka |
| -------- | :----: | :------------: | :------: | :------: |
| Teplotní koeficient | TCV<sub>0</sub> | 3 (typical) – 8,5 (max) | 7–8 | ppm/°C |
| Dropout voltage | V<sub>DO</sub> | 2 | 4 | V |
| Proud zátěží | I<sub>LOAD</sub> | 8–10 | 12,65–12,70 | mA |

## Použité zdroje
- \[1\]: Analog Devices. _Precision 2.5 V, 5.0 V, and 10.0 V Voltage References_ \[elektronický dokument\]. 2016 \[cit. 2.5.2023\]. Dostupný z: https://courses.e-ce.uth.gr/Software/Electronics_II/orcad/model/linear_tech.lib
- \[2\]: Analog Devices. _Library of Analog Devices Opamps, Transistor Arrays, Analog Multipliers, Buffer, Switches, Voltage References_. 20.7.2001 \[přístup 2.5.2023\]. Dostupný z: http://robustdesignconcepts.com/files/pspice/libs/anlg_dev.lib
- \[3\]: Linear Technology Corporation. _Library of Linear Technology op-amps and reference diodes models_. 31.5.1999 \[přístup 2.5.2023\]. Dostupný z: https://raw.githubusercontent.com/jfargentino/kicad/master/linear_tech.lib
- \[4\]: Analog Devices. _LTspice XVII_. 27.4.2023 \[přístup 2.5.2023\]. Dostupný z: https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html
