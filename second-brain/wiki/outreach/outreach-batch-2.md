---
type: project
status: active
created: 2026-07-15
updated: 2026-07-16
aliases: [Outreach batch 2]
tags: [cart-design, cold-outreach]
---

# Outreach batch 2 — 12 správ (EN) + brand-first/tech-first test

Fáza 1 otvárače podľa [[cold-outreach-manual]] a [[cold-outreach-pipeline]] (ICP v1). Fakty overené 2026-07-15 (curl).

**Experiment (Markov návrh):** rozdelené na **6 tech-first** (technický postreh je hlavný obsah) a **6 brand-first** (postreh o značke/príbehu je hlavný, technická vec je len vsuvka). Po prvej vlne porovnáme response rate podľa typu — pozri [[cold-outreach-pipeline]] sekcia Zber dát.

---

## TECH-FIRST (6)

### 1. The Low Key Co — IG DM (@thelowkeyco_)
Hook ✅15.7.: thelowkeyco.com je teraz **parkovaná doména** (GoDaddy parking page) — nefunguje vôbec, presmeruje na prázdnu stránku. `.store` varianta funguje.

> Hey Keila! Saw the "sold out tables" posts — that kind of demand at markets is rare. Random find though: thelowkeyco.com looks like it's turned into a parked/for-sale page now. Did you let that domain lapse, or is thelowkeyco.store the main one these days?

### 2. Sweet Nothings Studios — IG DM (@sweetnothingsstudios)
Hook ✅15.7.: sweetnothingsstudios.com **nenačíta sa vôbec** (timeout) — v júni ešte fungoval na Big Cartel.

> Hey! The "web drop 5PM CT" format is such a smart way to create urgency. Tried checking out sweetnothingsstudios.com just now though and it's not loading at all. Is the site down for you too, or is it just me?

**REAGOVALA 15.7. 15:54:** „Shop is up and running, perhaps try refreshing your browser!" — hook z jej pohľadu vyvrátila. **Re-verifikácia 16.7. (curl+openssl):** problém je reálny, ale presnejší — apex doména `sweetnothingsstudios.com` nemá SSL certifikát (https bez www padá), funguje len `www.`. Detail a ďalší krok: [[sweet-nothings-studios]] (promovaná do `projects/`).

### 3. Forest Nine — IG DM (@forestnine)
Hook ✅15.7.: forestnine.com je **zamknutý heslom** — obchod je uzavretý pre objednávky (potvrdené: "password" na stránke).

> Hey! 44K+ Etsy sales at 5 stars for handmade journals is seriously impressive longevity. Noticed forestnine.com is password-locked right now, though — is that the backlog closing things off, or a temporary site issue?

### 4. Miners Ink (J. Hiatt) — IG DM (@miners_ink)
Hook ✅15.7.: minersink.com **neexistuje** (mŕtva DNS).

> Hi! Turquoise and lapidary work like yours is hard to find done well. CuriousI looked up https://www.gemsofcalifornia.com/ and it doesn't resolve at all. Do you sell mostly at pop-ups and through IG these days, or is there a store I'm missing?

### 5. Kamari Candle Co — IG DM (@kamaricandleco)
Hook ✅15.7. (prerobené): web má /shop s košíkom, ale copyright na stránke je zamrznutý na **2022** — pôsobí opustene napriek aktívnemu TikToku.

> Hey! The 1,000-cup restock is wild — that's real demand. One odd thing: kamaricandleco.com still shows a 2022 copyright at the bottom, like it hasn't been touched in years even though you're clearly active on TikTok. Just an old template, or has the site kind of been left behind?

### 6. Macrame on the Move — IG DM (@macrameonthemove)
Hook ✅15.7. (prerobené — CSV mal "no cart", teraz cart existuje): Wix funguje, otázka smeruje na skúsenosť s predajom "on the road".

> Hey! Travelling and making macrame jewelry at the same time sounds like a logistics puzzle on its own. How's the Wix store working out for you while you're on the move — does it hold up okay, or is managing it from the road kind of a pain?

---

## BRAND-FIRST (6)

### 7. Disciple Designed — IG DM (@discipledesignedleather)
Hook: 6–8 mesačný backlog, 466K IG + 441K TikTok — obdiv k remeslu, technická vec len vsuvka na konci.

> Hey Jacob! One-man leather shop with a 6-8 month wait list and nearly half a million people watching you make it happen — that's a rare kind of trust people put in a craftsman. Genuinely curious how you're managing order tracking through a backlog that long. Still doing it all through the Squarespace cart?

### 8. Rebecca D Enamel — IG DM (@rebeccadenamel)
Hook: micromosaic/enamel remeslo od 2012, technika ako hlavný obdiv.

> Hi Rebecca! Micromosaic and vitreous enamel work at your level takes years to get right — you can tell it's not a trend for you, it's a craft. Just curious, since I know a lot of jewelers in this space struggle with it: does your current site do a good job showing the process, or mostly just the finished pieces?

**REAGOVALA 16.7. 8:17:** „I'm working on a renovation for my website right now." — najsilnejší timing signál z EN vlny. Detail: [[rebecca-d-enamel]] (promovaná do `projects/`).

### 9. Hazel Hand Engraving — IG DM (@hazel.handengraving)
Hook: hand-push engraving od 2013, zaujímavý fakt (predáva kurzy, nie šperky) je len zvedavá otázka na konci.

> Hey Marlen! Hand-push engraving is one of those skills that takes a decade to make look effortless — really cool to see it documented. Random question: I noticed your site's set up to sell courses/tutorials — is that the main focus now, or do people still commission custom pieces from you directly?

**REAGOVALA 15.7. 23:43:** nič nepredáva — všetko vzdelávanie free na YouTube, zákazky cez partnera @firestonefinejewelry. Research o „predaji kurzov" vyvrátený → **pravdepodobne nekvalifikovaná** (nemá a nechce vlastný predajný kanál). Detail: [[hazel-hand-engraving]] (promovaná do `projects/`).

### 10. Jake Newell (Custom Hand Engraving) — IG DM (@customhandengraving)
Hook: backlog "not accepting new work" — silný signál dopytu, žiadny web vôbec (technická vec je len otázka na konci).

> Hey Jake! "Not accepting new work at this time" is a good problem to have means the backlog speaks for itself. How are you keeping track of who's next in line right now, just through IG/DMs, or do you have something more organized behind the scenes?

### 11. DoubleK Custom Leathercraft — IG DM (@double_k_leatherwork)
Hook: niche remeslo (custom beaded tack), aktívny v komunite — otázka o organizácii objednávok.

> Hey! Custom beaded tack is such a specific craft — not a lot of people doing it well. Saw you're taking orders through FB/IG. Does that get overwhelming to track, or have you got a system down for it by now?

### 12. Optimistic Soap — IG DM (@optimisticsoap)
→ **Vlastná lead stránka: [[optimistic-soap]]** (promovaná do `projects/`).
Hook: 229K followers je obdiv, technická otázka (Wix at scale) je vsuvka.

> Hey Molly! 229K people following a handmade soap brand out of Portland is genuinely rare air. Curious how Wix has been holding up for you at that scale smooth, or does it start creaking once you're getting real volume through it?

**REAGOVALA 2026-07-15** — dlhá, priateľská, vtipná odpoveď (prvá reakcia z EN batchov, brand-first skupina). Kľúčové fakty z jej správy:
- Vyše roka „prechádza" na Shopify, ale nemá čas — **celý rok platí double hosting** (Wix + Shopify).
- Wix bug: na billing/shipping slipe sa občas zobrazí **nesprávne meno platcu** — zákazníčke pri darčeku prišlo cudzie meno, veľmi ju to znepokojilo. Peniaze chodia správne.
- Verdikt na Wix: „pretty good", ale keby začínala odznova, išla by rovno na Shopify.
- Kompliment jemne odbila: kamarát **Nathan / Clover Soapworks** (tiež solo soapmaker, Portland) má viac followerov → potenciálny ďalší lead.
- Otvorila vtipom o creeper DMs — oceňuje, že správa neznela ako sales/creep. Fáza 2 musí byť transparentná, nie „hrať prekvapeného".

**Fáza 2 ODOSLANÁ 2026-07-15** (finálna verzia po Markových úpravách — viac konverzácie pred pitchom, custom code namiesto Shopify, mäkké CTA):

> Ha — paying double hosting for a year as a form of procrastination might be the most relatable thing I've read all week 😄
>
> And honestly, that billing name thing is wilder than you're giving it credit for. "The money still arrives, but the customer thinks a stranger sent them soap" is such a specific kind of haunted. I get why that woman was unsettled — a gift from an unknown name is basically a horror movie opening scene.
>
> Cards on the table though, since you've been straight with me: this is actually what I do — I build custom-coded stores for handmade brands. No Shopify, no templates, built from scratch around how *you* actually work (which also means gremlins like the billing-name thing just can't happen). Zero pressure, but if you want, I can send a couple of thoughts on what getting off Wix would realistically look like for you — worst case, you finally stop paying double rent.
>
> (And say hi to Nathan!)

Štruktúra: vtip (jej double hosting) → empatia k billing bugu → transparentný pitch (custom code, „since you've been straight with me") → P.S. Nathan. Zámerne vyhodený vtip o Portland soap scéne (súťažil by s jej pointou o Nathanovi). Dôležité poučenie: **cart.design = custom code, nie Shopify** — pitch nikdy nerámovať ako Shopify migráciu.

---

## Kanál a poznámky

Všetko IG DM (podľa CSV stĺpca `channel`). Posielaj max 5–6/deň, US popoludnie (17:00–21:00 nášho času).

## Ako vyhodnotíme experiment

Po odoslaní všetkých 17 správ (batch 1 + batch 2) — zapíš do [[cold-outreach-pipeline]] tabuľky reakcie. Porovnáme:
- Response rate: tech-first vs. brand-first
- Response rate: mŕtvy/rozbitý web vs. funkčný web (redesign angle)
- Najsilnejšie reagujúca niche (koža/šperky/sviečky/mydlo)

## Zdroje

- `raw/cart.design/cold-outreach/Cart Leads - Sheet1.csv`
- Verifikácia: curl 2026-07-15
- [[cold-outreach-manual]], [[cold-outreach-pipeline]], [[outreach-batch-1]]
