---
type: project
status: active
created: 2026-07-15
updated: 2026-07-15
aliases: [Outreach batch 1, Prvá vlna outreach]
tags: [cart-design, cold-outreach]
---

# Outreach batch 1 — prvých 5 správ (EN)

Fáza 1 otvárače podľa [[cold-outreach-manual]] — bez predaja, cieľ vyvolať reakciu. Zdroj dát: Cart Leads CSV. Stav sa trackuje v [[cold-outreach-pipeline]].

**Všetky fakty overené 2026-07-15** (CSV research z 15. júna bol už čiastočne stale — 3 z pôvodných 5 hookov neplatili). Pravidlo: **hook sa overuje v deň odoslania**, nie deň predtým.

Posiela Marko. Po odoslaní: povedz Claudovi „poslané <meno>" → update pipeline.

---

## 1. LadyBuQ Art — IG DM (@ladybuq_art_studio) ✅ overené 15.7.

Hook: ladybuqart.com mŕtva doména (DNS nefunguje) + 8 721 Etsy sales.

> Hi! Came across your leather work — 8,700+ sales and 4.9 stars on Etsy is no joke. One thing surprised me though: ladybuqart.com doesn't resolve anymore. Did you drop the domain on purpose, or is that something that slipped through the cracks?

---

## 2. Jenny Topolski — email ✅ overené 15.7. (HTTP 403 stále)

Hook: 6 249 Etsy sales (5★), vlastný web blokuje návštevníkov chybou 403.

**Subject:** Your website is turning people away (literally)

> Hi Jenny,
>
> I came across your jewelry through Etsy — 6,000+ sales with a straight 5-star rating is genuinely rare.
>
> Here's the odd part: when I tried visiting topolski-jewelry.com, the site blocked me with an error (HTTP 403). It's likely doing that to everyone who finds you outside Etsy.
>
> Is that something you're aware of? Curious whether it's a hosting hiccup or the site's just been retired.
>
> Marek

---

## 3. iamrachel — IG DM (@iamrachelshop) ✅ overené 15.7.

Hook: iamrachelshop.com mŕtva (DNS) + 5 124 Etsy sales + live IG grid sales.

> Hi Rachel! Love the enamel work — and the live grid sales are such a clever format. Quick heads-up though: iamrachelshop.com doesn't load at all anymore. Is everything running through Etsy and the .co.uk now, or did the .com just quietly expire on you?

---

## 4. Creations That Rock — IG DM (@creationsthatrock) ✅ overené 15.7. (web práve zomrel)

Hook: creationsthatrock.com sa už nenačíta (v júni ešte fungoval ako portfólio) + 101K TikTok + timed drops.

> Hey Natalia! The timed drops are addictive to watch — "79/100 earrings" had me checking back. One thing though: I tried creationsthatrock.com and it's not loading at all right now. Do your TikTok followers have anywhere to land when they miss a drop, or is it all in the comments?

*Poznámka: web zomrel niekedy po 15.6. — čerstvý problém, možno o ňom ešte nevie. Najsilnejší hook z celej dávky.*

---

## 5. Pierre Laborde — IG DM (@pierrelabordenewyork) ✅ overené 15.7. (Squarespace beží)

Hook: drops vypredané za 30 min + NYT press; web beží, ale je základný Squarespace.

> Hey Francis! Read the NYT piece — "creates a frenzy with every drop" is the kind of press money can't buy. Genuine question: when bags sell out in 30 minutes, what happens to everyone who missed out? Do they just wait for the next drop, or is there a waitlist somewhere?

*Poznámka: tu web funguje, takže hook nie je "broken site" ale "demand leak" — čo sa deje s dopytom, ktorý sa nezmestí do dropu.*

---

## Vyradené z pôvodnej dávky (stale hooky — CSV research z 15.6. už neplatil)

| Lead | Pôvodný hook | Realita 15.7. | Čo s ním |
|---|---|---|---|
| Drop Dead Candles | web down | postavili nový Shopify store | nový uhol neskôr („gratulujem k novému webu" je slabé; sledovať) |
| Optimistic Soap | Wix bez košíka | Wix store s produktami už beží | prerobiť hook (napr. Wix limity pri 229K publiku); Tier 2 |
| Kamari Candle Co | web nevie predávať | GoDaddy /shop s košíkom existuje | prerobiť hook (stale 2022 web vs. TikTok momentum); Tier 2 |
| Hazel Hand Engraving | Shopify predáva len kurzy | na webe už vidno šperky | overiť hlbšie pred oslovením |

## Poznámky k odosielaniu

- **Overiť hook v deň odoslania** (Claude to spraví na povel „over batch").
- Posielaj v US popoludňajších hodinách (17:00–21:00 nášho času = ráno/obed US East).
- Max 5/deň — stíhaš reagovať a iterovať.
- Follow-up po 3–5 dňoch bez reakcie; po každej odpovedi → fáza 2 (pitch).

## Zdroje

- `raw/cart.design/cold-outreach/Cart Leads - Sheet1.csv` (research 2026-06-15)
- Verifikácia webov: curl 2026-07-15 (Claude)
- [[cold-outreach-manual]], [[cold-outreach-pipeline]]
