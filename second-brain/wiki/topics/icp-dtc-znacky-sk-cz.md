---
type: answer
status: active
created: 2026-07-20
updated: 2026-07-20
aliases: [ICP DTC značky SK/CZ, ICP v2, DTC brandy]
tags: [cart-design, cold-outreach, icp, sk, cz]
---

# ICP v2 — DTC značky SK/CZ (performance & lifestyle)

Druhý ICP pre cart.design, definovaný 2026-07-20 na Markov podnet („napísať slovenským brandom ako nosky.cz / pekne.eu"). **Nenahrádza** [[cold-outreach-pipeline|ICP v1]] (handmade makeri s rozbitým kanálom) — beží popri ňom ako samostatná línia.

## Prečo je toto iný ICP než v1

| | ICP v1 (batch 1–8) | ICP v2 (tento) |
|---|---|---|
| Kto | solo handmade maker | mladá DTC značka, 1 hero produkt |
| E-shop | rozbitý / chýba / mŕtva doména | **funkčný, na Shopify** |
| Hook | „tvoj web nefunguje" | „tvoj web funguje, ale brzdí ťa" |
| Rozhoduje | remeselník, netechnik | marketingovo zdatný zakladateľ |
| Grade | prvý e-shop | redesign / retainer |

**Dôsledok:** doterajší messaging playbook sa sem nedá skopírovať. Hook „site down" tu neexistuje — pain point musí byť **ekonomický alebo funkčný**, nie technický výpadok.

## Ako vznikol — korekcia zadania

Markova pôvodná formulácia znela ako „pekné slovenské dizajnové značky". Overenie oboch referenčných webov (2026-07-20, curl + `products.json`) ukázalo niečo iné:

| | nosky.cz | pekne.eu |
|---|---|---|
| Hero produkt | športové pásky na nos (399 Kč / 30 ks) | Pekne™ StripsClub Pack (29.95 €) |
| Doplnky | jedálničky, tréningové plány (299–399 Kč) | ebooky: Biohacking 101, Dopamin Detox (4.95–6.95 €) |
| Platforma | Shopify | Shopify |
| Katalóg | 22 produktov | 15 produktov |
| Jazyk | `cs` | — |

**Nie sú to dizajnové značky — sú to priami konkurenti v tej istej nike** (nosné pásky / biohacking performance). Marko teda intuitívne netrafil estetickú kategóriu, ale **obchodný model**: DTC značka s jedným opakovane nakupovaným produktom, digitálnymi doplnkami a marketingom cez IG/TikTok. To je pre targeting oveľa lepšie — dá sa podľa toho cielene hľadať.

## Definícia ICP v2

**Firma:** DTC značka s vlastným (nie preproduktovým) produktom, 1 hero produkt + odvodené balíčky/digitálne doplnky. Vlastný funkčný e-shop, prevažne Shopify (alebo Shoptet). SK + CZ trh. Vek značky ~1–5 rokov.

**Preukázaný dopyt (aspoň 1):**
- 5K+ IG alebo TikTok followerov s aktívnym postovaním (posledný post do 14 dní)
- platená reklama v obehu (FB/IG Ad Library — dôkaz, že už míňajú na akvizíciu)
- viditeľné kolaborácie so športovcami/tvorcami, press, retail listing
- rozšírený katalóg (pribúdajú bundly, edície, digitálne produkty = rastú)

**Kvalifikačná bolesť (aspoň 1 — všetky štyri schválené Markom 20.7.):**

1. **Prerástli šablónu** — brand v reklame a na IG je ostrý, web vyzerá ako default Shopify téma. Vizuálny rozpor medzi tým, ako značka komunikuje, a ako vyzerá jej checkout.
2. **Platforma limituje funkčne** — chcú konfigurátor, bundle logiku, predplatné, vernostný program, viacjazyčnosť, B2B ceny; šablóna to nevie alebo to lepia z 5 platených appiek.
3. **Výkon / rýchlosť / mobil** — merateľné, dá sa doložiť číslom už v prvej správe.
4. **Rast bez infraštruktúry** — značka sa posunula (retail, export, nová kategória), web zaostal.

**Diskvalifikátory:**
- posledný IG post starší než ~30 dní (poznatok #5 z [[outreach-batch-8]] — spiaci účet nie je lead)
- dropshipping / reseller bez vlastného produktu
- už majú custom-coded web (headless, Next.js na vlastnej doméne bez Shopify frontendu)
- korporát s interným IT / existujúcou agentúrou na retaineri

**Persóna:** zakladateľ 25–40, marketingovo zdatný (rozumie CPA, ROAS, konverzii), **nie je technik**. Web si postavil sám alebo cez lacného freelancera na začiatku a odvtedy ho lepí. Bolí ho konverzia a závislosť na appkách, nie estetika ako taká. **Argumentuje sa mu číslami, nie krásou.**

## Prečo custom kód (pitch logika)

cart.design predáva **flexibilitu custom kódu**, nie Shopify ([[cart-design-custom-code|pravidlo]]). Pri ICP v2 to sedí prirodzene, lebo:

- **Opakovaný nákup bez predplatného.** Nosné pásky sú spotrebný tovar — zákazník ich kupuje znova. Ak značka nemá predplatné, necháva na stole predvídateľný príjem. Shopify to rieši appkou s mesačným poplatkom + províziou z každej objednávky; custom to má natívne. *(Signál „subscription/selling_plan" sa v HTML oboch webov objavuje, ale môže ísť o boilerplate Shopify témy — **neoverené**, treba potvrdiť v reálnom checkoute pred použitím v správe.)*
- **App tax.** Typická rastúca Shopify značka platí 5–15 appiek; custom riešenie tieto náklady odstraňuje. Argument sa dá vyčísliť v eurách mesačne.
- **Rýchlosť.** `pekne.eu` má **111 `<script>` tagov**, `nosky.cz` **65** (overené 20.7.) — to je priama a merateľná brzda konverzie na mobile.

## Overený nález na referenčných značkách (k 2026-07-20)

- ~~**`pekne.eu` má prázdny `<title>`.**~~ **VYVRÁTENÉ 2026-07-20**, v ten istý deň. Titulok je v poriadku: *„Produkty pre lepší výkon, spánok, dýchanie a sústredenie. – Pekne"*. Pôvodný nález bola **chyba nástroja, nie chyba webu** — `grep -io '<title[^>]*>[^<]*'` nezachytí titulok, ktorý pokračuje na ďalšom riadku, čo Shopify témy bežne robia. Falošne to označilo 4 z 5 Shopify webov v dávke. **Titulky a čokoľvek v `<head>` parsovať v Pythone cez regex s `re.S`, nikdy riadkovým greplom.** Poznatok #3 z [[cold-outreach-pipeline]] (neoverený detail v správe) sa takmer zopakoval — tentokrát by hook vyvrátil prospekt jedným pohľadom na vlastnú záložku.
- **`nosky.cz` má v katalógu produkty za 0.00 Kč** („P.R. kartička", „Nosky s logem N") — PR/gifting riešený cez verejný katalóg. Funguje to, ale je to viditeľné zvonku.
- Ani jeden web nemá `hreflang` — pri CZ značke mierjacej na SK (a naopak) je to premárnený trh.

⚠️ Marko uvádza, že **`pekne.eu` už bol oslovený** — vo vaulte k tomu ale nie je záznam (žiadna stránka, žiadny riadok v pipeline). Pred odoslaním čohokoľvek doplniť, kedy a čo sa poslalo, nech nedôjde k duplicite.

## Research infraštruktúra

Trojvrstvový postup. Kľúčová zmena oproti batchom 1–8: **platforma a výkon sa dajú zistiť čistým `curl`-om**, bez Firecrawl tokenov aj bez Kimi WebBridge. Šetrí to Markovu usage (bolesť z [[flow-feedback|flow poznámok]]).

**Vrstva 1 — discovery (Firecrawl).** Hľadanie kandidátov. Poznatok #6 platí: Firecrawl instagram.com nescrapuje, profily sa dajú vyťažiť len z URL a `@mentions` v snippetoch. Zdroje kandidátov:
- Firecrawl search na CZ/SK DTC kategórie (doplnky výživy, performance, spánok, biohacking, kozmetika, fitness vybavenie)
- **FB/IG Ad Library** filtrovaná na SK/CZ — najlepší zdroj, lebo priamo dokazuje, že značka míňa na reklamu
- konkurenti už nájdených značiek (nosky.cz ↔ pekne.eu sú dôkaz, že nika má hráčov)
- SK/CZ Shopify značky cez `myshopify.com` odtlačok

**Vrstva 2 — kvalifikácia (curl, zadarmo).** Skript nižšie na každom kandidátovi: platforma, HTTP status, čas odozvy, počet scriptov, `<title>`, `hreflang`, veľkosť katalógu cez `/products.json`. Z toho vypadne bolesť #1–#3 automaticky.

**Vrstva 3 — verifikácia (Kimi WebBridge).** Len na tých, čo prešli vrstvou 2 — IG followers, dátum posledného postu, meno zakladateľa, kontakt. Toto je najdrahší krok, preto ide posledný.

### `stack.sh` — detekcia platformy a hygieny

```bash
#!/bin/bash
# stack.sh <domain>
UA="Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 Chrome/126 Safari/537.36"
d="$1"
html=$(curl -sL --max-time 20 -A "$UA" "https://$d")
code=$(curl -sL -o /dev/null -w "%{http_code} %{time_total}s" --max-time 20 -A "$UA" "https://$d")

plat="?"
echo "$html" | grep -qi "myshoptet.com\|Shoptet"            && plat="Shoptet"
echo "$html" | grep -qi "cdn.shopify.com\|Shopify.theme"    && plat="Shopify"
echo "$html" | grep -qi "wp-content/plugins/woocommerce"    && plat="WooCommerce"
echo "$html" | grep -qi "static1.squarespace.com"           && plat="Squarespace"
echo "$html" | grep -qi "wixstatic.com"                     && plat="Wix"
echo "$html" | grep -qi "_next/static\|__NEXT_DATA__"       && plat="$plat +Next.js"

echo "$d | $code | $plat | scripts: $(echo "$html" | grep -co '<script')"
echo "$html" | grep -io '<title[^>]*>[^<]*' | head -1
```

Katalóg (funguje na každom Shopify bez API kľúča):
```bash
curl -s "https://<domain>/products.json?limit=250" | python3 -c "import json,sys; d=json.load(sys.stdin)['products']; print(len(d))"
```

**Prahy na kvalifikáciu:** čas odozvy > 1.5 s **alebo** `<script>` tagov > 80 **alebo** chýbajúci/prázdny `<title>` **alebo** chýbajúci `hreflang` pri cezhraničnom predaji → kandidát má doložiteľnú bolesť.

## Kanál a sekvencia

Marko zvolil „oboje naraz" (mail + IG). **Odporúčanie: sekvenčne, nie súčasne** — Jason Fry sa pýtal, či Marko nie je bot, práve kvôli duplicitnej správe mail+IG v ten istý deň ([[jason-fry]]).

1. **Deň 0 — email** na `info@` / zakladateľa. Priestor na doloženie čísla, nižšie riziko IG banu (batch 8: 2 účty blokovali DM).
2. **Deň 3–4 — IG DM**, ak email mlčí. Krátky, s explicitným odkazom: *„písal som aj mailom, neviem či dorazil"* — priznanie duplicity odstráni bot efekt.
3. Rovnaký podpis na oboch kanáloch.

## Logika správy

ICP v1: *tvoj dopyt je reálny → tvoj kanál ho nezvláda → otázka.*
**ICP v2:** *tvoj brand/marketing je dobrý (uznanie) → ale [konkrétne merateľné číslo] ti z toho uberá (doložený postreh) → otázka.*

Stále dvojfázovo (otvárač bez predaja → pitch až po reakcii), stále 5–8 viet, krátke vety ([[flow-feedback]]: „velmi kratke vety funguju"), žiadne dlhé pomlčky.

## Otvorené otázky

- Cena: ICP v2 je redesign/retainer-grade, nie „prvý e-shop". Cenník z by_alisha (mesačne bez setup fee) sem nemusí sedieť — vyriešiť pred prvým pitchom.
- Referencie: títo klienti sa budú pýtať na portfólio tvrdšie než handmade makeri. Čo im ukážeme?

## Zdroje

- Overenie `nosky.cz` a `pekne.eu` — curl + `/products.json`, 2026-07-20 (v tejto session)
- [[cold-outreach-pipeline]] — ICP v1, pipeline, poznatky #1–#6
- [[cold-outreach-manual]] — dvojfázový systém, Origami princípy, pravidlo overenia hookov
- [[flow-feedback]] — Markove poznámky k nástrojom a usage
- [[outreach-batch-8]] — poznatok #5 (spiaci účet), #6 (Firecrawl vs. IG)
