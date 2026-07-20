---
type: project
status: active
created: 2026-07-20
updated: 2026-07-20
aliases: [Batch 9, DTC spánok/dýchanie SK-CZ]
tags: [cart-design, cold-outreach, sk, cz, dtc]
---

# Outreach batch 9 — DTC značky spánok/dýchanie (SK/CZ)

Prvá dávka podľa [[icp-dtc-znacky-sk-cz|ICP v2]]. Vznikla z Markovho podnetu „napíšme značkám ako nosky.cz / pekne.eu". Overenie ukázalo, že obe referenčné značky predávajú **nosné pásky a biohacking produkty**, takže dávka cieli na tento klaster, nie na dizajnové značky.

Metóda: Firecrawl search (9 dotazov) → `curl` kvalifikácia zadarmo (platforma, rýchlosť, katalóg cez `/products.json`) → cielené overenie hookov. Bez Kimi WebBridge.

## Leady

| Značka | Trh | Platforma | Katalóg | Kontakt | IG | Hook |
|---|---|---|---|---|---|---|
| **Pekne** (pekne.eu) | SK | Shopify | 15 | ⚠️ chýba (kontakt formulár neoverený) | @pekne.eu | 111 `<script>` tagov na homepage (overené 2×) |
| **Hevi** (hevisleep.sk + .cz) | SK + CZ | Shopify ×2 | 29 / 31 | podpora@hevisleep.sk | @hevisleep.sk | dva samostatné obchody, katalóg dvakrát |
| **Gudslip** (gudslip.cz) | CZ | Shopify | 32 | shop@gudslip.cz | @gudslip.cz | spotrebný tovar bez predplatného |
| **Resty** (feelresty.com) | EN/medzinárodný | Shopify | 24 | ⚠️ chýba | @feelresty | predáva refilly, ale ako jednorazový nákup |

### Pekne — hook overený ✅ (nahrádza vyvrátený nález z 20.7.)

Homepage má **111 `<script>` tagov** (overené 2× nezávislým requestom, `python3 re` nie grep). 8 z 15 produktov beží s trvalo preškrtnutou "pôvodnou" cenou (compare_at_price) — vedľajšie zistenie, do hooku nepoužité (neistá interpretácia: môže byť legitímna zľava, nie manipulácia). Rýchlosť kolíše 0.28–0.94 s pri opakovaní — nekonzistentné, preto hook stojí na počte scriptov, nie na rýchlosti. Mail sa nepodarilo nájsť, len IG @pekne.eu.

### Hevi — hook overený ✅

`hevisleep.sk` a `hevisleep.cz` majú **identické názvy produktov, ale úplne odlišné product ID** (SK: 15489925316985, CZ: 10575046672723 pri tom istom „Hevi™ Deep Sleep Tea"). Sú to teda dva nezávislé Shopify obchody, nie jeden obchod s Markets. Znamená to dvojitú údržbu katalógu, dvojitý Shopify paušál a dvojitú sadu appiek. **Najsilnejší hook v dávke** a priamy argument pre custom riešenie.

### Gudslip — hook ako otázka ⚠️

32 produktov, 3 vypredané (okuliare proti modrému svetlu), ceny 69 až 3 999 Kč. Web je rýchly (0.23 s), takže výkonnostný uhol nesedí. Zostáva **spotrebný charakter produktu bez predplatného**. Pozor: `products.json` nevracia `selling_plan` spoľahlivo, takže absencia predplatného je **indícia, nie overený fakt** → v správe formulované ako otázka („nenašiel jsem", nie „nemáte"), aby sa nedalo vyvrátiť.

### Resty — najslabší fit ⚠️

Web je v angličtine (`lang="en"`), Trustpilot 91 recenzií, doprava od 20 €. Pravdepodobne necieli na SK/CZ, čím sa stráca výhoda „sme lokálni". Kontaktný mail sa nepodarilo nájsť (na webe je len placeholder `you@example.com`). **Zaradený ako tretí v poradí**, správa pripravená v EN.

## Vylúčení

- **naturdrop.cz** — HTTP 402, zmrazený Shopify za neplatenie. Mŕtvy biznis.
- **biohacker.sk** — nedostupný.
- **maluna.sk** — bot wall, neoverené.
- Veľkí predajcovia cudzích značiek (GymBeam, Brainmarket, Aktin, Nutrend, Ronnie, Pilulka…) — resellery, nie DTC značky, mimo ICP.

## ⚠️ Konflikt záujmov

`nosky.cz`, `pekne.eu`, `gudslip.cz`, `hevisleep.sk` a `feelresty.com` sú **navzájom konkurenti v tej istej nike**. Ak niektorý podpíše, ostatní sú konfliktní. Odporúčanie: neposielať všetkým naraz, ísť po jednom podľa sily hooku (Hevi → Gudslip → Resty) a čakať na odpoveď.

Marko uvádza, že **pekne.eu už oslovil** — vo vaulte o tom nie je záznam. Doplniť pred ďalším krokom.

## Správy (fáza 1, bez pitchu)

Kanál: **email deň 0, IG DM deň 3–4** ak mlčí, sekvenčne ([[jason-fry]] „si bot?"). Kde mail chýba (Pekne, Resty), len DM. Verzia opravená 20.7. — pôvodný Hevi draft obsahoval vetu "Robíme e-shopy", čo porušuje pravidlo fázy 1 (žiadna zmienka o službe); odstránené.

### 1. Pekne (SK) — len IG DM `@pekne.eu`

> Ahoj, sledujem Pekne. Otvoril som web na mobile a načítaval sa mi dlho. Pozrel som zdrojový kód — beží tam vyše 100 scriptov naraz na jednej stránke. Viete o tom?

### 2. Hevi (SK) — email `podpora@hevisleep.sk`

> **Predmet:** hevisleep.sk a .cz
>
> Dobrý deň,
>
> všimol som si, že hevisleep.sk a .cz bežia ako dva samostatné Shopify obchody — rovnaké produkty, ale každý má vlastné ID.
>
> Znamená to, že každú zmenu v katalógu robíte dvakrát?
>
> Marko

Hevi — IG DM `@hevisleep.sk` (ak mail mlčí):

> Ahoj, všimol som si, že Hevi má .sk aj .cz ako dva oddelené obchody na Shopify — rovnaké produkty, iné ID. Robíte každú zmenu v katalógu dvakrát?

### 3. Gudslip (CZ) — email `shop@gudslip.cz`

> **Předmět:** opakované objednávky
>
> Dobrý den,
>
> pásky na nos jsou spotřební zboží — kdo si zvykne, kupuje je znovu.
>
> Na Gudslipu jsem ale nikde nenašel předplatné ani opakovanou objednávku. Je to záměr?
>
> Marko

Gudslip — IG DM `@gudslip.cz` (ak mail mlčí):

> Ahoj, pásky na nos jsou spotřební zboží — kdo si zvykne, kupuje je znovu. Nenašel jsem u vás předplatné ani opakovanou objednávku. Záměr, nebo zatím nedošlo?

### 4. Resty (EN) — len IG DM `@feelresty`

> Hi, you sell magnetic nasal strip refills — so customers already come back for more. But the refill itself is still a one-off purchase, no subscription option anywhere I could find. Deliberate, or just haven't gotten to it?

## Stav

| Značka | Odoslané | Kanál | Reakcia |
|---|---|---|---|
| Pekne | — | — | — |
| Hevi | — | — | — |
| Gudslip | — | — | — |
| Resty | — | — | — |

## Zdroje

- Vlastné overenie `curl` + `/products.json`, 2026-07-20 (v session)
- Firecrawl search, 9 dotazov, 2026-07-20
- [[icp-dtc-znacky-sk-cz]] — definícia ICP v2 a research infra
- [[cold-outreach-pipeline]] — poznatky #1–#8
