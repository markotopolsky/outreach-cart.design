---
type: project
status: active
created: 2026-08-10
updated: 2026-08-11
aliases: [Batch 18, Craft makers + knives SK/CZ/EN]
tags: [cart-design, cold-outreach, sk, cz, en, craft-makers, noze, sperky, koza, keramika]
---

# Outreach batch 18 — Craft makers (nože, šperky, koža, keramika) SK/CZ/EN

Remeselnícka niche naprieč štyrmi kategóriami (nožiarstvo, šperky, kožené výrobky, keramika),
tri trhy naraz (SK, CZ, EN). Marko explicitne uvoľnil kvalifikačnú latku 11.8.: *„nemusí byť
každý totálne kvalifikovaný, len potrebujem 50 leadom poslať email/IG správu dnes"* — dôraz na
objem cez jeden deň, nie na hĺbku overenia jedného leadu. Dôsledok: **žiadny lead v tejto dávke
nemá Kimi WebBridge overenie** (followers, dátum posledného postu = `neoverené` všade), celá
kvalifikácia stojí na zadarmo dostupnom `curl` + extrakcii kontaktu z HTML.

Metóda: Firecrawl search (discovery, 8 dotazov) → `curl` kvalifikácia (`qualify.py`, prahy zo
[[icp-dtc-znacky-sk-cz]] `stack.sh`, uvoľnené na 25+ scriptov namiesto 80+) → extrakcia emailu/IG
z HTML (`extract_contact.py`). Správy: variant A — [[opener-dvojfazovy-v1]] (fáza 1, žiadna
zmienka o službe) + [[pis-ako-clovek]] + [[citatel-nema-cas]] aplikované na každú správu.

⚠️ **Nič v tejto dávke nebolo odoslané.** Táto stránka je výstup `/scrape`, nie `/send` — správy
čakajú na Markovo schválenie a re-verifikáciu hookov v deň odoslania.

## Schválenie

- [ ] **Marko:** OK, posielaj / OK po úpravách
- Schválené: [dátum + čas]
- Schválených správ: [počet]

## Zhrnutie

| Metrika | Počet |
|---|---|
| **Preverených kandidátov** | 98 |
| **Kvalifikovaných leadov** | 51 |
| **Napísaných správ** | 51 |
| **Emailov** | 37 |
| **IG DM** | 14 |
| **SK leady** | 15 |
| **CZ leady** | 20 |
| **EN leady** | 16 |
| **Odoslaných (k 2026-08-11)** | 34 email draft + 3 IG naživo = 37 |
| **Odpovedí** | 1 (Lady Bead Jewelry, do 5 minút od odoslania) |
| **Reply rate** | 1/3 doručených IG (priebežné, príliš skoro na email drafty) |
| **Hook prežil re-verifikáciu (2026-08-11, deň odoslania)** | 46/51 |
| **Hook mŕtvy (re-overené 2026-08-11)** | 5/51 |
| **Neodoslané dnes — IG pauza (throttle)** | 9 (1 CZ MOOYYY + 8 EN), poslať zajtra |

Kvalifikácia podľa niky: nože 9 (všetkých 9 ⚠️HIGH-RISK platby), šperky 18, koža 13, keramika 11.

⚠️ **11.8. popoludní — IG search zaseklo na 4. DM (MOOYYY) po 3 úspešných sendoch (SK), možný throttle
signál po sérii rýchlych vyhľadávaní.** Žiadny duplikát, žiadne vlákno nevzniklo — len sa nedalo
pokračovať. Marko rozhodol zastaviť IG na dnes namiesto skúšania cez throttle (riziko banu > strata
jedného dňa). 3 IG DM doručené a potvrdené screenshotom (Lady Bead Jewelry, AP Jewellery, Janelit.sk),
34 emailov ako Gmail drafty (čakajú na Markovo Send), 9 IG DM (1 CZ + 8 EN) zapísané ako pripravené,
pošlú sa zajtra s denným re-overením hookov podľa `/send` skillu. Lady Bead Jewelry odpovedala do
5 minút: „Zdravím, mala som človeka ktorý mi stránku robil, tak túto informáciu rovno posuniem
ďalej, ja sa do toho nevyznám, ďakujem krásne!" — treba spracovať ako fázu 2.

### Re-verifikácia hookov v deň odoslania (2026-08-11, popoludní)

Krok 1 `/send batch-18` — rovnaká metóda ako pri pôvodnej kvalifikácii, ale tentokrát **4× curl na
lead** (medián, poznatok #11), nie 1×. Výsledok: **46/51 hookov prežilo, 5 zomrelo.** Status
stĺpec v tabuľkách nižšie má u každého leadu marker `✅`/`❌`. Žiadny lead nebol vymazaný — mŕtve
hooky zostávajú v tabuľke viditeľné, ako vyžaduje `/send` skill.

**5 mŕtvych hookov** (čas odozvy dnes popoludní klesol pod prah 1,5s, hook už nesedí):

| Lead | Pôvodný hook | Re-overené (4× curl, medián) | Poznámka |
|---|---|---|---|
| Nasha Keramika (nashakeramika.sk) | načítanie 2,19s | medián 1,45s (2,07/1,49/1,40/1,35s) | pod prahom; **NOVÝ hook, nie pôvodne písaný — treba prepísať správu**: 53 script tagov na homepage (nad uvoľneným prahom 25+) |
| MHKNIVES (mhknives.sk) | načítanie 2,20s | medián 1,20s (2,55/1,05/1,21/1,18s) | pod prahom; scripty = 24, tiež tesne pod uvoľneným prahom 25 — bez náhradného hooku |
| Keramika Patrik Daič (keramikadaic.cz) | načtení 1,76s | medián 0,14s (4,33/0,19/0,09/0,08s) | prvé meranie (4,33s) bol presne ten typ studeného/odľahlého merania, pred ktorým varuje poznatok #11; scripty = 15, bez náhradného hooku |
| Tomáš Linger (tomaslinger.cz) | načtení 1,79s | medián 0,37s (0,38/0,34/0,43/0,36s) | pod prahom; scripty = 26, tesne nad uvoľneným prahom — slabý kandidát, **NOVÝ hook, nie pôvodne písaný — treba prepísať správu** ak sa má poslať |
| Moss Bags (mossbags.com) | 1,90s | medián 0,52s (1,45/0,33/0,71/0,33s) | pod prahom; **NOVÝ hook, nie pôvodne písaný — treba prepísať správu**: 63 script tagov na homepage (solídne nad uvoľneným prahom) |

**4 hooky, kde sa presné číslo v texte správy zmenilo, ale prah stále platí** (hook žije, číslo v
správe pred odoslaním skontrolovať/upraviť):

- **Keramická dílna Petra Raisová** (keramickadilnapetra.cz) — pôvodne 3,50s, teraz medián 1,71s (2,97/1,65/1,74/1,68s). Stále nad prahom 1,5s, ale číslo v správe ("3,5 vteřiny") je teraz nepresné.
- **MontMat** (montmat.cz) — pôvodne 77 scriptov + 1,41s, teraz **výrazne horšie**: medián ~12,9s (20,05/19,18/6,61/2,67s, vrátane dvoch 20s timeoutov a jedného 301 presmerovania), scripty 77 nezmenené. Bolesť sa zosilnila, číslo v správe treba pred odoslaním aktualizovať.
- **Kovářství Čurda** (kovarstvicurda.cz) — pôvodne 3 zo 4 pokusov OK / 1 timeout, teraz **2 zo 4 timeout** (20,0/1,19/0,19/20,01s). Nestabilita potvrdená a mierne horšia.
- **river.sk** — SSL mismatch re-overený `curl -v`: identická chyba `SSL: no alternative certificate subject name matches target host name 'river.sk'` ako pri pôvodnej verifikácii. Hook nezmenený, plne platný.

## Leady a PRE-WRITTEN MESSAGES

### IG DM — SK leady

| # | Značka | IG handle | Followers | Hook (overené) | Správa | Dĺžka | Status | Dátum |
|---|---|---|---|---|---|---|---|---|
| 1 | Nasha Keramika | @nasha.keramika | neoverené | načítanie 2,19s (curl, 11.8.2026) | Ahoj, skúšal som dnes otvoriť Nasha Keramika a načítanie trvalo cez 2 sekundy, čo je na mobile cítiť. Riešiš to sama, alebo máš niekoho na web? | 26 slov | ❌ hook mŕtvy (re-overené 2026-08-11) | — |
| 2 | Ladybead Jewelry | @lady.bead.jewelry | neoverené | 92 script tagov na homepage (curl, 11.8.2026) | Ahoj, pozrel som sa na zdrojový kód ladybeadjewelry.sk a na hlavnej stránke sa spúšťa 92 scriptov naraz. To je dosť aj pre Shopify. Vieš o tom, alebo to niekto pridával appky postupne? | 32 slov | ✅ odoslané naživo (WebBridge, screenshot potvrdený) — **lead už odpovedal** | 2026-08-11 |
| 3 | AP Jewellery | @_ap_jewellery | neoverené | 71 script tagov na homepage (curl, 11.8.2026) | Ahoj, pozrel som si AP Jewellery a web má na homepage 71 script tagov spustených naraz. To je dosť aj na WooCommerce. Pridávala si appky postupne, alebo to tam bolo od začiatku? | 32 slov | ✅ odoslané naživo (WebBridge, screenshot potvrdený) | 2026-08-11 |
| 4 | Janelit | @janelit.sk | neoverené | 25 script tagov na homepage (curl, 11.8.2026) | Ahoj, pozrel som si Janelit.sk a na homepage mi napočítal 25 spustených scriptov, dosť veľa na taký jednoduchý katalóg. Je to appkami, alebo to bolo takto od začiatku? | 28 slov | ✅ odoslané naživo (WebBridge, screenshot potvrdený) | 2026-08-11 |

### Email — SK leady

| # | Značka | Email | Followers | Hook (overené) | Subject | Správa | Dĺžka | Status | Dátum |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Vegalm | info@vegalm.sk | neoverené | načítanie 2,76s (curl, 11.8.2026) | Rýchlosť webu Vegalm | Dobrý deň, skúšal som dnes otvoriť vegalm.sk a načítanie trvalo skoro 3 sekundy. Na mobile to vie odradiť skôr, než sa niekto dostane ku košíku. Riešite to interne, alebo cez niekoho externého? | 32 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 2 | River | river@river.sk | neoverené | SSL certifikát nesedí s doménou (curl -v, 11.8.2026) | Certifikát na river.sk | Dobrý deň, skúšal som otvoriť river.sk a prehliadač hlási, že bezpečnostný certifikát nesedí s doménou. Chrome to rovno označí ako nezabezpečené pripojenie, čo vie odradiť pri platbe. Viete o tom? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 3 | Vintageleather.sk | vintageleathereurope@gmail.com | neoverené | načítanie 2,43s + 85 script tagov (curl, 11.8.2026) | Web Vintageleather.sk pri meraní | Dobrý deň, pri meraní dnes trval vintageleather.sk 2,4 sekundy a na homepage beží 85 scriptov naraz. To je dosť aj na WooCommerce. Riešite to sami, alebo cez agentúru? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 4 | MHKNIVES ⚠️nože | info@mhknives.sk | neoverené | načítanie 2,20s (curl, 11.8.2026) | Rýchlosť mhknives.sk | Dobrý deň, skúšal som dnes otvoriť mhknives.sk a načítanie trvalo vyše 2 sekúnd. Pri damaškových nožoch, kde ľudia porovnávajú fotky detailov, to vie byť cítiť. Riešite web sami? | 28 slov | ❌ hook mŕtvy (re-overené 2026-08-11) | — |
| 5 | EGNE | egne@egne.sk | neoverené | načítanie 1,91s + 95 script tagov (curl, 11.8.2026) | 95 scriptov na egne.sk | Dobrý deň, pozrel som sa na egne.sk, na homepage beží 95 script tagov a načítanie trvá skoro 2 sekundy. To je dosť pre e-shop so šperkami. Pridávali ste appky postupne? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 6 | BountyBoho | info@bountyboho.sk | neoverené | 154 script tagov na homepage (curl, 11.8.2026) | 154 scriptov na BountyBoho | Dobrý deň, pozrel som sa pod kapotu bountyboho.sk a na homepage beží 154 script tagov naraz, čo je vysoko aj na bežné Shopify či WooCommerce štandardy. Viete, čo tam všetko beží? | 31 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 7 | DaLea | sperky@dalea.sk | neoverené | načítanie 2,23s (curl, 11.8.2026) | Rýchlosť dalea.sk | Dobrý deň, skúšal som dnes otvoriť dalea.sk a načítanie trvalo cez 2 sekundy. Pri mandalách a živicových šperkoch, kde ľudia listujú fotky, to vie byť cítiť na mobile. Riešite to sami? | 31 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 8 | RK Design | kabrichard@gmail.com | neoverené | 75 script tagov na homepage (curl, 11.8.2026) | 75 scriptov na RK Design webe | Dobrý deň, pozrel som si rkdesign.sk, na homepage beží 75 scriptov naraz. Pri Wixe je to dosť vysoko. Pridávali ste appky postupne, alebo to tak vzniklo od začiatku? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 9 | Kožené veci (Jozef Rabatin) | kozenevecisk@gmail.com | neoverené | 35 script tagov na homepage (curl, 11.8.2026) | Web kozeneveci.sk | Dobrý deň, pozrel som si kozeneveci.sk, na homepage mi napočítal 35 spustených scriptov, dosť na jednoduchý katalóg koženej galantérie. Je to appkami, alebo to bolo takto od začiatku? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 10 | OstréNože.sk ⚠️nože | info@ostrenoze.sk | neoverené | 27 script tagov na homepage (curl, 11.8.2026) | Web ostrenoze.sk | Dobrý deň, pozrel som si ostrenoze.sk, na homepage beží 27 scriptov, dosť na katalóg s nožmi a brúsením. Je to appkami z WooCommerce, alebo to tam pridával niekto postupne? | 29 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 11 | LaWande | lawande.handmade@gmail.com | neoverené | 31 script tagov na homepage (curl, 11.8.2026) | Web LaWande | Dobrý deň, pozrel som si lawande.sk, na homepage mi napočítal 31 scriptov, dosť na jednoduchý šperkový katalóg. Pridávate appky priebežne, alebo to bolo takto od začiatku? | 26 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |

### IG DM — CZ leady

| # | Značka | IG handle | Followers | Hook (overené) | Správa | Dĺžka | Status | Dátum |
|---|---|---|---|---|---|---|---|---|
| 1 | MOOYYY | @mooyyy_jewelry | neoverené | 42 script tagov na homepage (curl, 11.8.2026) | Ahoj, koukal jsem na MOOYYY a na homepage běží 42 scriptů najednou, dost na jednoduchý katalog minimalistických šperků na WordPressu. Přidávaly se appky postupně, nebo to bylo takhle? | 28 slov | ⏸️ neodoslané — IG vyhľadávanie zaseklo (možný throttle), žiadny duplikát, žiadne vlákno nevzniklo | — |

### Email — CZ leady

| # | Značka | Email | Followers | Hook (overené) | Subject | Správa | Dĺžka | Status | Dátum |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Keramika Patrik Daič | keramika.daic@seznam.cz | neoverené | načtení 1,76s (curl, 11.8.2026) | Rychlost webu Keramika Daič | Dobrý den, dnes jsem zkoušel otevřít keramikadaic.cz a načtení trvalo skoro 2 sekundy. Na mobilu to je cítit, hlavně u fotek keramiky. Řešíte to sami, nebo přes někoho externího? | 29 slov | ❌ hook mŕtvy (re-overené 2026-08-11) | — |
| 2 | Keramická dílna Petra Raisová | info@touchesofclay.eu | neoverené | načtení medián 1,71s, 4x curl (re-overené 11.8.2026) | Web se načítal 1,7 vteřiny | Dobrý den, zkoušel jsem dnes čtyřikrát otevřít vaši dílnu na webu a načtení trvalo v průměru 1,7 vteřiny. To je dost i na WooCommerce. Řešíte web sama, nebo máte na to někoho? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send — text opravený na aktuálne číslo (bolo 3,5s, teraz 1,71s) | 2026-08-11 |
| 3 | Lovecky Leather | jakub@loveckyleather.cz | neoverené | 95 script tagov na homepage (curl, 11.8.2026) | 95 scriptů na loveckyleather.cz | Dobrý den Jakube, koukal jsem na loveckyleather.cz, na homepage běží 95 script tagů najednou. To je docela vysoko i na Shopify. Přidávaly se appky postupně, nebo to tam bylo od začátku? | 31 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 4 | Tomáš Linger | tomaslinger@gmail.com | neoverené | načtení 1,79s (curl, 11.8.2026) | Rychlost tomaslinger.cz | Dobrý den, zkoušel jsem dnes otevřít tomaslinger.cz a načtení trvalo skoro 1,8 vteřiny. U kožených peněženek, kde lidi porovnávají detaily na fotkách, to je cítit. Řešíte web sám, nebo přes agenturu? | 31 slov | ❌ hook mŕtvy (re-overené 2026-08-11) | — |
| 5 | Kovářství Čurda ⚠️nože | curda.jiri@centrum.cz | neoverené | 3 zo 4 pokusov OK, 1 zo 4 timeout na 20s (curl 4x, 11.8.2026) | Web dnes 1x úplně spadl | Dobrý den, zkoušel jsem dnes web kovarstvicurda.cz čtyřikrát. Třikrát naběhl rychle, jednou úplně spadl na 20 vteřin timeoutu. Víte o tom, nebo je to jen u mě? | 27 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send — nestabilita potvrdená, teraz 2/4 timeout (predtým 1/4) | 2026-08-11 |
| 6 | Kera Studio | info@kerastudio.cz | neoverené | 71 script tagov na homepage (curl, 11.8.2026) | 71 scriptů na kerastudio.cz | Dobrý den, koukal jsem na kerastudio.cz a na homepage běží 71 script tagů najednou, dost i na Next.js stránku. Přidávaly se appky nebo pluginy postupně, nebo to tak bylo od začátku? | 31 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 7 | Sharp Knives ⚠️nože | info@sharpknives.cz | neoverené | 50 script tagov na homepage (curl, 11.8.2026) | 50 scriptů na Sharp Knives webu | Dobrý den, koukal jsem na sharpknives.cz, na homepage běží 50 script tagů najednou na WooCommerce. U nožů, kde lidi zvětšují fotky ostří, to zpomalení je cítit. Přidávaly se pluginy postupně? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 8 | Katyba | info@katyba.cz | neoverené | 50 script tagov na homepage (curl, 11.8.2026) | 50 scriptů na katyba.cz | Dobrý den, koukal jsem na katyba.cz, na homepage běží 50 scriptů najednou, dost na katalog šperků a dřevěných hodin. Přidávaly se appky postupně, nebo to bylo takhle od začátku? | 29 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 9 | Perlina | perlinacz@email.cz | neoverené | 46 script tagov na homepage (curl, 11.8.2026) | 46 scriptů na Perlina.cz | Dobrý den, koukal jsem na perlina.cz, na homepage běží 46 scriptů na Shoptetu, dost na jednoduchý katalog šperků. Přidávaly se appky postupně, nebo to tam bylo od začátku? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 10 | MontMat | info@montmat.cz | neoverené | 2 zo 4 pokusov ~20s timeout, medián 12,9s (curl 4x, re-overené 11.8.2026) | MontMat dnes 2x nenaběhl | Dobrý den, koukal jsem dnes na montmat.cz čtyřikrát a dvakrát ze čtyř pokusů se stránka vůbec nenačetla (20 vteřin timeout). Homepage běží i tak na 77 scriptech. Přidávaly se appky postupně, nebo to tam bylo od začátku? | 32 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send — text prepísaný na aktuálne (silnejšie) dáta, pôvodne 1,4s | 2026-08-11 |
| 11 | Atelier Kruh | info@atelierkruh.cz | neoverené | 72 script tagov na homepage (curl, 11.8.2026) | 72 scriptů na Atelier Kruh | Dobrý den, koukal jsem na atelierkruh.cz, na homepage běží 72 scriptů na WooCommerce, dost na jednoduchý keramický katalog. Přidávaly se appky postupně, nebo to bylo takhle od začátku? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 12 | Kůže Kubát | JanKubat@email.cz | neoverené | 36 script tagov na homepage (curl, 11.8.2026) | Web kubatkuze.cz | Dobrý den, koukal jsem na kubatkuze.cz, na homepage mi napočítal 36 scriptů, dost na jednoduchý katalog kabelek a aktovek. Je to appkami, nebo to bylo takhle od začátku? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 13 | Keramika Katka | info@keramikakatka.cz | neoverené | 34 script tagov na homepage (curl, 11.8.2026) | Web Keramika Katka | Dobrý den, koukal jsem na keramikakatka.cz, na homepage mi napočítal 34 scriptů, dost na jednoduchý keramický katalog. Přidávaly se appky postupně, nebo to tam bylo od začátku? | 27 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 14 | Originální šperky Dity Fleischlingerové | dita.fle@gmail.com | neoverené | 34 script tagov na homepage (curl, 11.8.2026) | Web sperkydita.cz | Dobrý den Dito, koukal jsem na sperkydita.cz, na homepage mi napočítal 34 scriptů na WooCommerce, dost na jednoduchý katalog šperků. Přidávaly se appky postupně, nebo to bylo takhle od začátku? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 15 | Puncz.cz | informace@puncz.cz | neoverené | 33 script tagov na homepage (curl, 11.8.2026) | Web Puncz.cz | Dobrý den, koukal jsem na puncz.cz na Shoptetu, na homepage mi napočítal 33 scriptů, dost na jednoduchý katalog autorských šperků. Přidávaly se appky postupně, nebo to bylo takhle od začátku? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 16 | Ateliér Hnízdo | rldekor@seznam.cz | neoverené | 26 script tagov na homepage (curl, 11.8.2026) | Web Ateliér Hnízdo | Dobrý den, koukal jsem na atelierhnizdo.cz na Shoptetu, na homepage mi napočítal 26 scriptů, dost na jednoduchý keramický katalog. Přidávaly se appky postupně, nebo to tam bylo od začátku? | 29 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 17 | Brašnářství Tlustý | mail@tlustypraha.cz | neoverené | 26 script tagov na homepage (curl, 11.8.2026) | Web Brašnářství Tlustý | Dobrý den, koukal jsem na tlustypraha.cz, na homepage mi napočítal 26 scriptů, dost na jednoduchý katalog tašek a batohů. Řešíte web sami, nebo přes někoho externího? | 26 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 18 | Ateliér Radost (Pichovi) | atelierradost@seznam.cz | neoverené | 26 script tagov na Next.js homepage (curl, 11.8.2026) | Web Ateliér Radost | Dobrý den, koukal jsem na atelier-radost.cz, na Next.js homepage mi napočítal 26 scriptů, dost i na modernější stack. Řešíte web sami, nebo přes někoho externího? | 25 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 19 | Keramika Maříž | keramika@keramika-mariz.cz | neoverené | 47 script tagov na homepage (curl, 11.8.2026) | 47 scriptů na Keramika Maříž | Dobrý den, koukal jsem na keramika-mariz.cz, na homepage běží 47 scriptů na WooCommerce, dost na jednoduchý keramický katalog. Přidávaly se appky postupně, nebo to bylo takhle od začátku? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |

### IG DM — EN leady

| # | Značka | IG handle | Followers | Hook (overené) | Správa | Dĺžka | Status | Dátum |
|---|---|---|---|---|---|---|---|---|
| 1 | YV Ceramics | @yv.ceramics | neoverené | 82 script tags on homepage (curl, 2026-08-11) | Hey, I checked YV Ceramics and the homepage loads 82 scripts at once on Shopify. That's above what most small pottery shops run. Were those apps added one at a time? | 31 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 2 | Moss Bags | @moss.bags | neoverené | načítanie 1,90s (curl, 2026-08-11) | Hey, I pulled up mossbags.com today and it took almost 2 seconds to load. On mobile that's the kind of delay people bounce on before they even see the bags. Is the site slow for you too, or just at my end? | 42 slov | ❌ hook mŕtvy (re-overené 2026-08-11) | — |
| 3 | Everthine Jewelry | @everthine_jewelry | neoverené | 77 script tags on homepage (curl, 2026-08-11) | Hey, I checked Everthine Jewelry and the homepage loads 77 scripts at once on Shopify. That's high for a small studio catalog. Were those added one app at a time? | 30 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 4 | AMO Bladesmithing ⚠️nože | @amobladesmithing | neoverené | 62 script tags on homepage (curl, 2026-08-11) | Hey, I checked amobladesmithing.com and the homepage runs 62 scripts on Wix. That's a lot for a handmade kitchen knife shop. Were those added gradually, or built that way? | 29 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 5 | Awl Snap | @awlsnap | neoverené | 61 script tags on homepage (curl, 2026-08-11) | Hey, I checked Awl Snap's site and the homepage loads 61 scripts at once on Shopify. That's high for a leather goods shop. Were those apps added one at a time? | 31 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 6 | Sunny Ceramics | @sunnyceramicsatl | neoverené | 58 script tags on homepage (curl, 2026-08-11) | Hey, I checked Sunny Ceramics and the homepage loads 58 scripts at once on Squarespace. That's high for a pottery shop. Were those added gradually, or built in from the start? | 31 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 7 | Woody Brand Knives ⚠️nože | @woodybrandknives | neoverené | 57 script tags on homepage (curl, 2026-08-11) | Hey, I checked Woody Brand Knives and the homepage runs 57 scripts at once on Shopify. That's a lot for a knife catalog. Were those apps added one at a time? | 31 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 8 | Fail Jewelry | @failjewelry | neoverené | 52 script tags on homepage (curl, 2026-08-11) | Hey, I checked Fail Jewelry and the homepage loads 52 scripts at once on Shopify. Were those apps added one at a time, or built that way from the start? | 30 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |
| 9 | Fiddleback Forge (Andy Roy) ⚠️nože | @fiddlebackforge | neoverené | 47 script tags on homepage (curl, 2026-08-11) | Hey Andy, I checked Fiddleback Forge and the homepage loads 47 scripts at once on Shopify. Were those added one at a time, or built that way from the start? | 30 slov | ⏸️ neodoslané dnes — IG pauza po throttle signáli, poslať zajtra s denným re-overením | — |

### Email — EN leady

| # | Značka | Email | Followers | Hook (overené) | Subject | Správa | Dĺžka | Status | Dátum |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Dragon's Breath Forge ⚠️nože | info@dragonsbreathforge.com | neoverené | 71 script tags on homepage (curl, 2026-08-11) | 71 scripts on Dragon's Breath Forge | Hey, I pulled up dragonsbreathforge.com and counted 71 script tags loading on the homepage. That's a lot for a WooCommerce knife shop. Were those added one plugin at a time, or built that way? | 34 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 2 | J.Mills Studio | staff@jmillsstudio.com | neoverené | 58 script tags on homepage (curl, 2026-08-11) | 58 scripts on J.Mills Studio | Hey, I checked jmillsstudio.com and the homepage loads 58 script tags at once. That's a lot for a Shopify jewelry catalog. Were those added gradually, or was it like that from the start? | 33 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 3 | Billie Marie | hello@billiemariegoods.com | neoverené | 57 script tags on homepage (curl, 2026-08-11) | 57 scripts on Billie Marie | Hey, I looked under the hood of billiemariegoods.com and the homepage runs 57 scripts at once on Shopify. Were those apps added one at a time, or built in from day one? | 32 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 4 | Haley Lebeuf | info@haleylebeuf.com | neoverené | 54 script tags on homepage (curl, 2026-08-11) | 54 scripts on Haley Lebeuf | Hey, I pulled up haleylebeuf.com and counted 54 script tags on the homepage. That's a fair amount for a small jewelry shop. Were those added one app at a time? | 30 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 5 | Stitch and Tickle | info@stitchandtickle.com | neoverené | 51 script tags on homepage (curl, 2026-08-11) | 51 scripts on Stitch and Tickle | Hey, I checked stitchandtickle.com and the homepage loads 51 scripts at once on Shopify. Were those apps added gradually, or was it built that way from the start? | 28 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 6 | Chelsea Miller Knives ⚠️nože | chelsea@chelseamillerknives.com | neoverené | 51 script tags on homepage (curl, 2026-08-11) | 51 scripts on Chelsea Miller Knives | Hey Chelsea, I pulled up chelseamillerknives.com and counted 51 script tags loading on the homepage. That's a lot for a handmade knife catalog. Were those added one plugin at a time? | 31 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |
| 7 | Storica Studio | info@storicastudio.com | neoverené | 47 script tags on homepage (curl, 2026-08-11) | 47 scripts on Storica Studio | Hey, I checked storicastudio.com and the homepage runs 47 scripts at once. That's a fair amount for a small jewelry studio site. Were those added one app at a time, or built that way from the start? | 37 slov | 📧 draft vytvorený (Gmail), čaká na Markovo Send | 2026-08-11 |

## Vylúčení kandidáti

Plný zoznam všetkých 47 vylúčených s dôvodmi a dôkazmi je v raw súbore (zdroje nižšie).
Najdôležitejšie prípady:

| Meno | Dôvod | Zistený |
|---|---|---|
| kozeny.sk | rovnaký kontaktný email ako vegalm.sk (info@vegalm.sk/vega@vegalm.sk), pravdepodobne rovnaký prevádzkovateľ — neoslovovať dvakrát tú istú firmu | curl + extrakcia kontaktu, 11.8.2026 |
| harakka.eu | má reálnu bolesť (1,54s), ale žiadny funkčný kontakt — email v HTML je placeholder `example@yourdomain.com`, žiadny IG odkaz | curl + Firecrawl scrape /pages/contact, 11.8.2026 |
| kudlarstvi.cz | mŕtva doména — žiadna odpoveď ani cez HTTP/HTTPS insecure | curl, 11.8.2026 |
| sima-prague.com | HTTP 403 — nejednoznačné (možný anti-bot blok, nie preukázateľne mŕtvy biznis) | curl, 11.8.2026 |
| ostatných 43 | pod uvoľneným prahom (< 25 scriptov, < 1,5s odozva, žiadna iná bolesť) — platformový boilerplate, nie nález | curl `qualify.py`, 11.8.2026 |

## Poznámky

- **Uvoľnená kvalifikačná latka.** Marko 11.8.: potreboval 50 leadov na dnešné odoslanie, nie hĺbkové
  overenie jedného leadu. Preto sa táto dávka opiera takmer výhradne o `curl` (platforma, čas
  odozvy, počet `<script>` tagov) a **nie** o Kimi WebBridge — na rozdiel od batchov 13-17.
  Dôsledok: **followers a dátum posledného postu sú `neoverené` pri všetkých 51 leadoch.**
  Pred `/send` treba aspoň spot-check na najsilnejších hookoch (BountyBoho 154 scriptov,
  river.sk SSL certifikát, Keramická dílna Petra Raisová 3,5s), aby sa vylúčili spiace účty
  (poznatok #5).
- **Prah kvalifikácie znížený z 80 na 25+ scriptov** pre kandidátov bez inej bolesti. Toto je
  slabšia bolesť než oficiálny prah (poznatok #10 varuje pred platformovým boilerplate) — správy
  preto rámcujú fakt opatrne ("na homepage beží X scriptov", otázka "pridávali ste appky
  postupne") namiesto tvrdenia o preukázanom probléme. Kandidáti s oficiálnym prahom (čas > 1,5s,
  scripty > 80, SSL chyba, mŕtva doména) sú silnejšie hooky — viď stĺpec Hook v tabuľkách.
- **⚠️ Nože = HIGH-RISK platby (9 leadov v dávke):** mhknives.sk, kovarstvicurda.cz, sharpknives.cz,
  ostrenoze.sk, dragonsbreathforge.com, amobladesmithing.com, woodybrandknives.com,
  chelseamillerknives.com, fiddlebackforge.com. Podľa [[icp-handmade-makers]] treba platobný
  procesor overiť **pred fázou 2 (pitch), nie pred otváračom** — v poriadku poslať tieto otvárače,
  ale nepokračovať do pitchu bez overenia Stripe/platobnej brány.
- **Backlog-heavy nožiari nemajú čo predávať.** Žiadny z 9 knife leadov v tejto dávke nebol overený
  na kapacitu ("má vôbec čo predávať", filter z [[icp-handmade-makers]] — porovnaj s Don Hansonom,
  ktorý mal 6-8-ročný backlog). Odporúčanie: pri odpovedi sledovať, či lead hovorí ako predajca s
  voľnou kapacitou, alebo ako remeselník zavalený objednávkami (pattern #2 v [[insights]]).
- **Duplicitný prevádzkovateľ vylúčený, nie duplicitne oslovený.** vegalm.sk a kozeny.sk zdieľajú
  kontaktné emaily — zaradený len vegalm.sk.
- **Zdieľaný web-builder kontakt.** ladybeadjewelry.sk a awlsnap.com mali v HTML identický email
  `info@stagheaddesigns.com` (pravdepodobne spoločná šablóna/agentúra) — pre oba nahradený IG DM
  kanálom, aby sa nepísalo na kontakt, ktorý nemusí byť značky.
- **Krátke emaily oproti cieľovému rozsahu 40-80 slov.** Väčšina SK/CZ/EN emailov v tejto dávke má
  26-37 slov, pod cieľovým rozsahom z [[citatel-nema-cas]]. Zámerné — dáta v tom istom skille
  ukazujú, že najkratšie správy v celej pipeline (SK dávka, [[outreach-batch-3]]) mali najvyššiu
  odpoveďovosť (67 %). Nepridávaná vata len na dosiahnutie cieľového počtu slov.
- **river.sk je najneobvyklejší hook v dávke** — nie pomalý web, ale neplatný SSL certifikát
  (curl -v: `no alternative certificate subject name matches target host name`). Presne typ
  nespochybniteľného nálezu, ktorý poznatok #18 odporúča nad slabšie proxy signály.

## Zdroje

- Re-verifikácia hookov v deň odoslania (2026-08-11, popoludní) — `curl` 4× na lead (medián,
  User-Agent Chrome desktop, `--max-time 20`), počet `<script>` tagov cez Python `re.S` regex,
  `curl -v` pre river.sk SSL. Vlastný skript tejto session, rovnaká metodika ako pôvodná
  kvalifikácia. Krok 1 z `/send batch-18`.
- `raw/cart.design/cold-outreach/craft-knives-batch18-verified-2026-08-11.md` — plný zoznam všetkých 98 kandidátov (51 kvalifikovaných + 47 vylúčených)
- [[wiki/outreach/prompts/opener-dvojfazovy-v1|Prompt: variant A]]
- [[wiki/outreach/skills/pis-ako-clovek|Skill: píš ako človek]]
- [[wiki/outreach/skills/citatel-nema-cas|Skill: čitateľ nemá čas]]
- [[icp-handmade-makers]] — ICP v1, nože HIGH-RISK platby, kapacitný filter
- [[icp-dtc-znacky-sk-cz]] — `stack.sh` metodika kvalifikácie
- [[insights]] — poznatky #5 (spiaci účet), #10 (boilerplate), #11 (merať 4×), #18 (nespochybniteľný nález)