---
type: project
status: active
created: 2026-07-20
updated: 2026-07-20
aliases: [Gudslip.cz]
tags: [cart-design, cold-outreach, dtc, spánok, Czech]
---

# Gudslip (gudslip.cz)

## Info

| | |
|---|---|
| **Firma** | Gudslip.cz — pásky na nos + doplnky pre spánek a regeneráciu |
| **Trh** | Česko (čeština) |
| **Platforma** | Shopify, 32 produktov |
| **Kontakt** | `shop@gudslip.cz` · **+420 722 287 570** (WhatsApp/SMS priamo) · @gudslip.cz |
| **ICP** | [[icp-dtc-znacky-sk-cz|ICP v2]] — DTC značka s funkčným Shopify, spotrebný tovar bez predplatného |

## Hook (overený 2026-07-20)

**Spotrebný tovar bez predplatného.** Pásky na nos sú produkty, ktoré zákazník kupuje opakovane — kto si zvykne, kupuje ich znova. Na Gudslipu nikde ale nie je predplatné ani opakovaná objednávka, takže opakovaný nákup ponecháva zákazníka, nech si sám spomenie.

Overenie: `curl` + `/products.json`, bez predplatného tagov v katalógu ([[outreach-batch-9]] poznámka: `selling_plan` v Shopify sa nepodarilo zistiť spoľahlivo bez API, takže táto analýza je indíciou, nie faktom — formulované ako otázka v správe, nie tvrdenie).

## Stav konverzácie

| Dátum | Kanál | Obsah |
|---|---|---|
| 2026-07-20 | email `shop@gudslip.cz` | **POSLANÉ**: kombinovaná správa (variant B) — rapport + technický nález + ponuka prvého vylepšenia zadarmo + CTA na 15min call. Subjekt: "Pri prechádzaní Gudslipu sme našli pár vecí" |
| 2026-07-20 | WhatsApp `+420 722 287 570` | **DRAFT PRIPRAVENÝ**, Marko posiela osobne — krátky draft (50 slov) s priznaním duplicity s mailom. |
| — | — | Čaká sa na prvú odpoveď. |

## Návrh — fáza 1 (odoslaný)

**Kanál:** email `shop@gudslip.cz`

**Predmet:** Pri prechádzaní Gudslipu sme našli pár vecí

> Ahoj,
>
> som Marek a spolu s Adamom vytvárame a spravujeme e-shopy.
>
> Nebudem chodiť okolo horúcej kaše — Gudslip sledujeme dlhšie a páči sa nám, akú komunitu okolo spánku a regenerácie budujete na českom trhu.
>
> Prešli sme si e-shop aj po technickej stránke. Pásky na nos sú spotrebný tovar — kto si zvykne, kupuje ich znova. Nikde sme však nenašli predplatné ani opakovanú objednávku, takže opakovaný nákup teraz necháva zákazníka, nech si spomenie sám.
>
> Máme pár konkrétnych nápadov, ako by sa to dalo doriešiť. Prvé vylepšenie spravíme bez nároku na odmenu — ak budeš spokojný, budeme radi za referenciu, ak nie, ostane ti zoznam odporúčaní.
>
> Máš 15 minút na krátky call?
>
> Marek

**WhatsApp draft (+420 722 287 570):**

> Ahoj, som Marek, robíme s Adamom e-shopy. Dnes som ti aj mailom napísal pár postrehov ku Gudslipu — hlavne že pásky na nos sú spotrebný tovar, ale nikde som nenašiel predplatné na opakovaný nákup. Mal by si 15 min na krátky call?

## Archiv (raw sources)

Überenie: `curl https://gudslip.cz` + `curl https://gudslip.cz/products.json`, 2026-07-20, [[outreach-batch-9]] zápisy.

## Zdroje

- [[outreach-batch-9]] — batch informácie, overenie, výber variantu B
- [[icp-dtc-znacky-sk-cz]] — ICP v2 definícia
- [[cold-outreach-manual]] — variant B (kombinovaná správa)
