---
type: project
status: active
created: 2026-07-15
updated: 2026-07-20
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
| [[rebecca-d-enamel|Rebecca D Enamel]] | IG DM | brand-first: micromosaic remeslo | 2026-07-15 | — | **2026-07-16** — „renovujem práve web"; 20.7. len lajk bez odpovede | **vlákno na pauze** — manžel stavia web sám, nepingovať skoro |
| [[hazel-hand-engraving|Hazel Hand Engraving]] | IG DM | brand-first: hand-push engraving | 2026-07-15 | — | **2026-07-15** — nič nepredáva (free YouTube) | **reagovala — nekvalifikovaná**, slušne uzavrieť; sekundárny lead @firestonefinejewelry |
| Jake Newell | IG DM | brand-first: backlog "not accepting work" | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| DoubleK Custom Leathercraft | IG DM | brand-first: niche remeslo (tack) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Optimistic Soap | IG DM | brand-first: 229K obdiv (prerobené) | 2026-07-15 | — | **2026-07-15** — dlhá, otvorená; sama: rok „prechádza" na Shopify, platí double hosting, Wix billing bug | **reagovala** — pitch zdvorilo odmietla („too many choices"), push follow-up s call CTA poslaný 15.7. ([[optimistic-soap]]) |
| saint.jewellry | IG DM | spiaci účet + sashe 0/81 | 2026-07-15 | — | **2026-07-15** — pýta fotku šperku | **reagovala** — fáza 2 poslaná ([[outreach-batch-3]]) |
| darcekove_kytice | IG DM | DM objednávkový chaos | 2026-07-15 | — | 2026-07-15 — pitch odmietnutý | **mŕtve** ([[outreach-batch-3]]) |
| handmadebyluvela | IG DM | obsah bez predajného miesta | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-3]]) |
| badynco | IG DM | zľavy bez dosahu | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-3]]) |
| [[sperky-richterova|sperkyrichterovahandmade]] | IG DM | zákazková tvorba bez katalógu | 2026-07-15 | — | **2026-07-15** — ako zákazníkovi (foto v pondelok 20.7.) | **reagovala** — priznanie treba pred pondelkom ([[sperky-richterova]]) |
| [[by-alisha|by_alisha.sk]] | IG DM | vlastný improvizovaný (predaj cez správy?) | 2026-07-15 | — | **2026-07-16** — cenová námietka: e-shop mala, 3–4k € znova nedá; fáza 3 poslaná: reframe (katalógový e-shop ≠ dopytový flow, mesačne bez setup fee) + videohovor 15–20 min | **fáza 3 poslaná** — čaka sa na videohovor ([[by-alisha]]) |
| AC keramika (Anna Čičková) | email | sashe 8/68 — dopyt > ponuka | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-4]]) |
| Umelecká keramika | email | svojpomocný web brzdí predaj | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-4]]) |
| Jupiter Oak Jewelry | IG DM | brand-first: moth šperky, 132K ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Wolf Ceramics | IG DM | brand-first: tím + restaurant collabs ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Melissa Weiss Pottery | IG DM | brand-first: vlastná hlina, newsletter sales ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Mila.jito Leather | IG DM | brand-first: waitlist do 2027 ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| RBD Pottery | IG DM | brand-first: restock 21.7. sellouts ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Mud Lowery | IG DM | brand-first: Native American striebro ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Lulu LaFortune | IG DM | brand-first: Vogue press, Discord v bio ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Workaday Handmade | IG DM | brand-first: NY tableware ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Janel Foo Glassworks | IG DM | brand-first: Martha Stewart press ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Sacha Carlos-Raps | IG DM | brand-first: custom glass interiors ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Yuzu Pottery | IG DM | tech-first: bio Etsy vs. "restock on my website" ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| LOLiDE | IG DM | tech-first: lolide.com 521 down ✅16.7. 2× | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| [[gollik-knives|Gollik Knives (Jakub Golla)]] | IG DM | tech-first: .com nefunguje | 2026-07-16 | — | **2026-07-16** — .com kúpil niekto iný, jeho .cz nefunguje, robí custom orders | **reagoval** — CZ maker! Rapport otázka (CZ/SK) odoslaná 16.7., follow-up pripravený ([[gollik-knives]]) |
| Brit McDaniel (ex Paper & Clay) | IG DM | tech-first: stará doména timeoutuje po rebrande ✅16.7. 2× | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Callahan Ceramics | IG DM | tech-first: bio "next release: 2025 tbd" (spiaci) ✅16.7. | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| Beanpole Pottery | IG DM | tech-first: web timeout + predaj len emailom ✅16.7. 2× | 2026-07-16 | — | — | **oslovený** ([[outreach-batch-6]]) |
| [[nino-rostomashvili|Nino Rostomashvili]] | email | brand-first: cloisonné enamel niche, enamel-arts.com dead-DNS ✅potvrdené | 2026-07-16 | 2026-07-20 (oddelenie poštovného + ponuka prepočtu marže) | **2026-07-20** — „Many Thanks. Will think about this." (2× soft-close) | **nurture** — ďalší push zastavený, re-touch ~09/2026 len s novým dôvodom ([[nino-rostomashvili]]) |
| Raina Nicole Woodworks | IG DM | brand-first: 248K IG, Makita/BRUNT partnerstvá, web bez shopu ✅20.7. | — | — | — | **pripravený** ([[outreach-batch-7]]) |
| Doucette and Wolfe (Matthew Wolfe) | IG DM | brand-first: „museum quality", starý statický web bez cart ✅20.7. | — | — | — | **pripravený** ([[outreach-batch-7]]) |
| Chuck Richards Knives | IG DM | brand-first: 116K, Wix + 7× sold out ✅20.7. | 2026-07-20 | 2026-07-20 | odpísal ako predajca („FreeBird is on sale, available in all options") | **reagoval** → [[chuck-richards-knives]]; fáza 2 (poznanie+reframe) odoslaná 20.7., čaká sa na odpoveď ⚠️nože |
| Nick Anger (@angerknives) | IG DM | brand-first: 107K, žiadny web ani link v bio ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| RAD Knives (Collin) | IG DM | brand-first: 59K, 16× sold out ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Lew Griffin | IG DM | brand-first: 58K/85 postov, Shopify OK (redesign-grade) ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Ilya Alekseyev (@slavicsmith) | IG DM | brand-first: 47K, žiadny link, všetko cez DM ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| OOAK Forge | IG DM | brand-first: 28K, „No Custom Orders!" + prázdny shop ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Crimson Knife Co | IG DM | brand-first: 25K, 20 z 20 položiek sold out ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Iron Grove Tool Co (Daniel Collier) | IG DM | brand-first: 16K, doména bez DNS, bio → cudzí článok ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Nanda Knives (Nick Anderson) | IG DM | brand-first: 13K, 1 produkt + „DM for inquiries" ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Dark Timber Customs (Peter Kohler) | IG DM | brand-first: 11.5K, žiadny link v bio ✅20.7. | — | — | — | **⚠️ nedoručené** — účet blokuje DM od cudzích, treba iný kanál ([[outreach-batch-8]]) ⚠️nože |
| MorrisonMade Leather | IG DM | brand-first: 169K, vlastný shop utopený v partnerskom linktree ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Odin Leather Goods | IG DM | brand-first: 82K, bio linkuje blog namiesto shopu ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| DS Leather Goods (Deyan) | IG DM | brand-first: 82K, Etsy-dependent (117 krajín) ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Girty Leather Co (Ethan Girty) | IG DM | brand-first: 71K, „custom orders open" + 10× sold out ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Nerb Handcrafted | IG DM | brand-first: 69K, v bio len gmail ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Luava (FI) | IG DM | brand-first: 51K, Shopify OK (redesign-grade) ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Foolish Pride Leather Craft | IG DM | brand-first: 43K, Wix web nezodpovedá brandu ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Lord Leathercraft (Geoffrey) | IG DM | brand-first: 37K, produkty v Notione namiesto eshopu ✅20.7. | — | — | — | **⚠️ nedoručené** — účet blokuje DM od cudzích, treba iný kanál ([[outreach-batch-8]]) |
| Orox Leather Co | IG DM | brand-first: 18K, 4. generácia od 1933, príbeh chýba na webe ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| The Local Branch | IG DM | brand-first: 9.8K (⚠️pod prahom), Shopify + kamenná predajňa ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) |
| Pekne (pekne.eu) | IG DM | kombinovaná správa: 111 script tagov, pomalý mobile load ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-9]]) — ICP v2 |
| Hevi (hevisleep.sk/.cz) | email | kombinovaná správa: dva samostatné SK/CZ Shopify obchody ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-9]]) — ICP v2 |
| [[gudslip|Gudslip (gudslip.cz)]] | email | kombinovaná správa: spotrebný tovar bez predplatného ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[gudslip]] — projekt, [[outreach-batch-9]] — batch) — ICP v2 |
| Resty (feelresty.com) | IG DM | kombinovaná správa: refilly bez predplatného ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-9]]) — ICP v2 |
| Tatramodel (tatramodel.sk) | email | žiadny `<meta viewport>` — web nemá mobilnú verziu ✅20.7. | — | — | — | **pripravený** ([[outreach-batch-10]]) — zastarané SK e-shopy |
| Vcelo (vcelo.sk) | email | 3.7–4.2 s načítanie na mobile, 4 merania ✅20.7. | — | — | — | **pripravený** ([[outreach-batch-10]]) |
| Konvička (konvicka.sk) | email | 2.3–4.2 s na mobile, kolísavé ✅20.7. | — | — | — | **pripravený** ([[outreach-batch-10]]) |
| Neoprot (neoprot.sk) | email | 2.4–2.7 s na mobile ✅20.7. | — | — | — | **⏸️ pozdržaný** — možno nepredáva online ([[outreach-batch-10]]) |

### Cart Leads databáza (38 leadov, US/EN trh)

Zdroj: `raw/cart.design/cold-outreach/Cart Leads - Sheet1.csv` (k 2026-06-15, importované 2026-07-15). Handmade makers (koža, šperky, sviečky, mydlo, nože) so silným publikom a rozbitým/chýbajúcim eshopom — presne náš ICP. CSV už obsahuje research (followers, stav webu, uhol) aj delenie owner: Marek/Adam.

**⚠️ Časovo kritické:** Shannon Steel Labs — doména expiruje **20. 7. 2026** (o 5 dní); ~~Gollik Knives — expiruje 2. 8. 2026~~ (k 16.7. už .com kúpil niekto iný — CSV odhad bol stale; lead ale reagoval, pozri [[gollik-knives]]). Uhol „domain rescue" funguje len pred expiráciou — Gollik je dôkaz, že squatteri sú rýchli.

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

## Nová línia — ICP v2: DTC značky SK/CZ (2026-07-20)

Prvý **druhý ICP**, nie ďalšia niche. Doteraz všetkých 8 batchov cielilo na handmade makerov
s **rozbitým** kanálom; ICP v2 cieli na mladé DTC značky s **funkčným** Shopify e-shopom, ktorý
ich brzdí (šablóna, app tax, rýchlosť). Iný hook, iná persóna, iný grade (redesign/retainer).
Definícia, kvalifikačné prahy a research infra: [[icp-dtc-znacky-sk-cz]]. **20.7. odoslané všetky 4 leady** ([[outreach-batch-9]]: Pekne, Hevi, Gudslip, Resty) — variant B, kombinovaná správa (rapport + technický nález + ponuka + CTA v jednej správe, podľa reálneho precedensu Nosky).

**Poznatok #7 — overiť, čo lead reálne predáva, skôr než sa postaví kategória.** Marko navrhol
nosky.cz a pekne.eu ako „pekné SK dizajnové značky". Overenie (`curl` + `/products.json`) ukázalo,
že ide o **priamych konkurentov v nike nosných pások / biohackingu**, nie o dizajnové značky.
Spoločným menovateľom nebola estetika, ale **obchodný model** (1 hero produkt + digitálne doplnky
+ IG/TikTok marketing) — a to je použiteľné na targeting, kým „pekné značky" nie je.

**Poznatok #8 — platforma a výkon sa dajú kvalifikovať zadarmo.** `curl` + `grep` zistí platformu,
čas odozvy, počet scriptov, `<title>`, `hreflang`; `/products.json` vráti celý Shopify katalóg bez
API kľúča. Firecrawl a Kimi WebBridge treba až na discovery a IG verifikáciu → výrazná úspora usage.

## Nová línia — zastarané SK e-shopy (2026-07-20)

Tretia cieľová skupina popri ICP v1 (handmade makeri s rozbitým kanálom) a ICP v2 (DTC značky
s funkčným Shopify). Cieľ: **etablované SK firmy s reálnym obratom a objektívne zastaraným webom**
— redesign grade, kanál email. Metodika je celá zadarmo (Python/`curl`), Firecrawl len na discovery.
Preverených ~50 domén, kvalifikovaní 4. Detaily: [[outreach-batch-10]].

**Poznatok #9 — technicky rozbitý web ešte neznamená biznis.** `rybarskepotreby-poprad.sk` mal
najlepší technický profil dávky (neplatný SSL + žiadny viewport), ale bol to **SEO satelit**
odkazujúci na iné e-shopy toho istého prevádzkovateľa. Rozšírenie poznatku #5: kontrolovať
**odchádzajúce odkazy** — ak web vedie hlavne inam, je to doorway page, nie obchod.

**Poznatok #10 — platformový boilerplate nie je nález.** jQuery 1.11.3 sa objavilo na 12 weboch
v dávke — na všetkých Shoptet, lebo je to default platformy. Pred použitím technického detailu
ako hooku overiť, či nejde o vlastnosť platformy, ktorú má rovnako každý jej zákazník.

**Poznatok #11 — rýchlosť merať 4×, inak klame.** `e-luma.sk` (3.11 s) a `ortokomplet.sk` (1.51 s)
prešli prahom pri prvom meraní a pri opakovaní spadli na 0.53 / 0.63 s — oba vyradené. Použiť
len konzistentne pomalé weby. (Zovšeobecnenie výkyvu, ktorý sme videli pri `pekne.eu`.)

## Nová niche — nože + koža (2026-07-20)

Druhá nová niche v ten istý deň. Firecrawl discovery (9 queries, 47 kandidátov) + Kimi WebBridge verifikácia →
**20 kvalifikovaných (~43 % strike rate)** — výrazne lepšie než drevo. Kľúčový poznatok: nože a koža majú
**opačný problém**. Nože majú eshop, ktorý je vypredaný (demand leak), koža má funkčný eshop, ktorý je
schovaný (bio vedie na blog/linktree/Notion namiesto shopu). Detaily: [[outreach-batch-8]].

**Poznatok #5 — spiaci účet nie je lead.** @margigaba mala ideálny technický profil (15.7K followers +
doména úplne bez DNS), ale posledný príspevok z 2021. Mŕtva doména bez živého dopytu je bezcenná →
do kvalifikácie pridať kontrolu **dátumu posledného postu**, nielen followers + stav webu.

**Poznatok #6 — Firecrawl instagram.com nescrapuje** („we do not support this site"). Discovery cez
Firecrawl search funguje (profily sa dajú vyťažiť z URL aj z `@mentions` v snippetoch), ale všetky
followers/bio dáta musia ísť cez Kimi WebBridge. Pri ďalších dávkach rátať s týmto rozdelením.

## Nová niche — drevo/nábytok (2026-07-20)

Prvý test mimo doterajších niší (koža, šperky, sviečky, mydlo, keramika/sklo, nože), na Markov povel. Firecrawl discovery + Kimi WebBridge verifikácia priniesli 2 kvalifikovaných z ~20 preverených — nižší strike rate než pri koži/šperkách (remeselníci v tejto nise skôr vôbec nemajú e-shop, nie rozbitú doménu). Detaily: [[outreach-batch-7]].

## Zdroje

- [[cold-outreach-manual]] — postup, prompty
- `raw/cart.design/cold-outreach-clients/` — research poznámky jednotlivých prospektov
- `raw/cart.design/cold-outreach-system/` — šablóna, master prompty
- `raw/cart.design/cold-outreach/ig-sk-leads-2026-07-15.md` — SK Instagram leady bez e-shopu (Firecrawl + Kimi WebBridge)
- `raw/cart.design/cold-outreach/firecrawl-test-batch-2026-07-15.csv` — test dávka SK e-shopov cez Firecrawl (väčšinou aktívne e-shopy, nie cieľový ICP)
