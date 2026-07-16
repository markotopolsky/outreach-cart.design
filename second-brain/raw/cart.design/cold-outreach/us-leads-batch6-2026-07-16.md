# US leads batch 6 — research 2026-07-16

Metóda: WebSearch/Google discovery (kurátorské zoznamy makerov + IG sellout signály) → curl overenie domén/platforiem → Kimi WebBridge (prihlásený browser) overenie IG profilov (followers, bio, link-in-bio, aktivita). Všetky fakty overené **2026-07-16**. Firecrawl bol nedostupný (invalid token) — discovery bežalo cez WebSearch + Google v browseri.

Kľúčový trik: starší kurátorský zoznam makerov s doménami (napr. abeautifulplate.com ceramics guide, ~76 makerov) → hromadný curl → mŕtve/rozbité domény = hotové tech-first leady.

## Kvalifikovaných 15 (top výber zo 17 overených)

| # | Lead | IG handle | Followers | Niche | Lokalita | Web (stav 16.7.) | Hook |
|---|---|---|---|---|---|---|---|
| 1 | Jupiter Oak Jewelry (Jami & Miguel) | @jupiteroakjewelry | 132K | šperky (botanical/moth) | Evergreen, CO | jupiteroak.com — Shopify, cart OK | brand |
| 2 | Wolf Ceramics (Sarah Wolf) | @wolfceramics | 126K | keramika | Hood River, OR | wolfceramics.com — Shopify, cart OK; má tím + restaurant collabs | brand |
| 3 | Melissa Weiss Pottery | @melissaweisspottery | 107K | keramika (vlastná hlina) | Asheville, NC | melissaweisspottery.com — Squarespace; predaj cez newsletter notifikácie | brand |
| 4 | Mila.jito Leather (Lili W Storella) | @mila.jito | 88.5K | koža, made-to-order | Littleton, NH (podľa artisans.life, neoverené; bio má WeChat) | bio link = surová PHP URL na mob.mila-craftwork.com | brand (⚡ "Waiting list starts at 2027") |
| 5 | RBD Pottery (Rachel & Jamin Bultman) | @rbdpottery | 45.8K | keramika | Smoky Mountains, NC | rbdpottery.com — funguje; bio: "Next website restock: July 21" | brand (restock sellouts) |
| 6 | Yuzu Pottery (Mina) | @handmadeinseattle | 45.4K | keramika | Seattle, WA | bio link = **yuzupottery.etsy.com**, pritom bio: "Next Restock: July 28 at 10am PT on my website" | tech (Etsy vs. website mismatch) |
| 7 | Mud Lowery (Shannon Lowery) | @mudlowery | 39.7K | šperky (Native American striebro/tyrkys) | Fort Worth, TX | mudlowery.com — Shopify, cart OK | brand |
| 8 | Lulu LaFortune | @lulu.lafortune | 31.7K | svietidlá/vitrážové lampy, nábytok | Los Angeles, CA | lululafortune.com — 200; **bio link = Discord**, nie shop; press: Vogue | brand |
| 9 | Brit McDaniel (ex Paper & Clay) | @britmcdaniel | 25.6K | keramika | Memphis, TN | britmcdaniel.com — Shopify OK (rebrand); stará doména **shoppaperandclay.com TIMEOUT** | tech (mŕtva stará doména po rebrande) |
| 10 | Callahan Ceramics | @callahanceramics | 23K | keramika | US (lokalita neoverená) | callahanceramics.com — 200; bio: "next release: 2025 tbd" (stale, sme 2026); 58 postov / 23K followers | tech (spiaci účet) |
| 11 | Workaday Handmade | @workadayhandmade | 22K | keramika | NY | workadayhandmade.com — Squarespace OK | brand |
| 12 | Janel Foo Glassworks | @janelfooglassworks | 19.6K | vitráže | Pasadena, CA | janelfoo.com — Squarespace OK; shop účet @pasadenastainedglass; press: Martha Stewart, T Magazine, LA Times | brand |
| 13 | LOLiDE (Lori Devine) | @lolideseattle | 16.5K | šperky (svadobné prstene) | Seattle, WA | **lolide.com — HTTP 521 (Cloudflare: web server down)**, overené 2× 16.7. | tech |
| 14 | Sacha Carlos-Raps | @sacharaps | 5.5K | vitráže (custom interiors + glassware) | Brooklyn, NY | sacharaps.com — 200, cart | brand |
| 15 | Beanpole Pottery | @beanpole_pottery | 3.9K | keramika | Pacific Northwest | **beanpolepottery.com — TIMEOUT** (overené 2× 16.7.); bio: "For sales & inquiries please email me directly" | tech |

## Overení ale vyradení

- **jellenceramics** (1.5K, New Mexico) — predaj cez PayPal linky v bio; príliš tenké publikum, nurture neskôr
- **vozcollective** (3.8K, LA, maľované drevo) — Squarespace s košíkom funguje, slabý broken-channel signál
- **ceramics_by_jas** (283K!) — pivot na edukátorku (kurzy, "IG for Potters") — lekcia z Hazel: predáva kurzy, nie produkty
- **bethcyrstudio** (17.9K) — pivot na relationship coaching, šperky už nie sú core
- **piecesofnaturebyanna** (9K) — UK (RHS výstavy), nie US
- **sastainedglassco** — Hong Kong, nie US
- **firestonefinejewelry** (1.1K, sekundárny lead od Hazel) — nový Shopify web funguje, tenké publikum
- **mŕtve IG účty:** @cupboardgoods, @meha_ceramics, @jorgensenstoneware, @shop31suns, @anamarinajewelry (stránky nedostupné); @tinavidak private; @potterybyosa 0 postov
- **agoodplacemarket** — tattoo space s mydlom, nejasný fit

## Poznámky k metóde

- Google/WebSearch na "handmade + sold out/restock" vracia hlavne posty, nie účty — účty treba doťahovať cez posty (pomalé, nízky yield).
- Najvyšší yield: kurátorský guide so 76 doménami → curl za ~3 min našiel 7 rozbitých domén (z toho ale 5 malo mŕtvy aj IG — rozbitá doména často = zavretý biznis; IG verifikácia je nutná).
- IG reels sa cez evaluate nenačítajú spoľahlivo (video overlay) — posty (/p/) áno.
