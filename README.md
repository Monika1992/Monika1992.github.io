# Zadání seminární práce
Cílem seminární práce je osvojit si základy práce s klimatologickými časovými řadami. V rámci práce budou využita volně dostupná pozorovaná data [Českého hydrometeorologického ústavu (ČHMÚ)](https://www.chmi.cz/). Data jsou k dispozici v denním či měsíčním časovém kroku a pro minulost jsou volně ke stažení.

Kromě práce s pozorovanými daty se rovněž seznámíme s klimatickými scénáři připravenými [Ústavem výzkumu globální změny AV ČR, v. v. i. (CzechGlobe)](https://www.czechglobe.cz/cs/) dostupnými na portálu [ClimRisk](https://www.climrisk.cz/) a evropského programu [Copernicus](https://www.copernicus.eu/en).

<details markdown="1">
<summary> Základní informace o kurzu </summary>

# Základní informace
- Můj kontaktní email je monika.hlavsova@mendelu.cz, najdete mě v kanceláři N5064 po předchozí domluvě
- Kontakt pro seminární práci z fenologie je Ing. Petra Dížková (dizkova.p@czechglobe.cz)
- Na každé cvičení potřebuju notebook, MS Excel s dokončenou prací z minulého cvičení

## Jak dostanu zápočet
- Splním 3 úkoly:
  - Seminární práce z fenologie (MUSÍM SE REGISTROVAT [TADY](http://www.fenofaze.cz/extranet/cs/sign/up-student/))
  - Seminární práce z klimatologie
  - Docházka (max 2 absence)   

## Co potřebuji pro práci ve cvičení
- Wi-Fi - ideálně EDUROAM ([ZDE najdu jak se připojit](https://eduroam.mendelu.cz/25350-navody-k-instalaci))
- MS Excel ([ZDE najdu jak ho získám](https://tech.mendelu.cz/25346-instalace-baliku-microsoft))

## Co mám dělat když něco nevím nebo nestíhám?
  - Ptám se na cvičení
  - Ptám se spolužáků
  - Ptám se Googlu nebo AI

</details>

<details markdown="1">
<summary> Cvičení 02 </summary>

# Cvičení 02 (02.10.2025) - Zadání seminární práce z klimatologie, získání dat

- Cílem cvičení je vybrat si stanici se kterou budu v rámci semestru pracovat a získat výchozí data pro další práci
- __Na konci cvičení mám MS Excel soubor s měsíčními daty pro průměrné teploty vzduchu a sumy srážek pro mojí vybranou stanici__

## DŮLEŽITÉ ODKAZY ##
- Mapa stanic Českého hydrometeorologického ústavu: [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
- Metadatový soubor pro vyhledání identifikátoru stanic: [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
- Datový repozitář ČHMÚ: [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)

## Postup získání dat ##

1. Pro práci ve cvičení a na seminární práci vytvořím nový MS Excel soubor, který pojmenuju jako __PrijmeniJmeno_AgroMeteo.xlsx__ (uložím si ho, vím kde je, budu ho potřebovat každé cvičení)

2. Na mapě stanic vyberu stanici [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
     - 2.1 V legendě vyberu stanice podle legendy (zakliknu T a SRA a hledám stanici kde se obě veličiny sledují)
     - 2.2 Každý student ve skupině si vybere jinou stanici
     - 2.3 Zapamatuji (opíšu si) z mapy ID stanice (např. B2KUCH01) a jméno
     - 2.4 nevybírám si následující stanice (nedostatečná data)
          - _Žamberk_, _Třebařov_, _Ústí nad Orlicí_, _Jičín_, _Libice nad Doubravou_ 

3. Stáhnu si z odkazu soubor s metadaty o stanicích [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
     - 3.1 Otevřu metadatový soubor v MS Excel
     - 3.2 Vyhledám svoji vybranou stanici pomocí jména či ID stanice
     - 3.3 Ověřím že stanice měří kontinuálně od roku 1961, pokud ne, raději zvolím jinou
     - 3.4 Poznačím si interní kód stanice (sloupec A "WSI")
     - 3.5 Poznačím si souřadnice stanice (sloupce F "GEOGR1" a G "GEOGR2") a nadmořskou výšku (sloupec H "ELEVATION")

4. Vrátím se na stránky datového repozitáře [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)
     - 4.1 Volím složku __monthly__
     - 4.2 Budeme pracovat se dvěma složkami - __temperature__ a __precipitation__ (postup bude stejný, začneme teplotou)
     - 4.3 Nyní využiji svůj interní kód stanice (_viz. bod 3.4_) a pomocí něj vyhledám příslušné soubory (__CTRL+F__)
     - 4.4 Zajímá nás pouze soubor označený "T" (Nezajímá nás: TMA, TMI, TMInoc, TPM) a ten stáhneme
     - 4.5 Zopakuji postup získání dat pro srážky
   
5. Příprava vstupních dat
     - 5.1 Otevřu stažený CSV soubor v MS Excel 
     - 5.2 Rozdělíme data do sloupců (POZOR NA HODNOTY! - Podívám se do sloupce "VALUE" jestli tam nevidím žádné římské číslice - Excel možná bude převádět vaše čísla na datumy, pokud jo, zavřu soubor a nejdříve upravím data dle bodu "Úprava dat" na konci zadání)
     - 5.3 U teploty nezapomenu vyfiltrovat pouze průměrné hodnoty ("AVG" - sloupce E a F): výsledkem jsou měsíční hodnoty průměrné teploty vzduchu ve všech letech dostupných pro moji stanici
     - 5.4 Data ze sloupců C ("YEAR"), D ("MONTH") a G ("VALUE") zkopíruji do připraveného Excelu (viz __Krok 1__) na první list
     - 5.5 Sloupec "VALUE" přejmenuji na TAVG
     - 5.6 Zopakuji postup pro srážky (hodnota "SUM" ze sloupce F "MDFUNCTION")

6. Bonus
     - 6.1 Z dat srážek a průměrných denních teplot si vytvořím jednoduchý spojnicový graf a podívám se na průběh hodnot v čase

Úprava dat (návod pro Windows):
- 1: najdu si pomocí průzkumníku souborů stažená data ve formátu csv
- 2: Pravým tlačítkem myši otevřu na souboru kontextovou nabídku a zvolím "Otevřít v aplikaci poznámkový blok"
- 3: Data se otevřou v poznámkovém bloku
- 4: Zmáčknu současně klávesy __CTRL__ a __H__ a otevře si mi nabídka "Najít a nahradit"
- 5: Nejdříve nahradím všechny symboly čárky (,) za symboly středník (;) a dám "Nahradit vše" (Všechny čárky v souboru by měly nyní být změněny na středníky
- 6: Pak opakuji postup a nahradím všechny symboly tečky (.) za symboly čárky (,)
- 7: Uložím soubor (klávesová zkratka __CTRL__ a __S__) a otevřu ho  aplikaci MS Excel - nyní by už mělo být vše v pořádku a pokračuju filtrováním dat (bod 5.3)

## Další zdroje:
  - (OS Windows) Klávesové zkratky a mapa znaků pro českou klávesnici: [ZDE](http://www.ceskaklavesnice.cz/zkratky) 
</details>

<details markdown="1">
<summary> Cvičení 03 </summary>
# Cvičení 03 (09.10.2025) - Radiace a teplota
- Cílem cvičení je vysvětlit si základní terminologii k tématu solární radiace, pochopení vztahu radiace a teploty vzduchu a otestovat si možnosti získání dat z jiných zdrojů než je ČHMÚ
- __Na konci cvičení mám MS Excel soubor s novým listem kde srovnáme měsíční hodnoty solární radiace a teplot pro naši vybranou stanici__
  
## DŮLEŽITÉ ODKAZY ##
- Data pro radiaci: [Data k získání ZDE](https://ads.atmosphere.copernicus.eu/datasets/cams-solar-radiation-timeseries?tab=overview)

## Postup práce ve cvičení ##

1. Ve svém MS Excel souboru __PrijmeniJmeno_AgroMeteo.xlsx__ vytvořím nový list a pojmenuji ho TeplotaRadiace
 - 1.1 Do prvních 3 sloupců na novém listu nakopíruji data ze sloupců obsahujících __rok, měsíc a hodnoty teploty vzduchu__ z listu s daty pro teplotu
 - 1.2 Nechám si pouze hodnoty pro rok 2004-2024 a zbytek mohu z tohoto listu smazat (__pozor, nesmažte si hodnoty z originálních dat teploty, které máte na listu _Teplota___)

2. Získám data pro solární radiaci ze služby Copernicus
 - 2.1 Na stránkách Copernicus [Data k získání ZDE](https://ads.atmosphere.copernicus.eu/datasets/cams-solar-radiation-timeseries?tab=overview) vyberu záložku __Download__ (MUSÍM SE REGISTROVAT)
 - 2.2 Vyplním formulář pro získání dat s pomocí následující nápovědy
 - 2.3 U výběru __Sky type__ volím __Both cloud-free and actual weather conditions__
 - 2.4 Zadám souřadnice mojí stanice (pokud jsem si minule neopsal souřadnice, najdu si je pomocí mapy.cz). Na mapě mohu zkontrolovat že jsem souřadnice zadal správně a poloha puntíku cca odpovídá poloze mojí stanice
 - 2.5 Zadám nadmořskou výšku mojí stanice
 - 2.6 Jako rozpětí datumů zvolím __2004-01-01 až 2024-12-31__
 - 2.7 U výběru __Time step__ volím __1 month__
 - 2.8 U výběru __Time reference__ volím __True solar time__
 - 2.9 U výběru __Data format__ volím __CSV__
 - 2.10 Potvrdím potřebné souhlasy a požádám o data - budeme pár minut čekat než se pro nás data vygenerují a pak si je stáhneme

3. Práce se staženými daty solární radiace
 - 3.1 Stažený soubor otevřeme v programu MS EXCEL, pomocí kombinace kláves __CTRL__ a __H__ (nebo nástroje __Najít a nahradit__) najdeme čárky a nahradíme je středníky (;), dále nahradíme tečky za čárky
 - 3.2 Použijeme trik s rozdělením dat do sloupců (Vyberu sloupec _A_ a na kartě _Data_ zvolím _Text do sloupců_), kde máme středník jako oddělovač
 - 3.3 Prozkoumáme hlavičky souboru a co v nich vše můžeme vidět za informace
 - 3.4 Pro další postup budeme pracovat s hodnotami __Globální radiace__ označená jako __GHI__
 - 3.5 Vybereme hodnoty ze sloupce __GHI__ a __Observation period__ a nakopírujeme je na náš připravený list TeplotaRadiace v MS Excel (Zkontroluji jestli maají data stejný začátek a konec v čase a případně to upravím tak, aby měla)

4. Porovnání dat měsíčních teplot a sum globální radiace
 - 4.1 Pro snadné vizuální porovnání hodnot vytvoříme spojnicový graf průběhu obou veličin v čase, na kterém si zároveň vyzkoušíme tvorbu kompletního grafu se všemi náležitostmi  
 - 4.2 Na listu TeplotaRadiace vybereme data pro měsíční teploty a globální radiaci
 - 4.3 Vložíme spojnicový graf (Karta __Vložit__)
 - 4.4 Rozdělíme naše dvě veličiny na dvě osy - pomocí kontextové nabídky grafu vyberu __Změnit type grafu__ a vyberu z nabídky __Kombinovaný__
 - 4.5 Obě veličiny chceme zobrazit jako spojnicový graf, na sekundární osu přesuneme globální radiaci
 - 4.6 Kompletní graf je čitelný a obsahuje minimálně: Název, Legendu, Popisky os včetně jednotek, Uvedený zdroj/zdroje dat
</details>
  
<details markdown="1">
<summary> Cvičení 04 </summary>
# Cvičení 04 (16.10.2025) - Energetická bilance
</details>
  
<details markdown="1"> 
<summary> Cvičení 05 </summary>
# Cvičení 05 (23.10.2025) - Změna klimatu
</details>
  
<details markdown="1">
<summary> Cvičení 06 </summary>
# Cvičení 06 (30.10.2025) - Teplota vzduchu
</details>
  
<details markdown="1">
<summary> Cvičení 07 </summary>
# Cvičení 07 (06.11.2025) - Charakteristické dny
</details>
  
<details markdown="1">
<summary> Cvičení 08 </summary>
# Cvičení 08 (13.11.2025) - Vlhkost vzduchu a výpar
</details>
  
<details markdown="1">
<summary> Cvičení 09 </summary>
# Cvičení 09 (20.11.2025) - Srážky
</details>
  
<details markdown="1">
<summary> Cvičení 10 </summary>
# Cvičení 10 (27.11.2025) - Sucho
</details>
  
<details markdown="1">
<summary> Cvičení 11 </summary>
# Cvičení 11 (04.12.2025) - Tlak a vítr
</details>
  
<details markdown="1">
<summary> Cvičení 12 </summary>
# Cvičení 12 (11.12.2025) - Kontrola seminárních prací a zápočty
</details>


