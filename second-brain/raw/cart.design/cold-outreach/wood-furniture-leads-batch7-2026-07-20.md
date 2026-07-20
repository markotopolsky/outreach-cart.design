# Wood/furniture makers — nová niche, discovery 2026-07-20

Experiment na povel Marka: otestovať novú nišu (drevo/nábytok, US/UK/CA trh) mimo doterajších (koža, šperky, sviečky, mydlo, keramika/sklo, nože). Metóda: Firecrawl `site:instagram.com` search na kľúčové slová → Kimi WebBridge (prihlásený browser) na overenie followers/bio/link-in-bio → curl/Kimi na overenie cieľovej stránky (má/nemá cart).

## Search queries použité (Firecrawl)

1. `site:instagram.com custom furniture maker handmade woodworking`
2. `site:instagram.com live edge table maker sold out waitlist`
3. `site:instagram.com woodworker "DM to order" OR "link in bio" cutting boards bowls handmade`
4. `site:instagram.com wood turning bowls handmade backlog "not accepting" OR "waitlist"`
5. `site:instagram.com hand carved wood spoon maker handmade sold out`
6. doplnkové lookupy: Yeg Woodcraft (Canada), Wood & Weld Furniture (Chris Perry)

## Kvalifikovaní (spĺňajú ICP: 10K+ followers ALEBO preukázaný dopyt + rozbitý/chýbajúci predajný kanál)

### Raina Nicole Woodworks (@rainanicolewoodworks)
- **248K IG followers**, Orange County CA. Custom furniture maker, brand partnerstvá (Home Depot x Makita, BRUNT Champs), YouTube + TikTok.
- Bio link → linktr.ee → rainanicolewoodworks.com (Squarespace).
- **Nav webu: Home / The Process / Gallery / Contact — žiadny shop/cart.** Obrovské publikum, no spôsob ako si niečo objednať/kúpiť online, len kontaktný formulár.
- Overené 2026-07-20 (Kimi WebBridge snapshot + evaluate na nav).

### Doucette and Wolfe Furniture Makers — Matthew Wolfe (@dwfurnituremakers)
- **25.2K IG followers**. "Museum quality custom furniture... for clients around the world." Mt. Washington Valley, ME.
- Web: doucetteandwolfefurniture.com — **starý iWeb-style statický web (celý na obrázkoch, žiadna reálna navigácia/cart)**, kontakt len telefón + email.
- Overené 2026-07-20 (Firecrawl scrape markdown — web je prakticky len obrázky + telefón/email, žiadny nákupný/objednávkový flow).

## Preverení, ale nekvalifikovaní (dôvod vylúčenia)

| Lead | Followers | Dôvod vylúčenia |
|---|---|---|
| TK Fareed (@tk.fareed) | 346K | **Má funkčný e-shop** (tkfareed.com — Shop/Checkout/Collections) — kanál nie je rozbitý, nesedí na ICP |
| CT Woodwork (@ctwoodwork) | 5,569 | Skôr woodworking škola/kurzy než predaj hotových kusov; pod 10K, slabý demand signál |
| Saman's Custom Woodwork (@samanscustomwoodwork) | 3,001 | Pod 10K, žiadny doložený dopyt (sellout/waitlist/backlog) |
| Elwood Design (@elwooddesignco) | 2,799 | Pod 10K, má vlastný web s adresou — pravdepodobne funguje, žiadny dôkaz rozbitého kanála |
| DeVine Woodworking (@devinewoodworking) | 911 | Pod 10K, má vlastný web (devine-woodworking.com), žiadny demand signál |
| Yeg Woodcraft (@yegwoodcraft) | 5,028 | Pod 10K, má vlastný web + "Boxing Day Sale" — pravdepodobne funkčný predaj |
| Wood & Weld Furniture / Chris Perry (@chrispaulperry, @woodandweldfurniture) | 20K+ | Je marketingový kouč pre iných remeselníkov, má tím (crew) — už sofistikovaný v predaji, nesedí na ICP (nie je "topí sa v operatíve") |
| Peterman's Boards & Bowls (@petermanwoodworking) | 563 | Príliš malé publikum |
| Tyler van Iderstein (@heronmarkbenchworks) | 252 | Príliš malé publikum |
| Sean Miller (@imenthused281) | 1,410 | Príliš malé publikum |

## Úplný zoznam — všetko, čo vypadlo z 5 search queries (nielen overení)

Marko chcel vidieť všetkých kandidátov, nielen môj vyfiltrovaný výber — nižšie je kompletný zoznam z surových výsledkov Firecrawl search, so stavom overenia pri každom. Handle „neistý" = meno/firma je zo search snippetu, ale nemám potvrdený IG handle (netýkal som sa ho cez Kimi WebBridge) — treba dohľadať manuálne pred akýmkoľvek kontaktom.

| # | Lead | Zdroj (query) | Stav |
|---|---|---|---|
| 1 | **Raina Nicole Woodworks** (@rainanicolewoodworks) | 1 | ✅ **kvalifikovaná** — pozri vyššie |
| 2 | **Doucette and Wolfe / Matthew Wolfe** (@dwfurnituremakers) | 1 | ✅ **kvalifikovaný** — pozri vyššie |
| 3 | Kamiya Furniture (@furnitureisart) | 1 | Neoverené — "No nails/screws/stains, Guaranteed for Life", treba skontrolovať followers + web |
| 4 | CT Woodwork (@ctwoodwork) | 1 | Vylúčené — pozri tabuľku vyššie (5,569, škola/kurzy) |
| 5 | Metal and Wood / John Malecki (@metalandwood.us) | 1 | Neoverené — John Malecki je známy YouTuber/maker, pravdepodobne má plnohodnotný e-shop, ale nekontroloval som priamo |
| 6 | DeVine Woodworking (@devinewoodworking) | 1 | Vylúčené — pozri tabuľku vyššie (911, vlastný web) |
| 7 | Saman's Custom Woodwork (@samanscustomwoodwork) | 1 | Vylúčené — pozri tabuľku vyššie (3,001, žiadny demand signál) |
| 8 | Jeff Miller (@furnituremaking) | 1 | Neoverené — 50 rokov v odbore, pravdepodobne prevádzkuje furnituremaking.com (woodworking škola) — treba overiť, či predáva aj hotové kusy |
| 9 | Parkman Woodworks LA (@parkmanwoodworks) | 1 | Neoverené — inzerujú nábor ("WE'RE HIRING"), naznačuje zabehnutý tím, nie solo maker — nízka priorita |
| 10 | Elwood Design (@elwooddesignco) | 1 | Vylúčené — pozri tabuľku vyššie (2,799, vlastný web) |
| 11 | Redden Custom Woodworks (Sean, Napa Valley) | 1 | Handle neistý — one-man shop, "single-item focus", z post-snippetu bez potvrdeného @handle |
| 12 | Boggsbench / Brian Boggs | 2 | Neoverené — vlastný web boggsbench.com s waitlistom (timberframe), robí nábytok od 1982 — treba overiť, či web má cart alebo len waitlist formulár |
| 13 | Ophelia's Garden tables — Hamlet / Arega Grigoryan | 2 | Handle neistý — "live edge epoxy river tables, kompletne ručne robené", z post-transkriptu bez potvrdeného @handle |
| 14 | shegong.one | 2 | Neoverené, nízka priorita — meno firmy pôsobí ako reseller/manufacturer, nie solo remeselník, možno mimo US/UK/CA |
| 15 | Art of Tree | 2 | Neoverené — z popisu znie ako firma ("we help people create spaces"), pravdepodobne nie solo maker |
| 16 | Yeg Woodcraft (@yegwoodcraft) | 2 | Vylúčené — pozri tabuľku vyššie (5,028, vlastný web + Boxing Day Sale) |
| 17 | Wood & Weld / Chris Perry (@woodandweldfurniture, @chrispaulperry) | 2 | Vylúčené — pozri tabuľku vyššie (marketing kouč, má crew) |
| 18 | Flowyline Design | 2 | Neoverené, iný model — predáva stavebné plány (400 objednávok plánov), nie hotový nábytok |
| 19 | Tailored Timber Co | 3 | Handle neistý — "HANDMADE WITH CARE. BUILT TO LAST." cutting boards, z OCR textu na reeli bez potvrdeného @handle |
| 20 | Peterman's Boards & Bowls (@petermanwoodworking) | 3 | Vylúčené — pozri tabuľku vyššie (563, príliš malé) |
| 21 | hardwoodelevated | 3 | Handle neistý — spomenuté len ako "hardwoodelevated's profile" v snippet texte |
| 22 | craftedwood_diy (@craftedwood_diy) | 3 | Neoverené, iný model — predáva plán-knižnicu (DIY návody), nie hotové kusy |
| 23 | planeshavingswoodworking.com | 3 | Neoverené — vlastná doména viditeľná v bio jedného z postov, handle nepotvrdený |
| 24 | twice_turned (@twice_turned) | 3 | Neoverené — spomínaný ako umelec zastúpený galériou (Left Bank Galleries) — predaj cez galériu, možno mimo ICP (nie DTC) |
| 25 | Heron Mark Benchworks (@heronmarkbenchworks) | 4 | Vylúčené — pozri tabuľku vyššie (252, príliš malé) |
| 26 | prettygoodwoodturning.com | 4 | Neoverené — vlastný web s waitlistom, treba overiť handle a followers |
| 27 | Sean Miller (@imenthused281) | 4 | Vylúčené — pozri tabuľku vyššie (1,410, príliš malé) |
| 28 | andyspoons (@andyspoons) | 5 | Neoverené — spomenutý ako spoon carver v cudzom poste (tag), vlastný účet nekontrolovaný |

**Mimo niche / šum (nepatria sem, search ich vrátil omylom):** IKKAI Ceramics, orangeboy.ceramics (keramika, nie drevo), Walrus Oil (výrobca olejov na drevo, nie remeselník).

## Poznámka k metóde/nise

Wood/furniture niche má menej "mŕtva doména / web down" prípadov než koža/šperky — remeselníci v tejto nise skôr **vôbec nemajú e-shop** (portfolio-only alebo starý statický web) než že by mali rozbitý. Hook musí byť formulovaný ako "žiadny spôsob nákupu/objednávky online", nie "web nefunguje" (pozri poznatok #4 v [[cold-outreach-pipeline]] o krátkej trvanlivosti "tvoj web nefunguje" hookov — tu to ani neplatí, lebo web ako taký funguje, len nepredáva).

Vzorka je malá (2 kvalifikovaní z ~20 preverených) — vyšší strike-out rate než pri koži/šperkách, kde CSV bol vopred kurátorský. Pre ďalšie kolo by pomohlo vyhľadávať priamo cez BladeForums-style fórum ekvivalent pre drevárov (napr. Sawmill Creek, WoodNet) namiesto čistého IG search.
