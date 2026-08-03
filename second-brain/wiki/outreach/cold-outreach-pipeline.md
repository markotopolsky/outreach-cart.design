---
type: project
status: active
created: 2026-07-15
updated: 2026-08-03
aliases: [Outreach pipeline, Cold outreach pipeline]
tags: [cart-design, cold-outreach, sales]
---

# Cold outreach pipeline (cart.design)

Centrálny prehľad všetkých prospektov. Cieľ prvej vlny: **~20 mailov**, zber dát o tom, čo funguje. Postup pre jednotlivý prospekt: [[cold-outreach-manual]].

> ⏸️ **K 2026-07-21 je cold outreach pozastavený** — žiadne nové otvárače, kým nebeží eval na promptoch.
> Živé vlákna v tabuľke nižšie pokračujú normálne. Sčítané čísla a stav na jednom mieste: [[dashboard]].

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
| [[wiki/projects/biorythme\|biorythme]] | email + IG DM | pain point (objednávanie) ✅15.7. | 2026-07-15 | **2026-08-03** (fáza 2, IG) | **2026-07-25** (IG) — potvrdila: custom platforma, každá zmena „hacking" | **fáza 2 odoslaná** — presunuté do `projects/` |
| LadyBuQ Art | IG DM | mŕtva doména + Etsy sales ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| Jenny Topolski | email | web 403 + Etsy-dependent ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| iamrachel | IG DM | mŕtva .com + Etsy ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| Creations That Rock | IG DM | web práve zomrel + 101K TT ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| Pierre Laborde | IG DM | demand leak (vypredané drops) ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-1]]) |
| [[wiki/projects/drop-dead-candles|Drop Dead Candles]] | IG DM | vlastný, Marko poslal priamo | 2026-07-15 | — | **2026-07-15** — „it should be working" | **reagovala** — hook nevyšiel (web k 16.7. reálne beží), treba záchrannú odpoveď |
| The Low Key Co | IG DM | tech-first: doména parkovaná ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| [[wiki/projects/sweet-nothings-studios|Sweet Nothings Studios]] | IG DM | tech-first: web timeout ✅15.7. | 2026-07-15 | — | **2026-07-15** — „shop is up and running" | **reagovala** — 16.7. nájdený reálny problém (apex SSL), odpoveď s diagnózou pripraviť |
| Forest Nine | IG DM | tech-first: password-locked ✅15.7. | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| [[wiki/projects/gems-of-california\|Miners Ink / Gems of California]] | IG DM | tech-first: mŕtva DNS ✅15.7. (teraz stale — opravil web) | 2026-07-15 | **2026-08-03** (fáza 2) | **2026-07-27** — web opravený, pop-upy skončil, focus na ťaženie + custom objednávky | **fáza 2 odoslaná** |
| Kamari Candle Co | IG DM | tech-first: web stale od 2022 ✅15.7. (prerobené) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Macrame on the Move | IG DM | tech-first: skúsenosť na cestách (prerobené) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| [[disciple-designed|Disciple Designed]] | IG DM | vlastný (Marko): challenging question na pricing gap | 2026-06-18 | pripravený (15.7.) | **2026-06-19** — otvorená, vecná | **reagoval** — follow-up pripravený |
| [[wiki/projects/rebecca-d-enamel|Rebecca D Enamel]] | IG DM | brand-first: micromosaic remeslo | 2026-07-15 | — | **2026-07-16** — „renovujem práve web"; 20.7. len lajk bez odpovede | **vlákno na pauze** — manžel stavia web sám, nepingovať skoro |
| [[wiki/projects/hazel-hand-engraving|Hazel Hand Engraving]] | IG DM | brand-first: hand-push engraving | 2026-07-15 | — | **2026-07-15** — nič nepredáva (free YouTube) | **reagovala — nekvalifikovaná**, slušne uzavrieť; sekundárny lead @firestonefinejewelry |
| Jake Newell | IG DM | brand-first: backlog "not accepting work" | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| DoubleK Custom Leathercraft | IG DM | brand-first: niche remeslo (tack) | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-2]]) |
| Optimistic Soap | IG DM | brand-first: 229K obdiv (prerobené) | 2026-07-15 | — | **2026-07-15** — dlhá, otvorená; sama: rok „prechádza" na Shopify, platí double hosting, Wix billing bug | **reagovala** — pitch zdvorilo odmietla („too many choices"), push follow-up s call CTA poslaný 15.7. ([[wiki/projects/optimistic-soap|optimistic-soap]]) |
| saint.jewellry | IG DM | spiaci účet + sashe 0/81 | 2026-07-15 | — | **2026-07-15** — pýta fotku šperku | **reagovala** — fáza 2 poslaná ([[outreach-batch-3]]) |
| darcekove_kytice | IG DM | DM objednávkový chaos | 2026-07-15 | — | 2026-07-15 — pitch odmietnutý | **mŕtve** ([[outreach-batch-3]]) |
| handmadebyluvela | IG DM | obsah bez predajného miesta | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-3]]) |
| badynco | IG DM | zľavy bez dosahu | 2026-07-15 | — | — | **oslovený** ([[outreach-batch-3]]) |
| [[wiki/projects/sperky-richterova|sperkyrichterovahandmade]] | IG DM | zákazková tvorba bez katalógu | 2026-07-15 | — | **2026-07-15** — ako zákazníkovi (foto v pondelok 20.7.) | **reagovala** — priznanie treba pred pondelkom ([[wiki/projects/sperky-richterova|sperky-richterova]]) |
| [[wiki/projects/by-alisha|by_alisha.sk]] | IG DM | vlastný improvizovaný (predaj cez správy?) | 2026-07-15 | — | **2026-07-16** — cenová námietka: e-shop mala, 3–4k € znova nedá; fáza 3 poslaná: reframe (katalógový e-shop ≠ dopytový flow, mesačne bez setup fee) + videohovor 15–20 min | **fáza 3 poslaná** — čaka sa na videohovor ([[wiki/projects/by-alisha|by-alisha]]) |
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
| [[nick-anger-knives\|Nick Anger (@angerknives)]] | IG DM | brand-first: 107K, žiadny web ani link v bio ✅20.7. | 2026-07-20 | — | **2026-07-21** — „Was there something you were interested in?" (ako predajca) | **reagoval** — priznanie + hook odoslaný 24.7. ([[nick-anger-knives]]) ⚠️nože |
| RAD Knives (Collin) | IG DM | brand-first: 59K, 16× sold out ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Lew Griffin | IG DM | brand-first: 58K/85 postov, Shopify OK (redesign-grade) ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Ilya Alekseyev (@slavicsmith) | IG DM | brand-first: 47K, žiadny link, všetko cez DM ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| OOAK Forge | IG DM | brand-first: 28K, „No Custom Orders!" + prázdny shop ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| Crimson Knife Co | IG DM | brand-first: 25K, 20 z 20 položiek sold out ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-8]]) ⚠️nože |
| [[iron-grove-tool-co\|Iron Grove Tool Co (Daniel Collier)]] | IG DM | brand-first: 16K, doména bez DNS, bio → cudzí článok ✅20.7. | 2026-07-20 | — | **2026-07-21** — web je iná doména (irongrovetoolcompany.com), funguje; hook mimo | **reagoval** — draft odpovede NEODOSLANÝ (čaká schválenie), slabší fit ([[iron-grove-tool-co]]) ⚠️nože |
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
| [[wiki/projects/orox-leather-co\|Orox Leather Co]] | IG DM | brand-first: 18K, 4. generácia od 1933, príbeh chýba na webe ✅20.7. | 2026-07-20 | **2026-08-03** (fáza 2) | **2026-07-25** — „small team, thank you we should integrate it more" | **fáza 2 odoslaná** |
| [[the-local-branch\|The Local Branch]] | IG DM | brand-first: 9.8K (⚠️pod prahom), Shopify + kamenná predajňa ✅20.7. | 2026-07-20 | — | **2026-07-22** — „mostly in person, online is a fraction" (Mackenzie) | **reagovala — slabý fit**; naša otázka na Seen, nepingovať ([[the-local-branch]]) |
| [[wiki/projects/pekne\|Pekne (pekne.eu)]] | IG DM + email | kombinovaná správa: 111 script tagov, pomalý mobile load ✅20.7. | 2026-07-20 | — | **2026-07-20** (email) — „zatiaľ nebudeme potrebovať" | **reagoval — odmietol** — ICP v2 |
| Hevi (hevisleep.sk/.cz) | email | kombinovaná správa: dva samostatné SK/CZ Shopify obchody ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-9]]) — ICP v2 |
| [[gudslip|Gudslip (gudslip.cz)]] | email | kombinovaná správa: spotrebný tovar bez predplatného ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[gudslip]] — projekt, [[outreach-batch-9]] — batch) — ICP v2 |
| Resty (feelresty.com) | IG DM | kombinovaná správa: refilly bez predplatného ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-9]]) — ICP v2 |
| Tatramodel (tatramodel.sk) | email | žiadny `<meta viewport>` — web nemá mobilnú verziu ✅20.7. | 2026-07-20 | — | — | **oslovený** ([[outreach-batch-10]]) — zastarané SK e-shopy; odoslané aj napriek výhrade proti forme, viď batch stránka |
| Vcelo (vcelo.sk) | email | 3.7–4.2 s načítanie na mobile, 4 merania ✅20.7. | 2026-07-21 | — | — | **oslovený** ([[outreach-batch-10]]) |
| Konvička (konvicka.sk) | email | 2.3–4.2 s na mobile, kolísavé ✅20.7. | 2026-07-21 | — | — | **oslovený** ([[outreach-batch-10]]) |
| Neoprot (neoprot.sk) | email | 2.4–2.7 s na mobile ✅20.7. | — | — | — | **⏸️ pozdržaný** — možno nepredáva online ([[outreach-batch-10]]) |
| IMI Nitra (iminitra.sk) | email | žiadny `<meta viewport>` + jQuery 1.7.2 + konzistentne pomalý mobile ✅21.7. | — | — | — | **kvalifikovaný** ([[outreach-batch-11]]) — západné SK |
| RehaCARE (rehacare.sk) | email | 2.47–2.67 s na mobile, 4 merania ✅21.7. | — | — | — | **kvalifikovaný** ([[outreach-batch-11]]) — západné SK |
| Rybárstvo Trnava (rybarstvotrnava.sk) | email | platforma sama deklaruje `is_responsive_layout = false` ✅21.7. | — | — | — | **kvalifikovaný ⚠️ slabší fit** ([[outreach-batch-11]]) — západné SK |
| Home Bound Custom Decor (Sumita & Anuj) | IG DM | brand-first: 39,1K, custom gifting na „Dawn Copy" default šablóne ✅21.7. | 2026-07-21 | — | — | **oslovený** ([[outreach-batch-12]]) — US bulk |
| Corn Crib Candles | IG DM | brand-first/demand-leak: 31K, 33/238 vypredaných ✅21.7. | 2026-07-21 | — | — | **oslovený** ([[outreach-batch-12]]) — US bulk |
| Earth Berry Apothecary (Elena Bozzi Ardagna) | IG DM | brand-first: 14,1K, story brand na Dawn šablóne ✅21.7. | 2026-07-21 | — | — | **oslovený** ([[outreach-batch-12]]) — US bulk |
| Bounding Main | IG DM | brand-first: 3 predajne CA, „Copy of Dawn" + 83 scriptov ✅21.7. | 2026-07-21 | — | — | **oslovený** ([[outreach-batch-12]]) — US bulk |
| [[ember-coffee\|Ember Coffee Co.]] | IG DM | brand-first: „best coffee in MN", 89 scriptov ✅21.7. | 2026-07-22 | — | **2026-07-22** — „roasted fresh, shipped same week 😊☕️" (ako predajca) | **reagoval** — priznanie + reframe (subscription) odoslaný 24.7. ([[ember-coffee]]) ⚠️ redesign 2025 |

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

## ICP — kto je cieľová skupina

Definície sa presunuli na vlastné stránky (21.7.), aby sa dali porovnávať a verzionovať:

| ICP | Kto | Dávky | Stránka |
|---|---|---|---|
| **v1** | handmade makeri s rozbitým kanálom (US/UK/CA) | 1–8 | [[icp-handmade-makers]] |
| **v2** | mladé DTC značky SK/CZ s funkčným, ale brzdiacim Shopify | 9 | [[icp-dtc-znacky-sk-cz]] |
| **v3** | etablované SK firmy so zastaraným webom (redesign, email) | 10, 11 | [[icp-zastarane-sk-eshopy]] |

## Poznatky

Všetky poznatky (#1–#17) majú kanonický domov v [[insights]]. Predtým žili tu a v batch stránkach,
s kolíziami v číslovaní — tie sú vyriešené a preložené na stránke poznatkov.

Najdôležitejšie pre prácu s touto tabuľkou:
- **[[insights|#1]]** — „nemá e-shop" nie je pain point; treba viditeľný dôkaz nestíhania
- **[[insights|#2]]** — otvárač znejúci ako od zákazníka si vypýta priznanie (vystrelil 3×)
- **[[insights|#4]]** — hook „web nefunguje" overiť v deň odoslania a pomenovať presný failure mode
- **[[insights|#5]]** — spiaci účet nie je lead

## Výsledky a meranie

Agregované čísla (odoslané, odpovede, response rate podľa hooku/kanála/jazyka/dávky) sú
v [[dashboard]]. Vyhodnotenie promptov a rubrika sú v [[wiki/outreach/evals/index|evals/]].

Historické priebežné dáta k 16.7. (EN 5/18, SK IG 4/6, SK email 0/2; brand-first 3/6 vs.
tech-first 1/6) sú prekonané aktuálnymi číslami v dashboarde — ponechané v `log.md`.

## Nové línie a niche (2026-07-20)

- **Nože + koža** ([[outreach-batch-8]]) — 20 kvalifikovaných zo 47 (~43 % strike rate). Nože a koža
  majú **opačný problém**: nože majú eshop, ktorý je vypredaný (demand leak), koža má funkčný eshop,
  ktorý je schovaný (bio vedie na blog/linktree/Notion).
- **Drevo/nábytok** ([[outreach-batch-7]]) — len 2 kvalifikovaní z ~20. Remeselníci tu skôr **vôbec
  nemajú e-shop** než majú mŕtvu doménu, takže hook cieli na chýbajúci spôsob objednania.

## Zdroje

- [[cold-outreach-manual]] — postup, prompty
- `raw/cart.design/cold-outreach-clients/` — research poznámky jednotlivých prospektov
- `raw/cart.design/cold-outreach-system/` — šablóna, master prompty
- `raw/cart.design/cold-outreach/ig-sk-leads-2026-07-15.md` — SK Instagram leady bez e-shopu (Firecrawl + Kimi WebBridge)
- `raw/cart.design/cold-outreach/firecrawl-test-batch-2026-07-15.csv` — test dávka SK e-shopov cez Firecrawl (väčšinou aktívne e-shopy, nie cieľový ICP)
