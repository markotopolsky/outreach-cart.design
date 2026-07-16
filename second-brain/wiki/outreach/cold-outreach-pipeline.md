---
type: project
status: active
created: 2026-07-15
updated: 2026-07-16
aliases: [Outreach pipeline, Cold outreach pipeline]
tags: [cart-design, cold-outreach, sales]
---

# Cold outreach pipeline (cart.design)

Centrálny prehľad všetkých prospektov. Cieľ prvej vlny: **~20 mailov**, zber dát o tom, čo funguje. Postup pre jednotlivý prospekt: [[cold-outreach-manual]].

## Ako s týmto pracovať (Marko ↔ Claude)

1. **Marko:** nová firma → vytvor `raw/cart.design/cold-outreach-clients/<firma>-raw.md` (kópia [[Prospect_Template|šablóny]]), vyplň čo vieš.
2. **Claude** (na povel "sprav <firma>"): prečíta raw, navrhne otvárač (subject + správa), založí/doplní wiki stránku, pridá riadok do tabuľky nižšie.
3. **Marko:** pošle mail → povie "poslané" → Claude updatne status + dátum.
4. **Odpoveď od klienta:** Marko vloží ich odpoveď → Claude navrhne fázu 2 (pitch).
5. **Follow-upy:** Claude stráži dátumy — pri otázke "čo mám dnes robiť" vypíše, komu treba follow-up (3–5 dní bez reakcie).

## Pipeline

### Aktívne rozpracované

| Prospekt | Kanál | Hook (typ) | Oslovený | Follow-up | Reakcia | Stav |
|---|---|---|---|---|---|---|
| [[biorythme]] | email | pain point (objednávanie) | — | — | — | správa pripravená, čaká na odoslanie |
| LadyBuQ Art | IG DM | mŕtva doména + Etsy sales ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| Jenny Topolski | email | web 403 + Etsy-dependent ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| iamrachel | IG DM | mŕtva .com + Etsy ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| Creations That Rock | IG DM | web práve zomrel + 101K TT ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| Pierre Laborde | IG DM | demand leak (vypredané drops) ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| [[drop-dead-candles|Drop Dead Candles]] | IG DM | vlastný, Marko poslal priamo | 2026-07-15 | — | **2026-07-15** — „it should be working" | **reagovala** — hook nevyšiel (web k 16.7. reálne beží), treba záchrannú odpoveď |
| The Low Key Co | IG DM | tech-first: doména parkovaná ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| [[sweet-nothings-studios|Sweet Nothings Studios]] | IG DM | tech-first: web timeout ✅15.7. | 2026-07-15 | — | **2026-07-15** — „shop is up and running" | **reagovala** — 16.7. nájdený reálny problém (apex SSL), odpoveď s diagnózou pripraviť |
| Forest Nine | IG DM | tech-first: password-locked ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Miners Ink | IG DM | tech-first: mŕtva DNS ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Kamari Candle Co | IG DM | tech-first: web stale od 2022 ✅15.7. (prerobené) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Macrame on the Move | IG DM | tech-first: skúsenosť na cestách (prerobené) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| [[disciple-designed|Disciple Designed]] | IG DM | vlastný (Marko): challenging question na pricing gap | 2026-06-18 | pripravený (15.7.) | **2026-06-19** — otvorená, vecná | **reagoval** — follow-up pripravený |
| [[rebecca-d-enamel|Rebecca D Enamel]] | IG DM | brand-first: micromosaic remeslo | 2026-07-15 | — | **2026-07-16** — „renovujem práve web" | **reagovala** — najlepší timing signál, odpoveď pripraviť |
| [[hazel-hand-engraving|Hazel Hand Engraving]] | IG DM | brand-first: hand-push engraving | 2026-07-15 | — | **2026-07-15** — nič nepredáva (free YouTube) | **reagovala — nekvalifikovaná**, slušne uzavrieť; sekundárny lead @firestonefinejewelry |
| Jake Newell | IG DM | brand-first: backlog "not accepting work" | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| DoubleK Custom Leathercraft | IG DM | brand-first: niche remeslo (tack) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Optimistic Soap | IG DM | brand-first: 229K obdiv (prerobené) | 2026-07-15 | — | **2026-07-15** — dlhá, otvorená; sama: rok „prechádza" na Shopify, platí double hosting, Wix billing bug | **reagovala** — pitch zdvorilo odmietla („too many choices"), push follow-up s call CTA poslaný 15.7. ([[optimistic-soap]]) |
| saint.jewellry | IG DM | spiaci účet + sashe 0/81 | 2026-07-15 | — | **2026-07-15** — pýta fotku šperku | **reagovala** — fáza 2 poslaná ([[outreach-batch-3]]) |
| darcekove_kytice | IG DM | DM objednávkový chaos | 2026-07-15 | — | 2026-07-15 — pitch odmietnutý | **mŕtve** ([[outreach-batch-3]]) |
| handmadebyluvela | IG DM | obsah bez predajného miesta | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-3]]) |
| badynco | IG DM | zľavy bez dosahu | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-3]]) |
| [[sperky-richterova|sperkyrichterovahandmade]] | IG DM | zákazková tvorba bez katalógu | 2026-07-15 | — | **2026-07-15** — ako zákazníkovi (foto v pondelok 20.7.) | **reagovala** — priznanie treba pred pondelkom ([[sperky-richterova]]) |
| [[by-alisha|by_alisha.sk]] | IG DM | vlastný improvizovaný (predaj cez správy?) | 2026-07-15 | — | **2026-07-16** — cenová námietka: e-shop mala, 3–4k € znova nedá | **reagovala — cenová námietka** (kotva na starú zlú investíciu, nie odmietnutie); ďalší krok: reframe ([[by-alisha]]) |
| AC keramika (Anna Čičková) | email | sashe 8/68 — dopyt > ponuka | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-4]]) |
| Umelecká keramika | email | svojpomocný web brzdí predaj | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-4]]) |

### Cart Leads databáza (38 leadov, US/EN trh)

Zdroj: `raw/cart.design/cold-outreach/Cart Leads - Sheet1.csv` (k 2026-06-15, importované 2026-07-15). Handmade makers (koža, šperky, sviečky, mydlo, nože) so silným publikom a rozbitým/chýbajúcim eshopom — presne náš ICP. CSV už obsahuje research (followers, stav webu, uhol) aj delenie owner: Marek/Adam.

**⚠️ Časovo kritické:** Shannon Steel Labs — doména expiruje **20. 7. 2026** (o 5 dní); Gollik Knives — expiruje 2. 8. 2026. Uhol „domain rescue" funguje len pred expiráciou.

**Tier 1 — obrovské publikum, rozbitý predaj (poslať prvých):**

| Lead | Niche | Publikum | Problém | Uhol |
|---|---|---|---|---|
| Optimistic Soap | mydlo | 229K IG | Wix bez košíka — nevie predávať na vlastnom webe | escape Etsy / vlastný store |
| Pierre Laborde | koža | 115K IG + NYT press | drops vypredané za 30 min, web zanedbaný (Squarespace) | own your customers |
| Drop Dead Candles | sviečky | 12K IG + Etsy top 1 % | vlastný web NEFUNGUJE (timeout) | „tvoj web je down" |
| LadyBuQ Art | koža | 8,7K Etsy sales | vlastná .com MŔTVA (DNS) | „tvoja doména je mŕtva" |
| Kamari Candle Co | sviečky | 35,9K TikTok + sellouts | GoDaddy web bez košíka, stale 2022 | „tvoj store nevie predávať" |
| Natalia Dlugopolski | šperky | 101K TikTok | Squarespace len portfólio, bez košíka | prvý ozajstný store |
| Hazel Hand Engraving | šperky | 76K IG | Shopify predáva len kurzy, šperky cez DM | commission store |
| Jake Newell | šperky | 32,9K IG | žiadny web, backlog „not accepting work" | waitlist/commission store |
| iamrachel | šperky | 7,9K IG + 5,1K Etsy | .com mŕtva, Etsy-dependent | escape Etsy |
| Forest Nine | koža | 36K IG + 44,7K Etsy sales | store ambiguous (password-lock?) | escape Etsy |
| Disciple Designed | koža | 466K IG + 441K TT | 6–8 mes. backlog, prerástli Squarespace | redesign/scale (možno majú ľudí — screen) |
| Jenny Topolski | šperky | 6,2K Etsy sales, 5★ | web 403, Etsy-dependent — „core ICP" | escape Etsy (email) |

**Tier 2 — stredné publikum / redesign grade:** Rebecca D Enamel (73K, redesign), Sweet Nothings (25,4K, BigCartel), The Low Key Co (20,8K), Pam Farren, Lois/Hampton Gem, Lobo Gun Leather, Nino Rostomashvili, Macrame on the Move, DoubleK, Sharp & Fiery, Jamie Noelle, Miners Ink.

**Tier 3 — nože (HIGH-RISK platby — Stripe nože nemusí pustiť, treba overiť processor pred pitchom):** Hanson Knives (32K), REK Knives (14K), Ban Tang (12K), Chipped Metal (6,7K), Jason Fry (referral node — Guild president!), Mad Science Forge, Daniel Fairly, Shannon Steel Labs (⚠️ 20.7.), Jarrett Fleming, Redmeadow, Gersh Blades, CPE, Frazier, Siegle, Gollik (⚠️ 2.8.).

**Poznámky k databáze:**
- Jazyk oslovovania: **EN** (US/UK/CA trh) — na rozdiel od biorythme (SK).
- CSV má vlastné openery A/C a „week-2 batch" plán — pri generovaní správ rešpektovať stĺpce `approach` a `next action`.
- Owner stĺpec: časť leadov patrí Adamovi/Marekovi — s Markom si rozdeliť, kto posiela komu.

**Stav k 2026-07-16:** 18/39 leadov z CSV už oslovených ([[outreach-batch-1]] + [[outreach-batch-2]], niektorí reagovali — pozri tabuľku vyššie). Zvyšných **21 nekontaktovaných** má pripravené otváracie správy v [[outreach-batch-5]] (6 non-knife + 15 knife makerov, knife ⚠️ vyžaduje overenie platobného procesora pred odoslaním — HIGH-RISK).

**Stavy:** `pripravuje sa` → `správa pripravená` → `oslovený` → `follow-up poslaný` → `reagoval` → `pitch poslaný` → `stretnutie` → `klient` / `mŕtve`

## SK trh — Instagram leady bez e-shopu (2026-07-15)

Nová línia: slovenskí remeselníci/tvorcovia, ktorí predávajú **len cez Instagram/sociálne siete** (žiadny vlastný e-shop). Metóda: Firecrawl `site:instagram.com` search na kľúčové slová (rýchlejšie objavovanie ako hashtag crawling — hashtagy vracajú ~70-80% irelevantných postov) → Kimi WebBridge (prihlásený browser) overil bio/link-in-bio každého kandidáta.

**Dôležité zistenie:** Firecrawl web search na "slovenské e-shopy remeslo/handmade" (bez `site:instagram.com`) väčšinou nájde firmy, ktoré **e-shop už majú** — Google indexuje existujúce weby, takže čisto sociálni predajcovia sú týmto kanálom neviditeľní. Test dávka 29 SK e-shopov cez Firecrawl priniesla len 1-2 jasných "bez e-shopu" kandidátov (viď `firecrawl-test-batch-2026-07-15.csv`).

**Kvalifikovaní leadi (žiadny vlastný e-shop):**

| Lead | Niche | Followers | Prečo je dobrý lead |
|---|---|---|---|
| by_alisha.sk | šperky | 25.3K | Link v bio = objednávkový formulár (tally.so), nie e-shop; objednávky cez DM — najväčšie publikum z dávky |
| darcekove_kytice | darčekové kytice | 2,133 | Link vedie na Facebook profil namiesto e-shopu; aktívne "SKLADOM" príspevky |
| saint.jewellry | šperky | 1,424 | Predáva cez sashe.sk (marketplace), nie vlastnú doménu; platba prevodom, objednávka v správe |
| sperkyrichterovahandmade | šperky (Swarovski) | 439 | Len fyzická adresa ateliéru v bio, žiadny web |
| mc_remeselnik | remeselné služby | 367 | Iná kategória (služby nie produkty), žiadny web vôbec |
| badynco | prírodná kozmetika | 262 | Bio: "Info/order DM", žiadny web link |
| handmadebyluvela | autorské šperky | 47 | Jediný externý odkaz = Threads, žiadny e-shop |

Detaily, metodika a zoznam overených-ale-vylúčených (majú e-shop) v `raw/cart.design/cold-outreach/ig-sk-leads-2026-07-15.md`.

**→ Otvárače pripravené (15.7.):** [[outreach-batch-3]] — 6 SK správ s overenými hookmi z postov/komentárov (by_alisha 8× "cena prosím?" pod postom; darcekove_kytice DM chaos; atď.). mc_remeselnik vyradený — služby, nie produkty → merge.build ICP.

## Kalibrácia očakávaní (z Origami playbooku)

Špičkový cold email má **~5 % response rate** → z 20 mailov čakaj **~1 odpoveď**. Prvá vlna 20 mailov je test správ a targetingu, nie zdroj klientov — na reálne výsledky treba desiatky až stovky mailov. Detaily: [[cold-outreach-manual]] (sekcia Origami).

## ICP v1 (definované 2026-07-15, podľa Origami step 1)

**Firma:** solo/malý handmade maker (koža, šperky, sviečky, mydlo; nože = high-risk platby, overiť processor). US/UK/CA trh (+ CZ/SK ako biorythme).

**Preukázaný dopyt (aspoň 1):** 10K+ followers · 1K+ Etsy sales · sellout drops / backlog / „not accepting orders".

**Rozbitý predajný kanál (aspoň 1):** mŕtva doména / web down · web bez košíka · Etsy-dependent (vlastný web nefunkčný) · predaj len cez DM.

**Persóna:** majiteľ/ka = tvár značky, rozhoduje sám/sama, remeselník nie technik, topí sa v operatíve (DM objednávky, restocky).

**Logika správy z ICP:** tvoj dopyt je reálny (uznanie) → tvoj kanál ho nezvláda (postreh) → otázka. Ak lead nesedí na ICP, nedostane správu.

**Iterácia:** ICP nie je finálny — po 1. vlne (~20 správ) spresniť podľa toho, kto reálne odpovedal (niche? typ problému? veľkosť?). Origami: "It's okay if this is completely wrong."

## Zber dát (vyhodnotenie po ~20 mailoch)

Po prvej vlne vyhodnotíme:
- **Response rate: tech-first vs. brand-first** (test bežiaci od [[outreach-batch-2]], 6 vs. 6 + [[outreach-batch-1]] ako referenčné tech-first)
- **Response rate podľa hooku** — pain point vs. osobný/obdivný hook
- **Response rate podľa kanála** — email vs. IG DM vs. WhatsApp
- **Response rate podľa typu klienta** — lokálny biznis / online značka / zastaraný eshop / nový biznis
- Čas do odpovede; či follow-up niečo zachránil

Výsledky sa zapíšu sem a premietnu do [[cold-outreach-manual]].

### Dáta k 2026-07-16 ráno (IG inbox prepis `ig-status167`)

**Celkové skóre po ~20 hodinách:** EN 5/18 reakcií (28 %) · SK IG 4/6 (67 %) · SK email 0/2. Obe čísla vysoko nad Origami benchmarkom ~5 % — hyper-personalizované hooky fungujú, vzorka stále malá.

**Experiment tech-first vs. brand-first (priebežne):** brand-first **3/6** (Optimistic, Rebecca, Hazel) vs. tech-first **1/6** (Sweet Nothings) + batch 1 tech-štýl 0/5. Brand-first zatiaľ jasne vedie — ale pozor, 2 z reakcií (Hazel nekvalifikovaná, Optimistic odmietla) zatiaľ nekonvertujú. Vyhodnotiť po týždni.

**Poznatok #4 — hook „tvoj web nefunguje" má krátku trvanlivosť a majiteľ ho vie „vyvrátiť":** Drop Dead Candles aj Sweet Nothings odpovedali „funguje mi to, skús refresh" — majiteľ si web otvorí (z bookmarku/www) a hook pôsobí ako omyl. Drop Dead: web k 16.7. reálne beží (výpadok bol zrejme dočasný — curl 200). Sweet Nothings: problém je reálny, ale iný než tvrdil otvárač — **apex doména bez SSL certifikátu** (bez www padá https). Pravidlá: (a) site-down hook overiť tesne pred odoslaním, nie deň vopred z CSV; (b) pomenovať **presný failure mode** („bez www to hádže security error"), nie všeobecné „nenačíta sa" — presná diagnóza sa nedá odbiť refreshom a buduje kredibilitu; (c) na „works for me" odpoveď mať pripravenú záchranu: buď presnú diagnózu, alebo čestné „už to ide, asi som to trafil v zlom momente" + pivot.

### Prvé dáta z SK batch 3 (k 2026-07-15)

**Vzorka:** 3 odoslané otvárače, 2 reakcie v prvý deň (saint.jewellry, darcekove_kytice) — SK trh reaguje výrazne nad Origami benchmarkom (~5 %). Malá vzorka, ale hyper-personalizované hooky (konkrétny post/komentár) na nesaturovanom SK trhu vyzerajú ako silná kombinácia.

**Poznatok #1 — akútnosť pain pointu rastie s objemom dopytu:** darcekove_kytice (2.1K followers) na otvárač reagovala okamžite, ale pitch odmietla ("nie nepotrebujem") — pri jej objeme jej ručné DM vybavovanie reálne stačí. Dôsledok pre ICP: uprednostniť leady, kde je **viditeľný dôkaz nestíhania** (nezodpovedané "cena?" komenty, backlog, vypredané bez doplnenia), pred malými účtami, kde DM proces funguje. "Nemá e-shop" sám o sebe nie je pain point.

**Poznatok #2 — otvárač ako od zákazníka má vedľajší efekt:** prospekt odpovie ako predajca zákazníkovi ("Máte záujem o kyticu?") a fáza 2 potom vyžaduje priznanie, ktoré môže pôsobiť ako bait-and-switch. Zvážiť pri ďalších otváračoch formuláciu, ktorá znie zvedavo, ale nie ako nákupný záujem.

**Poznatok #3 — ručné úpravy faktov sú riziko:** zámena detailu v správe (náhrdelník → prsteň pri saint.jewellry) takmer spôsobila konflikt s realitou, keď si prospekt vyžiadal dôkaz. Pravidlo zapísané v [[cold-outreach-manual]] §3c.

## Zdroje

- [[cold-outreach-manual]] — postup, prompty
- `raw/cart.design/cold-outreach-clients/` — research poznámky jednotlivých prospektov
- `raw/cart.design/cold-outreach-system/` — šablóna, master prompty
- `raw/cart.design/cold-outreach/ig-sk-leads-2026-07-15.md` — SK Instagram leady bez e-shopu (Firecrawl + Kimi WebBridge)
- `raw/cart.design/cold-outreach/firecrawl-test-batch-2026-07-15.csv` — test dávka SK e-shopov cez Firecrawl (väčšinou aktívne e-shopy, nie cieľový ICP)
