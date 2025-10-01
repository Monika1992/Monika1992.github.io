# Zadání seminární práce
Cílem seminární práce je osvojit si základy práce s klimatologickými časovými řadami. V rámci práce budou využita volně dostupná pozorovaná data Českého hydrometeorologického ústavu (ČHMÚ). Data jsou k dispozici v denním či měsíčním časovém kroku.

Kromě práce s pozorovanými daty se rovněž seznámíme s klimatickými scénáři připravenými Ústavem výzkumu globální změny AV ČR, v. v. i. (CzechGlobe). Data budoucích klimatických podmínek jsou k dispozici zde.

# Základní informace
- Můj kontaktní email je hlavsova.m@czechglobe.cz, najdete mě v kanceláři N5064 po předchozí domluvě
- Kontakt pro seminární práci z fenologie je Ing. Petra Dížková
- Na každé cvičení potřebuju notebook, MS Excel s dokončenou prací z minulého cvičení

## Jak dostanu zápočet
- Splním 3 úkoly:
  - Seminární práce z fenologie
  - Seminární práce z klimatologie
  - Docházka (max 2 absence)   

## Co potřebuji pro práci ve cvičení
- WI-FI - ideálně EDUROAM ([ZDE najdu jak se připojit](https://eduroam.mendelu.cz/25350-navody-k-instalaci))
- MS Excel ([ZDE najdu jak ho získám](https://tech.mendelu.cz/25346-instalace-baliku-microsoft))

## Co mám dělat když něco nevím nebo nestíhám?
  - Ptám se na cvičení
  - Ptám se spolužáků
  - Ptám se Googlu nebo AI

---

# Cvičení 02 (02.10.2025) - Zadání seminární práce z klimatologie, získání dat

- Cílem cvičení je vybrat si stanici se kterou budu v rámci semestru pracovat a získat výchozí data pro další práci
- __Na konci cvičení mám MS Excel soubor s měsíčními daty pro průměrné teploty vzduchu a sumy srážek pro mojí vybranou stanici__

## DŮLEŽITÉ ODKAZY ##
- Mapa stanic Českého hydrometeorologického úřadu: [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
- Metadatový soubor pro vyhledání identifikátoru stanic: [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
- Datový repozitář ČHMÚ: [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)

## Postup získání dat ##

0. Pro práci ve cvičení a na seminární práci vytvořím nový MS Excel soubor, který pojmenuju jako __PrijmeniJmeno_AgroMeteo.xlsx__ (uložím si ho, vím kde je, budu ho potřebovat každé cvičení)

1. Na mapě stanic vyberu stanici [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
  1.1 V legendě vyberu stanice podle legendy (zakliknu T a SRA a hledám stanici kde se obě veličiny sledují)
  1.2 Každý student ve skupině si vybere jinou stanici
  1.3 Zapamatuji (opíšu si) z mapy ID stanice (např. B2KUCH01) a jméno

2. Stáhnu si z odkazu soubor s metadaty o stanicích ([Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
  2.1 Otevřu metadatový soubor v MS Excel
  2.2 Vyhledám svoji vybranou stanici pomocí jména či ID stanice
  2.3 Ověřím že stanice měří kontinuálně od roku 1961, pokud ne, raději zvolím jinou
  2.4 Poznačím si interní kód stanice (sloupec A "WSI")
  2.5 Poznačím si souřadnice stanice (sloupce F "GEOGR1" a G "GEOGR2") a nadmořskou výšku (sloupec H "ELEVATION")

3. Vrátím se na stránky datového repozitáře [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)
  3.1 Volím složku monthly
  3.2 Budeme pracovat se dvěma složkami - __temperature__ a __precipitation__ (postup bude stejný, začneme teplotou)
  3.3 Nyní využiji svůj interní kód stanice (_viz. bod 2.4_) a pomocí něj vyhledám příslušné soubory (__CTRL+F__)
  3.4 Zajímá nás pouze soubor označený "T" (Nezajímá: TMA, TMI, TMInoc, TPM) a ten stáhneme
  3.5 Zopakuji postup získání dat pro srážky
   
4. Příprava vstupních dat
  4.1 Otevřu stažený CSV soubor v MS Excel
  4.2 Rozdělíme data do sloupců
  4.3 U teploty nezapomenu vyfiltrovat pouze průměrné hodnoty ("AVG" - sloupce E a F): výsledkem jsou měsíční hodnoty průměrné teploty vzduchu ve všech letech dostupných pro moji stanici
  4.4 Data ze sloupců C ("YEAR"), D ("MONTH") a G ("VALUE") zkopíruji do připraveného Excelu (viz krok 0) na první list
  4.5 Sloupec "VALUE" přejmenuji na TAVG
  4.6 Zopakuji postup pro srážky (hodnota "SUM" ze sloupce F "MDFUNCTION")

## Další zdroje:
  - (OS Windows) Klávesové zkratky a mapa znaků pro českou klávesnici: [ZDE](http://www.ceskaklavesnice.cz/zkratky) 

---

# Cvičení 03 (09.10.2025) - Radiační bilance

# Cvičení 04 (16.10.2025) - Energetická bilance

# Cvičení 05 (23.10.2025) - Změna klimatu

# Cvičení 06 (30.10.2025) - Teplota vzduchu

# Cvičení 07 (06.11.2025) - Charakteristické dny

# Cvičení 08 (13.11.2025) - Vlhkost vzduchu a výpar

# Cvičení 09 (20.11.2025) - Srážky

# Cvičení 10 (27.11.2025) - Sucho

# Cvičení 11 (04.12.2025) - Tlak a vítr

# Cvičení 12 (11.12.2025) - Kontrola seminárních prací a zápočty


