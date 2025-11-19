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
     - 1.1 První list tohoto Excelu pojmenuji __Metadata__ a postupně sem doplním základní informace o stanici, kterou si vyberu (název, ID stanice, souřadnice, nadmořská výška)

3. Na mapě stanic vyberu stanici [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
     - 2.1 V legendě vyberu stanice podle legendy (zakliknu T a SRA a hledám stanici kde se obě veličiny sledují)
     - 2.2 Každý student ve skupině si vybere jinou stanici
     - 2.3 Zapamatuji (opíšu si) z mapy ID stanice (např. B2KUCH01) a jméno
     - 2.4 nevybírám si následující stanice (nedostatečná data)
          - _Žamberk_, _Třebařov_, _Ústí nad Orlicí_, _Jičín_, _Libice nad Doubravou_ 

4. Stáhnu si z odkazu soubor s metadaty o stanicích [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
     - 3.1 Otevřu metadatový soubor v MS Excel
     - 3.2 Vyhledám svoji vybranou stanici pomocí jména či ID stanice
     - 3.3 Ověřím že stanice měří kontinuálně od roku 1961, pokud ne, raději zvolím jinou
     - 3.4 Poznačím si interní kód stanice (sloupec A "WSI")
     - 3.5 Poznačím si souřadnice stanice (sloupce F "GEOGR1" a G "GEOGR2") a nadmořskou výšku (sloupec H "ELEVATION")

5. Vrátím se na stránky datového repozitáře [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)
     - 4.1 Volím složku __monthly__
     - 4.2 Budeme pracovat se dvěma složkami - __temperature__ a __precipitation__ (postup bude stejný, začneme teplotou)
     - 4.3 Nyní využiji svůj interní kód stanice (_viz. bod 3.4_) a pomocí něj vyhledám příslušné soubory (__CTRL+F__)
     - 4.4 Zajímá nás pouze soubor označený "T" (Nezajímá nás: TMA, TMI, TMInoc, TPM) a ten stáhneme
     - 4.5 Zopakuji postup získání dat pro srážky
   
6. Příprava vstupních dat
     - 5.1 Otevřu stažený CSV soubor v MS Excel 
     - 5.2 Rozdělíme data do sloupců (POZOR NA HODNOTY! - Podívám se do sloupce "VALUE" jestli tam nevidím žádné římské číslice - Excel možná bude převádět vaše čísla na datumy, pokud jo, zavřu soubor a nejdříve upravím data dle bodu "Úprava dat" na konci zadání)
     - 5.3 U teploty nezapomenu vyfiltrovat pouze průměrné hodnoty ("AVG" - sloupce E a F): výsledkem jsou měsíční hodnoty průměrné teploty vzduchu ve všech letech dostupných pro moji stanici
     - 5.4 Data ze sloupců C ("YEAR"), D ("MONTH") a G ("VALUE") zkopíruji do připraveného Excelu (viz __Krok 1__) na první list
     - 5.5 Sloupec "VALUE" přejmenuji na TAVG
     - 5.6 Zopakuji postup pro srážky (hodnota "SUM" ze sloupce F "MDFUNCTION")

7. Bonus
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

# Cvičení 04 (16.10.2025) - Srovnání průměrných měsíčních teplot za dvě normálová období
- Cílem cvičení je vytvořit grafy průměrných měsíčních teplot pro dva třicetileté klimatické normály a porovnat hodnoty v těchto obdobích
- __Na konci cvičení mám MS Excel soubor s novým listem NormalyTeploty, kde srovnáme data průměrných teplot vzduchu v jednotlivých měsících v rámci dvou klimatických normálů 1961-1990 and 1991-2020, včetně grafického zobrazení__

## Postup práce ve cvičení ##
1. Ve svém MS Excel souboru __PrijmeniJmeno_AgroMeteo.xlsx__ vytvořím nový list a pojmenuji ho __NormalyTeploty__
   
2. Příprava dat a vytvoření kontingenční tabulky - teplota vzduchu
     - 2.1 Na nový list __NormalyTeploty__ nakopíruji data z listu __Teplota__, vyberu pouze časové úseky 1961-1990 a 1991 až 2020. Hodnoty pro první normál (rok, měsíc, teploty) nakopíruju od sloupce __A__, hodnoty pro druhý normál (rok, měsíc, teploty) od sloupce __E__
     - 2.2 Pokud mi chybí záhlaví (pojmenování sloupců) tak ho u obou normálů doplním
     - 2.3 Nyní vložíme tzv. kontingenční graf a kontingenční tabulku. Na záložce __Vložit__ vybereme __Kontingenční graf__ a následně možnost __Kontingenční graf a kontingenční tabulka__ (Na MacOS stačí jen __Kontingenční graf__ a pak už rovnou zadávám oblast dat)
     - 2.3 V nabídce __Vybrat tabulku nebo oblast__ vybereme sloupce __A, B, C (data normálu 1961-1990)__ a potvrdíme výběr
     - 2.4 Měla by se objevit plátna pro kontingenční tabulku a kontingenční graf (zatím prázdná)
     - 2.5 V nabídce __Pole kontingenčního grafu__ přeneseme (drag and drop) položku __Měsíc__ (nebo odpovídající název vašeho sloupce s označením měsíce) do boxu __Osa kategorie__
     - 2.6 Stejným způsobem přeneseme položku __Teplota__ do boxu __Hodnoty__
     - 2.7 U boxu __Hodnoty__ změníme v nabídce __Nastavení polí hodnot...__ funkci na __Průměr__ a potvrdíme
     - 2.8 Prohlédnu si vygenerovaný graf a vizuálně zhodnotím jestli dává smysl (např. jaké hodnoty jsou na osách X, Y, jestli vidím předpokládaný roční průběh teploty v jednotlivých měsících atd.). Pokud je vše OK, samotný graf můžu smazat.
     - 2.9 hodnoty z vygenerované kontingenční tabulky vyberu a pomocí __Vložit hodnoty__ je nakopíruju na volné místo na listu (doporučuju sloupec __I__). Původní kontingenční tabulku smažu
     - 2.10 Postup tvorby kontingenční tabulky zopakujeme pro druhé normálové období

3. Vytvoření jednoho spojnicového grafu pro porovnání obou normálových období
     - 3.1 Po vytvoření obou kontingenčních tabulek pro období 1961-1990 a 1991-2020 budeme zobrazovat obě řady měsíčních průměrných teplot v jednom spojnicovém grafu
     - 3.2 Vybereme vstupní data a pomocí __Vložit__, __Spojnicový graf__ vložíme graf který dále upravíme do podoby kompletního grafu
     - Přidáme název, popisy os, zdroj vstupních dat, jednotky, upravíme legendu tak aby byla čitelná

## Otázky k interpretaci dat ##
1. Jaké pozorujete rozdíly a změny mezi dvěma srovnávanými obdobími
2. Které měsíce se oteplují nejvíce a které nejméně?
3. Jaké mohou tyto změny mít dopady v krajině v jednotlivých ročních obdobích?
4. Jak se liší roční teploty ve dvou srovnávaných obdobích
</details>
  
<details markdown="1"> 
<summary> Cvičení 05 </summary>

# Cvičení 05 (23.10.2025) - Změna klimatu - získání dat budoucího vývoje klimatu z portálu ClimRisk, teplotní gradient
- Cílem cvičení je prověřit předpokládaný budoucí vývoj klimatu pro naši stanici a jejich srovnání s daty získanými z historických měření ČHMÚ
- __Na konci cvičení mám MS Excel soubor s novými listy KlimatickyGradient a BudouciKlima kde srovnáme průměrné měsíční hodnoty normálových období 1961-1990 a 1991-2020 se získanými daty budoucího vývoje klimatu__
  
## DŮLEŽITÉ ODKAZY ##
- Tabulky podnebí: [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf)
- Data budoucího vývoje klimatu: [Dostupná na portálu ClimRisk](https://www.climrisk.cz/)

## Postup práce ve cvičení ##
1. Příprava pracovního Excelu
     - 1.0 Vytvořím si dva nové listy a pojmenuji je __KlimatickyGradient__ a __BudouciKlima__

2. Popsání klimatického teplotního gradientu s pomocí Tabulek podnebí
     - 2.0 Otevřu si Tabulky podnebí buď [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf) nebo si vezmu papírovou kopii
     - 2.1 Pomocí mapy vyberu 10 stanic s rozdílnými nadmořskými výškami
     - 2.2 Opíšu si jména stanic a nadmořské výšky z __Abecedního seznamu klimatických stanic__
     - 2.3 Opíšu průměrné roční teploty (__Tabulka 1: Průměrná teplota vzduchu (°C) za období 1901-1950__)
     - 2.4 V MS Excel vytvořím bodový graf z dat teploty a nadmořské výšky
     - 2.5 Zobrazím spojnici trendu včetně funkce a s pomocí zobrazené funkce ověřím míru teplotního gradientu u mojí stanice
     - 2.6 U grafu doplním veškeré náležitosti (Název, popisky os včetně jednotek, úplnou legendu, zdroj dat)
  
3. Získání ročních dat pro všechny časové agregace z portálu ClimRisk
     - 3.1 Otevřu portál [ClimRisk](https://www.climrisk.cz/)
     - 3.2 Vyberu __Česká Republika__
     - 3.3 V pravém menu vybereme jako parametr možnost __Průměrná teplota vzduchu__
     - 3.4 V horním menu stránky vyberu položku __Stahování dat__ a vyplníme formulář pro stažení hodnot
     - 3.5 Oblast: Česká republika, Podoblast: Okres ve kterém se nachází moje stanice, Region: Katastrální území mojí stanice (většinou stejné jako název obce)
     - 3.6 V nabídce Agregace vyberte pouze rok
     - 3.7 V nabídce Klimatická projekce vyberte __všechny dostupná období__
     - 3.8 V nabídce Scénář vyberte některou z možností __SSP126, SSP245, SSP370 nebo SSP585__
     - 3.9 V nabídce Klimatická charakteristika vyberte __Průměrná teplota vzduchu__ a  __Srážkový úhrn__
     - 3.10 V nabídce email zadejte vaši mailovou adresu a nechte si zaslat data
  
4. Práce se staženými daty a tvorba grafů
     - 4.1 Pro roční hodnoty časových agregací scénářů budoucího vývoje klimatu vytvořím spojnicový graf průběhu včetně mediánu a všech percentilů
  
5. Bonus: Získání měsíčních dat z portálu ClimRisk
     - 5.1 Otevřu portál [ClimRisk](https://www.climrisk.cz/)
     - 5.2 Vyberu __Česká Republika__
     - 5.3 V pravém menu vybereme jako parametr možnost __Průměrná teplota vzduchu__
     - 5.4 V horním menu stránky vyberu položku __Stahování dat__ a vyplníme formulář pro stažení hodnot
     - 5.5 Oblast: Česká republika, Podoblast: Okres ve kterém se nachází moje stanice, Region: Katastrální území mojí stanice (většinou stejné jako název obce)
     - 5.6 V nabídce Agregace vyberte všechny měsíce (leden-prosinec) a také rok
     - 5.7 V nabídce Klimatická projekce vyberte období __2035 (2021-2050)__ a __2065 (2051-2080)__
     - 5.8 V nabídce Scénář vyberte některou z možností __SSP126, SSP245, SSP370 nebo SSP585__
     - 5.9 V nabídce Klimatická charakteristika vyberte __Průměrná teplota vzduchu__ a  __Srážkový úhrn__
     - 5.10 V nabídce email zadejte vaši mailovou adresu a nechte si zaslat data
     - 5.11 Do grafu průměrných měsíčních teplot ve dvou normálových obdobích z minulého cvičení přidám data z budoucích normálových období 2035 (2021-2050)__ a __2065 (2051-2080)

</details>
  
<details markdown="1">
<summary> Cvičení 06 </summary>

# Cvičení 06 (30.10.2025) - Dotazy k seminární práci z fenologie, ukončení fenologických pozorování, doplnění k předcházejícím cvičením
- Cílem cvičení je kontrola fenologického pozorování, dořešení nejasností, případné odevzdání hotové práce
- __Na konci cvičení je mi jasné co musím udělat pro to abych získal/a zápočet za fenologickou seminárku a vím jakým způsobem postupovat u nedokončených pozorování__
</details>
  
<details markdown="1">
<summary> Cvičení 07 </summary>

# Cvičení 07 (06.11.2025) - Srážky, vlhkost vzduchu a výpar

- Cílem cvičení je prověřit předpokládaný budoucí vývoj klimatu pro naši stanici a jejich srovnání s daty získanými z historických měření ČHMÚ
- __Na konci cvičení mám MS Excel soubor s novými listy NormalySrazky a DnySnih3cm, kde srovnáme data srážkových úhrnů v jednotlivých měsících v rámci dvou klimatických normálů 1961-1990 and 1991-2020, včetně grafického zobrazení a počet dní se sněhovou pokrývkou nad 3 cm v současném a budoucím klimatu__

## DŮLEŽITÉ ODKAZY ##
- Data budoucího vývoje klimatu: [Dostupná na portálu ClimRisk](https://www.climrisk.cz/)

## Postup práce ve cvičení ##
1. Ve svém MS Excel souboru __PrijmeniJmeno_AgroMeteo.xlsx__ vytvořím dva nové listy a pojmenuji je __NormalySrazky__ a __DnySnih3cm__

2. Příprava dat a vytvoření kontingenční tabulky - srážky
     - 2.1 Na nový list __NormalySrazky__ nakopíruji data z listu __Srazky__, vyberu pouze časové úseky 1961-1990 a 1991 až 2020. Hodnoty pro první normál (rok, měsíc, teploty) nakopíruju od sloupce __A__, hodnoty pro druhý normál (rok, měsíc, teploty) od sloupce __E__
     - 2.2 Pokud mi chybí záhlaví (pojmenování sloupců) tak ho u obou normálů doplním (__ROK, MĚSÍC, SUMA SRÁŽEK__)
     - 2.3 Nyní vložíme tzv. kontingenční graf a kontingenční tabulku. Na záložce __Vložit__ vybereme __Kontingenční graf__ a následně možnost __Kontingenční graf a kontingenční tabulka__ (Na MacOS stačí jen __Kontingenční graf__ a pak už rovnou zadávám oblast dat)
     - 2.3 V nabídce __Vybrat tabulku nebo oblast__ vybereme sloupce __A, B, C (data normálu 1961-1990)__ a potvrdíme výběr
     - 2.4 Měla by se objevit plátna pro kontingenční tabulku a kontingenční graf (zatím prázdná)
     - 2.5 V nabídce __Pole kontingenčního grafu__ přeneseme (drag and drop) položku __Měsíc__ (nebo odpovídající název vašeho sloupce s označením měsíce) do boxu __Osa kategorie__
     - 2.6 Stejným způsobem přeneseme položku __Teplota__ do boxu __Hodnoty__
     - 2.7 U boxu __Hodnoty__ změníme v nabídce __Nastavení polí hodnot...__ funkci na __Průměr__ a potvrdíme
     - 2.8 Prohlédnu si vygenerovaný graf a vizuálně zhodnotím jestli dává smysl (např. jaké hodnoty jsou na osách X, Y, jestli vidím předpokládaný roční průběh teploty v jednotlivých měsících atd.). Pokud je vše OK, samotný graf můžu smazat.
     - 2.9 hodnoty z vygenerované kontingenční tabulky vyberu a pomocí __Vložit hodnoty__ je nakopíruju na volné místo na listu (doporučuju sloupec __I__). Původní kontingenční tabulku smažu
     - 2.10 Postup tvorby kontingenční tabulky zopakujeme pro druhé normálové období

3. Vytvoření jednoho spojnicového grafu pro porovnání obou normálových období
     - 3.1 Po vytvoření obou kontingenčních tabulek pro období 1961-1990 a 1991-2020 budeme zobrazovat obě řady měsíčních sum srážek v jednom sloupcovém grafu
     - 3.2 Vybereme vstupní data a pomocí __Vložit__, __Sloupcový graf__ vložíme graf který dále upravíme do podoby kompletního grafu
     - Přidáme název, popisy os, zdroj vstupních dat, jednotky, upravíme legendu tak aby byla čitelná
  
4. Stažení dat pro sněhovou pokrývku nad 3 cm z portálu ClimRisk
     - 4.1 Otevřu portál [ClimRisk](https://www.climrisk.cz/)
     - 4.2 Vyberu __Česká Republika__
     - 4.3 V horním menu stránky vyberu položku __Stahování dat__ a vyplníme formulář pro stažení hodnot
     - 4.4 Oblast: Česká republika, Podoblast: Okres ve kterém se nachází moje stanice, Region: Katastrální území mojí stanice (většinou stejné jako název obce)
     - 4.5 V nabídce Agregace vyberte všechny měsíce leden-prosinec
     - 4.6 V nabídce Klimatická projekce vyberte __1995 (1981-2010), 2005 (1991-2020), 2035 (2021-2050), 2065 (2051-2080)__
     - 4.7 V nabídce Scénář vyberte některou z možností __SSP126, SSP245, SSP370 nebo SSP585__
     - 4.8 V nabídce Klimatická charakteristika vyberte __Počet dní se sněhovou pokrývkou nad 3 cm__
     - 4.9 V nabídce email zadejte vaši mailovou adresu a nechte si zaslat data
       
5. Zpracování dat sněhové pokrývky
     - 5.1 Na nový list __DnySnih3cm__ nakopíruji data stažená z portálu ClimRisk
     - 5.2 Data rozdělím do skupin podle jednotlivých normálů, zachovám pouze identifikaci měsíce a počet dní se sněhovou pokrývkou v měsících a za celý rok, zbývající data z ClimRisk smažu
     - 5.3 Všchny stažené datové sady pro normálový období porovnám pomocí sloupcového grafu
       
## Otázky k interpretaci dat ##
1. Jaké pozorujeme rozdíly ve srážkových úhrnech mezi dvěma historickými normály?
2. Jak souvisí tyto změny s již posouzenými změnami teplot a změnami v zaznamenané a očekávané sněhové pokrývce?
3. Jaké mohou tyto změny mít dopady v krajině v jednotlivých ročních obdobích?
4. Pokud srovnáte výsledky na vaši stanici a výsledky některého z kolegů, jaké pozorujete rozdíly?

</details>
  
<details markdown="1">
<summary> Cvičení 08 </summary>

# Cvičení 08 (13.11.2025) - Srážky - měření srážek, meteory, srážkový gradient

- Cílem cvičení je doplnit teorii z přednášek k tématům srážek a meteorů a ověřit srážkový gradient na vybraných stanicích
- __Na konci cvičení mám MS Excel soubor s novým listem SrazkovyGradient s opsanými daty pro vybrané stanice a vykresleným grafem gradientu__

## DŮLEŽITÉ ODKAZY ##
- Tabulky podnebí: [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf)

1. Doplnění teorie ke srážkám a meteorům
     - 1.0: ZDE bude k dispozici několik slidů ze cvičení k prostudování

2. Popsání srážkového gradientu s pomocí Tabulek podnebí
     - 2.0 Otevřu si Tabulky podnebí buď [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf) nebo si vezmu papírovou kopii
     - 2.1 Opíšu si jména stanic a nadmořské výšky 10 stanic z __Abecedního seznamu srážkoměrných stanic__ (téměř na konci tabulek, před tabulkou č. 52) na list __SrazkovyGradient__ ve svém pracovním excelu
     - 2.2 Nalistuji téměř na konci __Tabulku č. 52: Průměrný úhrn srážek (mm) za období 1901-1950__
     - 2.3 Opíšu průměrné roční srážkové úhrny
     - 2.4 V MS Excel vytvořím bodový graf z dat srážek a nadmořské výšky
     - 2.5 Zobrazím spojnici trendu včetně funkce a s pomocí zobrazené funkce ověřím míru teplotního gradientu u mojí stanice
     - 2.6 U grafu doplním veškeré náležitosti (Název, popisky os včetně jednotek, úplnou legendu, zdroj dat)

</details>
  
<details markdown="1">
<summary> Cvičení 09 </summary>

# Cvičení 09 (20.11.2025) - Tlak a vítr
- Cílem cvičení je získat a zpracovat data směru větru pro námi vybranou stanici a vytvořit větrnou růžici
- __Na konci cvičení mám MS Excel soubor s novým listem SmerVetru s denními daty směru větru pro moji stanici a hotový graf větrné růžice__

## DŮLEŽITÉ ODKAZY ##
- Denní data směru větru pro naši stanici z repozitáře ČHMÚ [ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/daily/wind/)

1. Stažení denních dat směru větru pro moji stanici
     - 1.0 [ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/daily/wind/) vyhledejte pomocí ID stanice soubor který v názvu obsahuje parametr _Dmax_
     - 1.1 Pokud se sem dostáváte z úvodní stránky repozitáře tak zvolte __daily__ a následně __wind__
  
2. Zpracování stažených dat
     - 2.0 Stažená data obsahují denní hodnoty směru větru (pro maximální rychlost) ve stupních, pro výšku 10 m nad zemí
     - 2.1 Data jsou oddělena čárkami a oddělovačem desetinných míst je tečka - musím data dostat do formátu čitelného mojí verzí MS Excel
          - Možnost 1: Můj Excel je přenastaven nebo od začátku operuje s čárkami a tečkami - nic neměním a jen otevřu data a zkontroluji že vypadají v pořádku
          - Možnost 2: Přenastavím Excel aby takto fungoval (potenciálně si rozbiju veškerá starší data, která zde již mám)
          - Možnost 3: Použiju fígl s poznámkovým blokem - nahradím čárky za středníky (;) a následně tečky za čárky, data uložím jako csv a načtu do MS Excel
     - 2.2 Pro další práci budeme potřebovat sloupce _DT_ a __VALUE__, zbývající můžeme smazat
     - 2.3 Smažeme veškerá data před rokem 1961
     - 2.4 Vytvoříme si pomocný sloupec __SmerZaokrouhleni__, pomocí kterého zjednodušíme data pouze na základní směry větru
     - 2.5 Potřebujeme směry pro 45, 90, 135, 180, 225, 270, 315, 360 stupňů a také zachovat hodnoty 0, kterými se označuje bezvětří
          - Vzorec pro českou verzi MS Excel: =KDYŽ(B2=0;"Calm";ZAOKR.DOLŮ(B2;45))
          - Vzorec pro anglickou verzi MS Excel: =IF(B2=0,"Calm",ROUNDDOWN(B2,45))
     - 2.6 Funkční vzorec použijeme pro celá data
     - 2.7 Bokem na stejném listu připravíme pomocnou tabulku pro vykreslení větrné růžice
          - Nadepíšeme si sloupce __Směr, SměrText, Četnost, Podíl__
          - Do sloupce __Směr__ opíšeme hodnoty 360, 45, 90, 135, 180, 225, 270, 315 a Calm
          - Do sloupce __SměrText__ S, SV, V, JV, J, JZ, Z, SZ a Bezvětří
          - Do sloupce __Četnost__ spočítáme kolikrát se daná zaokrouhlená hodnota vyskytuje v našem denním záznamu a použijeme výpočet pro všechny hodnoty směru
               - Vzorec využije funkci countif: __=COUNTIF(C:C;F4)__ (sečti všechny výskyty ve sloupci C, kdy se hodnota rovná vybrané buňce - např. F4)
          - Do sloupce __Podíl__ dopočítáme procentuální vyjádření četnosti
               - Nejdříve si pro všechny vypočítané četnosti uděláme sumu hodnot (např. __=suma(H3:H11)__)
               - Následně do sloupce __Podíl__ pro jednotlivé směry vypočítáme trojčlenkou procentuální zastoupení - abychom mohli vzorec roztáhnout pro všechny hodnoty musíme si zafixovat hodnotu sumy pomocí symbolů dolaru - např. __$H$12__
          - Výsledkem je hotová tabulka pro tvorbu grafu větrné růžice pro naši stanici
      
3. Tvorba grafu větrné růžice
     - 3.0 Pro tvorbu grafu vybereme naše procentuální hodnoty směru větru (mimo bezvětří)
     - 3.1 Na kartě __Vložení__ zvolíme možnost __Vložit vodopádový, trychtýřový, burzovní, povrchový nebo paprskový graf__ a v další nabídce vybereme __Paprskový s výplní__
     - 3.2 Doplníme všechny náležitosti grafu
     - 3.3 Jako popisky os zvolíme námi připravené texty ze sloupce __SměrText__
     - 3.4 Do grafu jako text přidáme také procentuální hodnotu pro bezvětří


</details>

<details markdown="1">
<summary> Cvičení 10 </summary>

# Cvičení 10 (27.11.2025) - Vlhkost vzduchu a výpar
</details>
  
<details markdown="1">
<summary> Cvičení 11 </summary>

# Cvičení 11 (04.12.2025) - Příprava na závěrečné prezentace

# Důležité odkazy na zdroje dat #
- Metadatový soubor pro vyhledání identifikátoru stanic: [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
- Datový repozitář ČHMÚ: [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)
- Tabulky podnebí: [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf)
- Data budoucího vývoje klimatu: [Dostupná na portálu ClimRisk](https://www.climrisk.cz/)

</details>

<details markdown="1">
<summary> Cvičení 12 </summary>

# Cvičení 12 (11.12.2025) - Společné prezentace výsledků a zápočty
</details>


