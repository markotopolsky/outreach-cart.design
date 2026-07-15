# Konkurencia - čo ukázala analýza ich eshopu

Tento dokument je výťah z technickej analýzy fitnessmenu.eu. Nie je to len zoznam bugov. Je to dôkaz, že produkt, ktorý Boris aktuálne porovnáva s naším, má hlboké problémy, ktoré mu môžu uškodiť aj právne, aj obchodne.

## Čo je tam kritické (P0 problémy)

### Päť rôznych firiem na jednom eshope

Toto je najväčší nález z celej analýzy. V pätičke eshopu sa striedajú päť rôznych s.r.o. podľa toho, na akej stránke si. Objednávkový formulár ukazuje "Real Estate Factory s. r. o." z Senice, čo je firma, ktorá má v názve reality a predáva jedlo. Košík ukazuje INVIZ s. r. o. Cenník má Maboma Holding. A tak ďalej.

Toto nie je technická detailka. Zákazník, ktorý klikne z hlavnej stránky na objednávku, v skutočnosti kupuje od inej firmy. Pri platbe cez Stripe alebo ComGate je to problém s merchant-of-record nastavením. A pri akomkoľvek spore so zákazníkom je to spotrebiteľský problém, pretože zmluva nie je jasná s kým je uzavretá.

Pre Borisa je to konkrétny právny a reputačný risk, ktorý pravdepodobne nevie, že tam je.

### Broken SEO, 238 stránok, ktoré nefungujú správne

Vytvorili 238 stránok pre jednotlivé mestá, čo je dobrý SEO nápad. Ale pri generovaní URL adries použili chybný algoritmus na slovenské diakritické znaky. Výsledok je, že Žabokreky nad Nitrou má URL "/uabokreky-nad-nitrou", Dežerice má "/deyerice", a podobne. Tieto stránky sú buď zle zaindexované alebo nie sú zaindexované vôbec. SEO investícia je z veľkej časti premrhaná.

### Tri rôzne ceny za doručenie na troch rôznych stránkach

Hlavná stránka: 4,60 €. Stránka doručenia: zadarmo. Cenník: záleží od mesta. Zákazník, ktorý si prechádza eshop pred objednávkou, nedostane rovnakú odpoveď dvakrát. To je presne ten moment, keď ľudia prestanú dôverovať a opustia košík.

### Cena "od 11,90 €" vs reálne minimum 18,40 €

Na hlavnej stránke je hero cena 11,90 € za deň. Na cenniku je minimum 18,40 €. To je skoro 60% rozdiel medzi tým, čo zákazník vidí na úvod a čím nakoniec zaplatí. Pre ľudí, ktorí si porovnávajú ponuky, je toto klasický "anchor then shock" moment, ktorý zabíja konverzie.

## Čo je tam závažné (P1 problémy)

### Konfigurátor a menu sú dve oddelené veci

Keď zákazník konfiguruje balík, nevidí ani jedno jedlo. Menu je na inej stránke a z tej stránky sa nedá objednať. Zákazník si musí sám preskakať medzi záložkami a pamätať si, čo videl. Pre niekoho, kto si vyberá stravovanie na mesiac, je to frustrujúci zážitok.

### Alergie sa riešia až po nákupe

Zákazník si nakonfiguruje balík, zaplatí a až potom mu systém povie, či mu vie prispôsobiť jedlá podľa alergií. Pre niekoho s laktózovou intoleranciou alebo celiakiou to znamená, že platí naslepo.

### Trial neprechádza do subscripcie automaticky

Po skúšobnom balíku dostanú zákazníci 15 € zľavový kupón. To je všetko. Žiadny jeden klik, žiadne "pokračuj rovnakou konfiguráciou". Zákazník musí sám ísť znova nakonfigurovať celý balík od začiatku. Konverzný potenciál sa tým výrazne znižuje.

### Žiadny Apple Pay ani Google Pay

Napriek tomu, že majú Stripe (ktorý tieto platby nativne podporuje), nikde nie je zmienka o Apple Pay ani Google Pay. Pre mobilných zákazníkov, ktorí sú jadrom tejto cieľovky, je to zbytočná bariéra pri platbe.

## Čo tam naopak funguje dobre

Toto je dôležité vedieť, aby sme nepreceňovali slabiny a vedeli, čo budeme musieť prekonať:

Štvorkrokový konfigurátor je dobre navrhnutý ako informačná architektúra. Výber kalórií nie je len číslo, ale je pomenovaný cieľom ("Výrazné chudnutie", "Silový šport"). To je dobrý UX prístup.

Operatívne mechanizmy majú premyslené. Možnosť preskočiť deň a prekonvertovať ho na kredit je dobrá. Automatická substitúcia jedál pri alergii funguje a je lepšia ako väčšina konkurentov. Platba stravovacími poukážkami (Edenred, Up, Doxx, Ticket Restaurant) je pre firemných zákazníkov reálna výhoda.

## Čo to znamená pre náš pitch

Boris pravdepodobne nevie o väčšine týchto problémov. Má produkt, ktorý navonok vyzerá funkčne, ale vo vnútri je postavený na kóde, ktorý nikto poriadne neskontroloval.

Keď mu ukážeme náš produkt vedľa tohto, nehovoríme "naše je krajšie". Hovoríme "naše je bezpečné, funkčné a postavené tak, aby mu nespôsobilo problémy so zákonom, so SEO a so zákazníkmi pri platbe."

Kľúčové argumenty vyplývajúce z tejto analýzy:

Právna situácia s piatimi firmami je niečo, čo môže kedykoľvek skomplikovať jeho podnikanie. My by sme niečo také nikdy nedoručili.

SEO investícia do 238 stránok je z veľkej časti zbytočná kvôli technickej chybe, ktorú si nikto nevšimol. My máme review procesy.

Tri rôzne ceny za doručenie a dva rôzne zoznamy produktov na rôznych stránkach sú symptómom toho, že produkt bol generovaný bez toho, aby ho niekto prečítal ako zákazník. My to robíme inak.

## Čo ešte nevieme

Analýza bola robená cez server-rendered HTML bez spustenia JavaScriptu. Teda reálny konfigurátor, checkout formuláre, mobilné zobrazenie a správanie platobnej brány nebolo možné overiť. Je pravdepodobné, že ďalšie problémy sú aj tam, len nie sú viditeľné z HTML výstupu.
