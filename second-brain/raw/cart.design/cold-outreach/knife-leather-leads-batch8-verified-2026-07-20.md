# Knife + Leather makers — batch 8, OVERENÝ research (2026-07-20)

Nahrádza `knife-leather-leads-batch8-2026-07-20.md` z predchádzajúcej session (ten obsahoval prevažne
neoverené placeholdery: `TBD (@allstarknives)`, `?` followers, handles odhadnuté zo search výsledkov).
Starý súbor ponechaný nedotknutý (hard rule: raw/ sa needituje) — **nepoužívať ako zdroj leadov.**

## Metodika

1. **Discovery — Firecrawl** (`firecrawl search`), 9 queries, mix `site:instagram.com` + listicle queries.
   Pool: 47 unikátnych IG handles (profilové URL + `@mentions` v title/description search výsledkov).
2. **Verifikácia followers/bio — Kimi WebBridge** (prihlásený browser).
   ⚠️ **Firecrawl instagram.com nescrapuje** („we do not support this site") — všetky IG dáta idú cez Kimi.
   Skript: navigate na profil → `evaluate` čítajúci `og:description` + `body.innerText` (followers, bio, link).
3. **Verifikácia webu — curl** (HTTP status, DNS) + **Firecrawl scrape** (platforma, počet „Sold out" / „Add to cart").

## Kvalifikačné kritériá

- 10K+ IG followers **alebo** silný demand signál (sold-out katalóg, backlog, custom orders open)
- **A zároveň** rozbitý/chýbajúci predajný kanál: žiadny web · mŕtva doména · Etsy-dependent ·
  eshop existuje, ale je slabý (Wix/starý, prázdny, produkty mimo eshopu)

Marko explicitne chcel **aj leady, ktoré eshop majú, ale oplatí sa ho prerobiť.**

---

## Kvalifikovaní — nože (10)

| # | Handle | Followers | Web (stav k 20.7.) | Uhol |
|---|---|---|---|---|
| 1 | @chuckrichardsknives | 116K | chuckrichardsknives.com — **Wix**, shop 7× „Sold out", drobný katalóg | redesign + demand leak |
| 2 | @angerknives | 107K | **žiadny web, žiadny link v bio** (bio = len „Bladesmith") | žiadny spôsob nákupu |
| 3 | @radknives | 59K | rad-edc.com — Shopify, **16× „Sold out"** | demand leak |
| 4 | @lewgriffinknives | 58K | lewgriffinknives.com — Shopify, funkčný, 2× sold out | redesign-grade (najslabší hook) |
| 5 | @slavicsmith | 47K | **žiadny externý link v bio** (overené: 0 external links) | žiadny spôsob nákupu |
| 6 | @ooakforge | 28K | linktr.ee → ooakforge.com/shop (Squarespace) — **prázdny shop**, bio „No Custom Orders!" | dopyt odmietaný, nie zachytený |
| 7 | @crimsonknifeco | 25K | crimsonknives.com — Shopify, **20 z 20 položiek „Sold out"** | najsilnejší demand leak v dávke |
| 8 | @irongrovetoolco | 16K | **irongrovetoolco.com nemá DNS (000)**; bio linkuje článok na texasranches.com | žiadny vlastný predajný kanál |
| 9 | @nandaknives | 13K | nandaknives.com — Squarespace, **1 produkt** ($1,250); bio „DM for inquiries" | predaj cez DM |
| 10 | @darktimbercustoms | 11.5K | **žiadny link v bio** | žiadny spôsob nákupu |

## Kvalifikovaní — koža (10)

| # | Handle | Followers | Web (stav k 20.7.) | Uhol |
|---|---|---|---|---|
| 11 | @morrisonmadeleather | 169K | linktr.ee → morrisonmadeleather.com (Shopify, 4× sold out); linktree plný partnerských odkazov (Weaver, Wolverine) | vlastný predaj utopený medzi partnermi |
| 12 | @odinleather | 82K | odinleathergoods.com — Shopify; **bio linkuje „leather-craft-resources", nie shop** | shop schovaný za obsahom |
| 13 | @dsleathergoods | 82K | **dsleathergoods.etsy.com** — Etsy-dependent, 3000+ recenzií | escape Etsy |
| 14 | @girtyleatherco | 71K | girtyleatherco.com — Shopify, **10× „Sold out"**, bio „Custom Orders Open" | custom flow mimo eshopu |
| 15 | @nerbhandcrafted | 69K | **žiadny web — v bio len `nerbhandcraft@gmail.com`** | objednávky cez e-mail |
| 16 | @luavafinland | 51K | luavafinland.com — Shopify (FI) | redesign-grade |
| 17 | @f.p.leathercraft | 43K | msha.ke → foolishprideleather.com — **Wix** | redesign (Wix) |
| 18 | @lordleathercraft | 37K | lord.crofte.fr = **holá linková stránka**; produkty katalogizované na **Notion page**; shop.crofte.fr predáva len strihy | produkty v Notione, nie v eshope |
| 19 | @oroxleatherco | 18K | oroxleather.com — Shopify, 4. generácia (1933) | redesign-grade |
| 20 | @thelocalbranch | 9.8K | thelocalbranch.co — Shopify, 3× sold out; kamenná predajňa NY | ⚠️ pod 10K — najslabší v dávke |

---

## Overení a vylúčení

| Handle | Followers | Dôvod vylúčenia |
|---|---|---|
| @margigaba | 15.7K | margigaba.com **mŕtva doména (žiadny DNS)** — ale **posledné príspevky z 2021**, spiaci účet → žiadny živý dopyt |
| @number_41_lb | 30K | B2B továreň (Bejrút, „Manufacturing for Brands & Businesses") — nie solo maker, mimo ICP |
| @coalironworks | 57K | predáva kovacie lisy (vybavenie), nie výrobky |
| @isitleather | 25K | edukačný účet o koži, nič nepredáva |
| @dsleathergoods (čiastočne) | 82K | ponechaný, ale pozor: hlavný produkt sú **strihy/patterns**, nie hotové výrobky |
| @horweenleather, @lineapellefair, @laconceria, @customknifemakers | — | dodávateľ koží / veľtrh / odborný magazín / agregátor |
| @smitzoon | 796 | Royal Smit & Zoon — priemyselná garbiareň |
| @thekesterhomestead | 5.5K | svadobná lokalita, nesúvisí |
| ~25 ďalších (@enso_forge 2.9K, @adams.knives 2.1K, @coolbeansknives 2.4K, @kemblecustomknives 1.3K, @rawforgeknives 639, @balrog_forge 523, @arbor_bladesmith 516, @formedandforged 38, @easttennleather 38, @jennsleathercraft 2.6K, @alettabags 3.8K, @ianjamesmade 3.3K, @jcombsandco 1.1K, @dks_knives 4.5K, @littlewolfironworks 4.2K, @nicksknifeworks 1.3K, @andrewksmithknives 1.5K, @grayzer86 889, @ksw_customknives 1.8K, @akillesx2 1.8K, @petrescufactory 4.3K, @championxknives 9.6K, @jake2jakecustomknives 2.5K, @sir_knifesalot 507, @noakecustomknives 1.1K, @davidmoonforge 1.1K) | <10K | pod prahom publika, žiadny silný demand signál |

## Poznatky k nise

1. **Strike rate 20/47 (~43 %)** — výrazne vyšší než drevo/nábytok (batch 7: 2 z ~20).
   Nože aj koža majú veľa účtov s reálnym publikom.
2. **Nože ≠ „chýbajúci eshop", ale „vypredaný eshop".** Traja z desiatich (crimson 20/20,
   rad-edc 16, chuck 7) majú eshop, ktorý je prakticky celý sold out. To nie je technický problém —
   je to **demand leak**: publikum príde, nič si nekúpi, odíde. Iný hook než batch 7.
3. **Koža má opačný vzorec** — väčšina má funkčný Shopify; problém je, že **predaj je schovaný**
   (odin: bio vedie na blog, morrison: linktree plný cudzích partnerských odkazov,
   lord: produkty v Notione). Hook = „tvoj vlastný predaj je zakopaný".
4. **Účty bez akéhokoľvek linku majú prekvapivo veľké publikum** (anger 107K, nerb 69K, slavic 47K).
   V predošlých nišach to boli malé účty.
5. ⚠️ **Nože = HIGH-RISK platby** — pred pitchom overiť platobný procesor (platí od batch 5;
   Stripe nemusí nože pustiť).
6. **Spiaci účet != lead.** margigaba mala ideálny technický profil (15.7K + mŕtva doména),
   ale posledný post 2021. Mŕtva doména bez živého dopytu je bezcenná — kontrolovať dátum posledného postu.
