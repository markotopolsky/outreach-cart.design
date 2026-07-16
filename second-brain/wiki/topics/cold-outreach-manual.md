---
type: answer
created: 2026-07-15
updated: 2026-07-15
aliases: [Cold outreach manuál, Outreach systém]
tags: [cart-design, outreach, sales]
---

# Cold outreach — manuál (cart.design)

Syntéza troch raw súborov do jedného použiteľného postupu. Cieľ: z research poznámky o prospektovi vyrobiť personalizovanú cold správu cez AI a začať oslovovanie.

## Systém v jednej vete

```
Research → šablóna → FÁZA 1: otvárač (bez predaja) → reakcia? → FÁZA 2: pitch správa → follow-up po 3–5 dňoch
```

Tvoja práca je **research a štruktúrovaný zápis** — kvalita správy stojí a padá na kvalite dát v poznámke, nie na prompte.

**Dvojfázový prístup** (overený z minulých outreachov — reakcie prichádzali na pain point, nie na ponuku):
- **Fáza 1 — otvárač:** krátka správa, ktorá len otvorí konverzáciu. Postreh alebo otázka k ich pain pointu / háčiku. Žiadna zmienka o tom, čo predávaš.
- **Fáza 2 — pitch:** až keď zareagujú, nadviaž a prejdi k tomu, čo vieš ponúknuť (master prompt z Outreach_System).

## Krok za krokom

### 1. Nájdi prospekta a sprav research
Hľadaj lokálne biznisy / online značky bez eshopu alebo so zastaraným eshopom (Instagram explore, hashtagy, lokálne firmy). Zisti:
- web, sociálne siete, či má eshop a v akom stave
- **aspoň 1 konkrétny pain point** (predáva len cez DM, pomalý web, žiadny katalóg…)
- **aspoň 1 osobný háčik** (nedávny post, nová kolekcia, story "nestíham odpisovať"…)

### 2. Vyplň šablónu
Skopíruj `raw/cart.design/cold-outreach-system/templates/Prospect_Template.md` do `raw/cart.design/cold-outreach-clients/<firma>-raw.md` a vyplň. Povinné minimum: meno + firma, kanál, jazyk + tón, 1 pain point, 1 osobný háčik, sekcia „Ako začať konverzáciu". `status` udržuj aktuálny: `novy → osloveny → odpoved → stretnutie → klient / nezaujalo`. Stav všetkých prospektov naraz sleduje [[cold-outreach-pipeline]].

### 3. FÁZA 1 — otvárač (prvý reach-out, bez predaja)
V šablóne vyplň sekciu **„Ako začať konverzáciu"** — vyber 1 pain point / háčik, ktorý vie ukradnúť ich attention. Potom vlož do AI tento **opener prompt** + obsah poznámky:

```
Si expert na cold outreach. Napíš PRVÚ správu potenciálnemu klientovi, ktorej jediný cieľ je VYVOLAŤ REAKCIU a otvoriť konverzáciu — NIE predávať.

Pravidlá:
- Vyber najsilnejší pain point alebo osobný háčik z poznámky (prednostne zo sekcie "Ako začať konverzáciu")
- Sformuluj ho ako úprimný postreh alebo otázku, na ktorú sa im chce odpovedať
- ŽIADNA zmienka o mojich službách, o tom čo robím, ani náznak ponuky
- Žiadne CTA na call/stretnutie — jediné "CTA" je prirodzená otázka
- Krátke: DM/WhatsApp 20–40 slov, email 40–80 slov
- Tón a jazyk podľa polí `ton` a `jazyk` v poznámke
- Píš ako človek, ktorý si ich fakt všimol — nie ako sales šablóna

Dáta o klientovi:
[SEM VLOŽ OBSAH POZNÁMKY]

Výstup: 2 varianty otvárača + 1 veta prečo by mal vyvolať reakciu.
```

### 3b. FÁZA 2 — pitch (až po reakcii)
Keď odpovedia, vlož do AI **master prompt** z [[Outreach_System|Outreach_System]] (Krok 2, sekcia PROMPT) + obsah poznámky + ich odpoveď. Dostaneš 2 varianty (A = hlavný tip, B = iný uhol). Vyber, prípadne dolaď rukou — správa musí znieť ako ty.

Kontrola pred odoslaním (pravidlá zo systému):
- začína **o nich**, nie o tebe ("Dobrý deň, volám sa…" = zle)
- konkrétny problém, nie vágne frázy
- 1–2 vety riešenie + dopad, žiadny zoznam služieb
- mäkké CTA ("Stálo by za to sa o tom porozprávať?")
- dĺžka podľa kanála: email 80–150 slov, LinkedIn 50–100, IG/FB DM 30–70, WhatsApp/SMS 30–50

### 3c. Pozor pri ručnej úprave detailov v otvárači
Ak meníš konkrétny detail v návrhu (produkt, dátum, číslo) na želanie Marka, over ho **proti zdroju** predtým, než to pošleš — nie len štylisticky. Príklad z 15.7.: zámena "náhrdelník" → "prsteň" v otvárači pre saint.jewellry takmer spôsobila, že by sme jej poslali opis produktu, ktorý nikdy nepostovala; ona si vyžiadala fotku, čím sa chyba odhalila skôr, než napáchala škodu. Detail buď over v raw dátach, alebo sa opýtaj, či zmena sedí s tým, čo prospekt reálne zverejnil.

### 4. Over hook a pošli
**Pravidlo overenia (od 15.7.):** hook postavený na fakte (web down, mŕtva doména, chýbajúci košík) sa overuje **v deň odoslania** — research starne rýchlo (15.6. → 15.7. zomreli 3 z 5 hookov). Povel Claudovi: „over batch". Potom pošli, prepni `status: osloveny` a doplň `datum_oslovenia`.

### 5. Follow-up (3–5 dní bez reakcie na otvárač)
Použi follow-up prompt z Outreach_System (Krok 3): vlož pôvodnú správu + poznámku. Pravidlá: neopakuj sa, pridaj novú hodnotu (iný postreh/pain point), buď kratší, žiadne pasívno-agresívne "len sa uisťujem". Stále bez pitchu — predávaš až po reakcii.

## Princípy z Origami playbooku (0→$10k MRR len cez cold email)

Zdroj: [[document-origami|document-origami]]. Najdôležitejšie poznatky aplikovateľné na náš systém:

**Písanie emailu:**
- **5–8 viet max** — 70 %+ emailov sa číta na mobile; správa sa musí zmestiť na jednu obrazovku.
- **Max 2 vety bez zalomenia riadku** — ľudia skenujú, nie čítajú.
- **Nikdy nehovor o feature svojej služby** — hovor o ich firme a ich pain pointe; „pritlač na ranu", nech je problém cítiť. (Toto potvrdzuje náš dvojfázový prístup.)
- **Buď priamy** — netrikuj ľudí na call; chceš len tých, čo môžu reálne kúpiť.
- Slabší CTA = viac odpovedí, keď response rate viazne: „Môžem ti poslať pár postrehov, ako by sa to dalo vyriešiť?" namiesto „skočíme na call?".

**Očakávania a čísla (kalibrácia pre našu 1. vlnu):**
- Špičkový výsledok je **~5 % response rate** — čiže z 20 mailov čakaj realisticky **1 odpoveď**. Nie je to zlyhanie, je to norma.
- Dôsledok: 20 mailov je dobrý štart na otestovanie správ, ale na reálne výsledky treba rátať s desiatkami až stovkami. Origami posielalo 50–75/deň.
- **ICP (ideálny zákaznícky profil) rozhoduje viac než text správy** — „ak toto spravíš dobre, môžeš pokaziť všetko ostatné a aj tak uspieť". Pre cart.design: definovať presne, aký typ eshopu/značky oslovujeme (viď pipeline).
- **Iteračná slučka:** po každej odpovedi/calle uprav targeting aj správu. Dáta z [[cold-outreach-pipeline]] sú presne na toto.

**Na calle (keď sa dostaneš tak ďaleko):**
- 90 % času sa pýtaj na ich problémy, nepredvádzaj produkt. Demo až na druhom calle.
- Zisti, ktorá časť tvojho riešenia ich zaujala — tú rozviň.
- Close otázka: „Ak by sme vyriešili [ich problém], boli by ste ochotní za to zaplatiť X?"
- Prvé dealy môžeš poistiť garanciou vrátenia peňazí.

## Poznámky k raw súborom

- **Outreach_System.md** je hlavný zdroj — obsahuje SK master prompt, follow-up prompt aj vyplnený vzor poznámky (Jana Kováčová / Domáce Sviečky JK), ktorý sa oplatí pozrieť pred prvým použitím.
- **prompt-ai.md** je anglická duplicitná verzia master promptu — neprináša nič navyše; používaj SK verziu z Outreach_System. (Ponechané v raw, len na vedomie.)
- **Prospect_Template.md** (`cold-outreach-system/templates/`) je pracovná šablóna — kopíruj do `cold-outreach-clients/`, needituj originál.
- **document-origami.md** — Origami cold email playbook (syntéza vyššie).
- Odporúčaná Dataview query a tagy sú v Outreach_System (sekcia Tipy) — voliteľné, na začiatok stačí frontmatter `status`.

## Nastavenie vo vaulte

- **Metadata Menu** plugin → dropdown polia pre frontmatter prospect poznámok.
- Templater sa nepodarilo rozbehnúť (2026-07-15) — `datum_oslovenia` sa píše ručne; tracking dátumov rieši [[cold-outreach-pipeline]].

## Zdroje

- [[Outreach_System|Outreach_System.md]]
- [[Prospect_Template|Prospect_Template.md]]
- [[prompt-ai|prompt-ai.md]]
- [[document-origami|document-origami.md]]


Úplne vám rozumiem a presne preto za nami klienti chodia. Nefungujeme ako typické agentúry, ktoré vám vyfakturujú 50 € len za to, že na webe 'posunuli tlačidlo'.

Radšej navrhujeme férovú spoluprácu: 1 fixná suma a žiadne skryté poplatky. Ak s nami do toho pôjdete a nový e-shop alebo web vám nezarobí na svoje náklady a neprinesie profit, jednoducho nám neplatíte nič.

Sme síce na začiatku, no máme naozaj kvalitné produkty, ktoré predávajú samy. Mesačne za ne nepýtame sumu na úrovni nájmu za 3-izbový byt – cena vyjde približne ako dva lístky (napr na vas workshop) na mesiac. Žiadne tisíce eur vopred s neistým výsledkom