---
type: organization
created: 2026-07-13
updated: 2026-07-13
aliases: [Konkurencia FitnessMenu]
tags: [fitnessmenu, konkurencia]
---

# Konkurencia v dealu FitnessMenu

Agentúra/tím súťažiaci s nami o eshop [[boris|Borisa]] ([[fitnessmenu]]). Pravdepodobne prišli cez Borisovho nedôveryhodného spoločníka. Postavili aktuálny fitnessmenu.eu.

## Ich pozícia (k ~2026-07-06)

- **Náskok:** riešia to vyše mesiaca, ~5 stretnutí s Borisom, viac hotového (aj infraštruktúrne), viac info o jeho požiadavkách. Development nezastavili.
- **Model:** úkolový marketing — zaplatené dostanú, až keď sa niečo predá navyše. Pre Borisa atraktívne (žiadny upfront risk). Pokrývajú marketing aj eshop; my len eshop.
- **Plánované platby:** Stripe, stravné lístky (Edenred, Up, Doxx, Ticket Restaurant) cez ComGate, prevod.
- Nevieme, koľko si pýtajú, ani či Boris pozná obe ceny navzájom.
- Mali sme rovnaké nápady nezávisle (online platby, subscriptions).

## Slabiny — analýza fitnessmenu.eu

Produkt je vibecoded AI platforma, nie reálne postavený produkt. Kritické nálezy (P0):

- **5 rôznych s.r.o. na jednom eshope** — objednávkový formulár ukazuje „Real Estate Factory s. r. o.", košík INVIZ, cenník Maboma Holding… Právny a merchant-of-record problém; Boris o tom zrejme nevie.
- **Mŕtve SEO:** 238 mestských stránok s pokazenou diakritikou v URL („/uabokreky-nad-nitrou") — investícia z veľkej časti premrhaná.
- **3 rôzne ceny dopravy** na 3 stránkach; hero cena „od 11,90 €" vs. reálne minimum 18,40 € (anchor-then-shock).

Závažné (P1): konfigurátor oddelený od menu; alergie sa riešia až po platbe; trial neprechádza do subscription (len 15 € kupón); žiadny Apple/Google Pay napriek Stripe.

**Čo im funguje** (nepodceniť): dobre navrhnutý 4-krokový konfigurátor (kalórie pomenované cieľom), skip dňa → kredit, automatická substitúcia pri alergiách, stravné lístky pre firemných zákazníkov.

*Limit analýzy: robená zo server-rendered HTML bez JS — checkout, mobil a platobná brána neoverené.*

## Ako proti nim hráme

Neútočiť — ukázať vedľa seba (A/B test). Argument: „bezpečné, funkčné, jeden právny subjekt, jeden zdroj pravdy — my by sme toto nikdy nedoručili." A split návrh: oni dostanú novú značku + marketing (čo chcú), my FitnessMenu eshop. Detaily v [[fitnessmenu]].

## Zdroje

- [[Konkurencia - eshop analyza|Konkurencia — eshop analýza]] (výťah)
- [[ai analysis output|AI analysis output]] (plná analýza) + [[Prompt engineering|prompt]]
- [[Ako porazit konkurenciu|Ako poraziť konkurenciu]]
