---
type: project
status: active
created: 2026-07-20
updated: 2026-07-20
aliases: [Batch 10, Zastarané SK e-shopy, ICP v3]
tags: [cart-design, cold-outreach, sk, redesign]
---

# Outreach batch 10 — zastarané SK e-shopy (email)

Markov podnet 20.7.: *„poslať ďalšie maily do Slovenska, nájsť horšie e-shopy, ktoré si zaslúžia lepší"*.

Dávka zámerne **nemieri na ďalších drobných handmade predajcov** (tých pokrývajú batche 1–8, [[cold-outreach-pipeline|ICP v1]]), ale na **etablované SK firmy s reálnym obratom a objektívne zastaraným webom** — redesign grade. Kanál: **email** (Marko explicitne žiadal maily).

## Kvalifikačné pravidlo dávky

Vychádza z **poznatku #1** ([[cold-outreach-pipeline]]): *„škaredý e-shop sám o sebe nie je pain point"*. darcekove_kytice mala zlý kanál, ale objem, ktorý jej stačil — pitch odmietla. Preto dvojitý filter:

1. **Doložiteľná technická chyba**, ktorú si majiteľ vie sám overiť za 5 sekúnd, a
2. **dôkaz živého biznisu** (skladové stavy, novinky, aktívny katalóg, kamenná prevádzka).

## Metodika (100 % zadarmo, bez Firecrawl kreditov na kvalifikáciu)

Firecrawl len na discovery (7 dotazov, 7 kategórií) → **kvalifikácia čistým Pythonom + `curl`** (skript `qualify.py`, rozšírenie `stack.sh` z [[icp-dtc-znacky-sk-cz]]). Preverených **~50 domén**, kvalifikovaní **4**.

Nové kontroly oproti `stack.sh`: `<meta viewport>` (mobilná responzivita), platnosť SSL certifikátu, deklarovaný charset, verzia jQuery, počet `<table>`, prítomnosť `og:` tagov, opakované meranie rýchlosti pod **mobile User-Agentom**.

### Cielené kategórie

Zámerne odvetvia, kde býva starý web + reálny obrat: rybárske · včelárske · modelárske · chovateľské potreby · záhradná technika · zdravotnícke pomôcky · papiernictvo.

## ⚠️ Tri falošné hooky, ktoré sme počas dávky zamietli

Zapísané, lebo každý z nich by v správe vybuchol.

**1. `windows-1250` kódovanie nie je chyba.** `sports.sk`, `hacik.sk`, `krmiva.sk`, `miraoffice.sk`, `vcelieule-bozik.sk` vracali v mojom výpise rozsypaný text („Ryb�rske potreby"). Vyzeralo to ako pokazená diakritika na webe. Overenie hlavičiek ukázalo, že charset je **korektne deklarovaný** v HTTP aj v `<meta>` — v prehliadači sa zobrazuje správne. Bola to **chyba môjho dekódovania, nie webu**. Priama repríza poznatku o `pekne.eu` prázdnom `<title>`.

**2. jQuery 1.11.3 je default Shoptetu.** Objavil sa na 12 weboch v dávke — na všetkých Shoptet. Nie je to zanedbanie konkrétnej firmy, je to platformový boilerplate. Ako hook bezcenné.

**3. Jednorazové meranie rýchlosti klame.** `e-luma.sk` (3.11 s) a `ortokomplet.sk` (1.51 s) pri prvom meraní prešli prahom, pri 4 opakovaniach spadli na 0.53 s / 0.63 s. **Oba vyradené.** Pravidlo: rýchlosť merať **minimálne 4×** a použiť len vtedy, ak je pomalá **konzistentne**.

## Vyradení kandidáti (výber)

- **`rybarskepotreby-poprad.sk`** — technicky ideálny profil (neplatný SSL: cert je `*.webygroup.sk`, hostname mismatch → prehliadač zobrazí varovanie cez celú stránku; navyše žiadny viewport). **Ale nie je to e-shop** — je to SEO satelit odkazujúci na `hacik.sk` a `rybarskepotreby-eshop.sk`. Doorway stránka bez vlastného dopytu. *Poznatok #9 nižšie.*
- **Shoptet weby** (okfish, carpio, esox-rybar, outdoorfish, htmodel, ajtech, boel, kasumex, mojadielna, polnosevshop, zahrada-plantex, zahradnictvobrozany, zuzalo) — rýchle, responzívne, moderné. Šablónové, ale funkčné → mimo tejto dávky.
- **`rcprofi.sk`** — Next.js, 231 scriptov. Už má moderný custom stack, mimo ICP.
- **`vcely-eshop.sk`** — Webnode, ale minimálny obsah, nevyzerá na živý biznis.

## Leady

| # | Firma | Kategória | Platforma | Hook (overený 20.7.) | Kontakt | Sila |
|---|---|---|---|---|---|---|
| 1 | **Tatramodel** (tatramodel.sk) | modelárstvo | vlastný/starý | **žiadny `<meta viewport>`** — web nemá mobilnú verziu; jQuery **1.7.1** (2011) | tatramodel@tatramodel.sk | ⭐ najsilnejší |
| 2 | **Vcelo** (vcelo.sk) | včelárstvo | vlastný | **3.7–4.2 s** načítanie na mobile (4 merania, konzistentne) | obchod@vcelo.sk · +421 949 850 585 | silný |
| 3 | **Konvička** (konvicka.sk) | záhradkárstvo | WooCommerce | **2.3–4.2 s** na mobile (4 merania, vždy > 2 s) | info@konvicka.sk · +421 915 232 662 | stredný |
| 4 | **Neoprot** (neoprot.sk) | ortopedické pomôcky | vlastný | **2.4–2.7 s** na mobile (konzistentne) | sekretariat@neoprot.sk · +421 2 501 16 250 | ⚠️ slabý fit |

### 1. Tatramodel — hook overený ✅ (najsilnejší v dávke)

Jediný web z ~50 preverených, ktorý **vôbec nemá `<meta name="viewport">`**. Dôsledok je viditeľný a neodškriepiteľný: na telefóne sa stránka vykreslí v desktopovej šírke a zákazník musí prstami zväčšovať. Pri ~70 % mobilnej návštevnosti je to priama strata objednávok.

Druhotne: **jQuery 1.7.1** — vydané 2011, teda web má kostru starú ~15 rokov.

**Prečo je hook dobrý:** majiteľ si ho overí za 5 sekúnd na vlastnom telefóne. Nedá sa odbiť „mne to funguje" (poznatok #4), lebo naopak — on to na mobile videl už stokrát a vie, že je to nepohodlné. Správa len pomenuje, čo dávno cíti.

Živý biznis: skladové stavy + sekcia noviniek, obchod beží od 1991 (tvrdenie webu).

### 2. Vcelo — hook overený ✅

Načítanie **3.71 / 3.83 / 4.02 / 4.22 s** pod mobile User-Agentom — konzistentne pomalé, žiadny výkyv. 285 kB HTML, 27 scriptov, 8 `<table>` v layoute. Viewport má, takže responzívny je; problém je čisto rýchlosť.

Živý biznis: 7 skladových indikátorov, novinky, tri telefónne čísla (= viac ľudí na zákazníkoch).

### 3. Konvička — hook overený ⚠️ s výhradou

**2.33 / 2.45 / 3.25 / 4.17 s** — vždy nad 2 s, ale rozptyl je veľký. V správe preto formulovať ako **rozsah a pozorovanie**, nie ako jedno tvrdé číslo, aby sa nedalo vyvrátiť jedným rýchlym načítaním. WooCommerce, 62 scriptov, 14 skladových indikátorov (najživší katalóg v dávke).

### 4. Neoprot — ⚠️ najslabší fit, poslať posledný alebo vôbec

Rýchlosť je konzistentne pomalá (2.4–2.7 s), ale **nie je to klasický e-shop** — je to ortopedicko-protetická firma, kde predaj beží pravdepodobne cez zdravotné poisťovne a osobné merania, nie cez košík. Žiadne skladové stavy. Odporúčam **odložiť**, kým nebude overené, či vôbec predávajú online.

## Správy (variant B — kombinovaná, podľa [[outreach-batch-9]])

Kostra: predstavenie → rapport → **1 konkrétny overený nález** → ponuka prvého vylepšenia zadarmo → mäkký CTA → podpis **Marek**. Krátke vety, žiadne dlhé pomlčky.

⚠️ Mená majiteľov **nie sú overené** → správy oslovujú bez mena. Ak sa dá lacno zistiť (Impressum, IG bio), doplniť pred odoslaním.

### 1. Tatramodel — `tatramodel@tatramodel.sk`

> **Predmet:** Tatramodel na mobile
>
> Dobrý deň,
>
> som Marek a spolu s Adamom vytvárame a spravujeme e-shopy.
>
> Nebudem chodiť okolo horúcej kaše. Tatramodel som si našiel pri hľadaní modelárskych potrieb a zaujalo ma, že obchod funguje od roku 1991. To je na tomto trhu vzácne.
>
> Prešiel som si web aj po technickej stránke. Všimol som si, že stránka nemá mobilnú verziu — na telefóne sa načíta v šírke ako na počítači a treba ju prstami zväčšovať. Skúste si ju otvoriť na mobile, uvidíte to hneď.
>
> Dnes chodí väčšina ľudí na e-shopy z telefónu, takže je to škoda pri sortimente, ktorý máte.
>
> Máme pár konkrétnych nápadov, ako to napraviť. Prvé vylepšenie spravíme bez nároku na odmenu — ak budete spokojný, potešíme sa referencii, ak nie, ostane vám aspoň zoznam odporúčaní.
>
> Mali by ste 15 minút na krátky telefonát?
>
> Marek

### 2. Vcelo — `obchod@vcelo.sk`

> **Predmet:** Rýchlosť vcelo.sk na mobile
>
> Dobrý deň,
>
> som Marek a spolu s Adamom vytvárame a spravujeme e-shopy.
>
> Nebudem chodiť okolo horúcej kaše. Vcelo som si prezeral dlhšie a páči sa mi, aký široký sortiment pre včelárov držíte na sklade.
>
> Prešiel som si web aj po technickej stránke. Meral som načítanie stránky na mobile štyrikrát a zakaždým to trvalo skoro štyri sekundy. To je dosť dlho — časť ľudí odíde skôr, než sa im stránka vôbec ukáže.
>
> Máme pár konkrétnych nápadov, ako to zrýchliť. Prvé vylepšenie spravíme bez nároku na odmenu — ak budete spokojný, potešíme sa referencii, ak nie, ostane vám zoznam odporúčaní.
>
> Mali by ste 15 minút na krátky telefonát?
>
> Marek

### 3. Konvička — `info@konvicka.sk`

> **Predmet:** Načítanie konvicka.sk
>
> Dobrý deň,
>
> som Marek a spolu s Adamom vytvárame a spravujeme e-shopy.
>
> Nebudem chodiť okolo horúcej kaše. Konvičku som si prezeral a je vidieť, že katalóg reálne žije — skladové stavy sú aktuálne, čo pri záhradkárskom sortimente nie je samozrejmosť.
>
> Prešiel som si web aj po technickej stránke. Načítanie na mobile mi kolísalo medzi dvomi a štyrmi sekundami. Nie je to katastrofa, ale v sezóne, keď chodí najviac ľudí naraz, býva práve toto miesto, kde sa objednávky strácajú.
>
> Máme pár konkrétnych nápadov, ako to ustáliť. Prvé vylepšenie spravíme bez nároku na odmenu — ak budete spokojný, potešíme sa referencii, ak nie, ostane vám zoznam odporúčaní.
>
> Mali by ste 15 minút na krátky telefonát?
>
> Marek

### 4. Neoprot — ⏸️ pozdržané

Správa zámerne nenapísaná. Najprv overiť, či Neoprot vôbec predáva cez web (viď vyššie). Ak áno, hook na rýchlosť je pripravený.

## Nový poznatok

**Poznatok #9 — technicky rozbitý web ešte neznamená biznis.** `rybarskepotreby-poprad.sk` mal najlepší technický profil celej dávky (neplatný SSL + žiadny viewport + 15 rokov starý layout), ale išlo o **SEO satelit** odkazujúci na iné e-shopy toho istého prevádzkovateľa, nie o firmu s vlastným dopytom. Rozšírenie poznatku #5 („spiaci účet nie je lead"): pri weboch kontrolovať **odchádzajúce odkazy** — ak stránka vedie hlavne na iné domény, je to doorway page, nie obchod.

## Stav

| # | Firma | Hook overený | Odoslané | Reakcia |
|---|---|---|---|---|
| 1 | Tatramodel | ✅ 2026-07-20 | — | — |
| 2 | Vcelo | ✅ 2026-07-20 | — | — |
| 3 | Konvička | ✅ 2026-07-20 | — | — |
| 4 | Neoprot | ⏸️ pozdržané | — | — |

**Nič nie je odoslané** — všetky tri správy čakajú na Markovo schválenie.

⚠️ Pravidlo z [[cold-outreach-manual]] §4: hook overiť **v deň odoslania**. Ak sa posiela neskôr než 20.7., prehnať `qualify.py` znova (povel „over batch 10").

## Zdroje

- Vlastné overenie: Firecrawl search (7 dotazov) + `qualify.py` (Python/`curl`), 2026-07-20, v tejto session
- [[cold-outreach-pipeline]] — poznatky #1, #4, #5, ICP v1
- [[icp-dtc-znacky-sk-cz]] — `stack.sh`, trojvrstvová research infra
- [[outreach-batch-9]] — variant B (kombinovaná správa)
- [[cold-outreach-manual]] — pravidlá otváračov, Origami princípy
