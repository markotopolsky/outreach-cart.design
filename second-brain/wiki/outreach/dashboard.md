---
type: topic
status: active
created: 2026-07-21
updated: 2026-08-03
aliases: [Dashboard, Outreach dashboard, Prehľad outreachu]
tags: [cart-design, cold-outreach, dashboard]
---

# Outreach dashboard

Jedna stránka na otázku „ako to ide s leadmi a čo ľudia odpisujú". Zdroj pravdy zostávajú batch
stránky a `## Komunikácia` na project stránkach — toto je len ich sčítanie. Čísla k **2026-08-03**.

> 📥 **3.8. — ingest IG inboxu (Kimi WebBridge) + Gmailu, po 10-dňovej medzere.** Nové odpovede:
> [[wiki/projects/orox-leather-co|Orox Leather Co]] a [[wiki/projects/gems-of-california|Gems of
> California (Miners Ink)]] reagovali pozitívne (25.7., 27.7.); [[wiki/projects/biorythme|biorythme]]
> potvrdila pain point na IG (25.7.) a graduje z `prospects/` na `projects/`; [[wiki/projects/pekne|Pekne]]
> odmietol mailom (20.7., objavené teraz) = **+4 noví respondenti**. [[lobo-gun-leathers|Lobo Gun
> Leathers]] definitívne odmietol („No we are good", ~28.7.) → status `done`.
> **Email audit:** Gmail má výrazne viac odoslaných mailov než táto stránka evidovala (dôvod: kanál
> „Email" nižšie bol počítaný len z toho, čo bolo zapísané do batch stránok ručne, nie z reálnej
> schránky) — [[chuck-richards-knives|Chuck Richards]] mal celé 4-správové emailové vlákno
> zaznamenané v nesprávnom poradí (opravené), [[outreach-batch-10]] bol v skutočnosti **odoslaný
> 20.–21.7.** napriek explicitnej výhrade na stránke dávky proti forme správ. Detaily v §7.

> ⏸️ **Cold outreach je PAUSED od 2026-07-21.** Dôvod: pred ďalším odosielaním chceme vedieť, ktorý
> prompt píše najlepšie správy (eval), a mať skill files, ktoré držia správy tak, aby nezneli ako AI.
> **Živé vlákna bežia ďalej** — pauza sa týka len nových otváračov. Pripravené a zmrazené:
> [[outreach-batch-7]] (2 správy).
> **Výnimka 21.7.:** [[outreach-batch-12]] — Marko explicitne overridol pauzu pre celú dávku
> (37 leadov); podmienka obnovenia splnená, píše sa live variantom v2 (víťaz eval run 2).
> **Neoznačená druhá výnimka:** [[outreach-batch-10]] (3 SK maily) odišla 20.–21.7. bez zaznamenanej
> výnimky a bez odporúčaného prepisu — viď §7.

## 1. Čísla celkovo

| Metrika | Hodnota |
|---|---|
| Odoslané a doručené (overené) | **73** (+4: batch 10 ×3, biorythme — boli vedené ako „pripravené") |
| Odpovede na tieto | **22** (k 3.8., +4: Orox, Gems of California, biorythme, Pekne) |
| **Response rate (overená báza)** | **~30,1 %** |
| Odoslané vrátane [[outreach-batch-5]] (⚠️ nezaznamenané, ~21) | ~94 |
| Odpovede vrátane batch 5 (+8) | 30 |
| Response rate na celej báze | ~32 % |
| Nedoručené (IG blokoval DM) | 2 ([[outreach-batch-8]]: Dark Timber, Lord Leathercraft) |
| Pripravené, neodoslané | 2 (batch 7) |

⚠️ Aj tieto čísla podceňujú skutočný objem — pozri email audit v §7. Kanál „Email" v tabuľke nižšie
je známy nepresný smerom nadol.

Benchmark z Origami playbooku ([[cold-outreach-manual]]): špičkový cold email ~5 %. Sme rádovo vyššie —
ale vzorka je malá a väčšina odpovedí zatiaľ nekonvertovala na deal.

### Podľa typu hooku

Najdôležitejšia tabuľka v dashboarde — toto rozhoduje, čo písať ďalej.

| Typ hooku | Odoslané | Odpovede | RR | Kde |
|---|---|---|---|---|
| **SK hyper-personalizovaný** (konkrétny post/komentár) | 6 | 4 | **67 %** | [[outreach-batch-3]] |
| **Brand-first** (obdiv k remeslu, technická vec je vsuvka) | 40 | 12 | **30 %** | batch 2, 6, 8, 12 + Disciple |
| **Tech-first** (technický nález je hlavný obsah) | 16 | 1 | **6 %** | batch 1, 2, 6 |
| Kombinovaná správa (variant B) | 4 | 0 | 0 % | [[outreach-batch-9]] |
| SK email (keramika) | 2 | 0 | 0 % | [[outreach-batch-4]] |
| Markov vlastný otvárač | 1 | 1 | — | Drop Dead Candles |

**Záver zatiaľ:** brand-first porazil tech-first ~4:1 na väčšej vzorke, než keď sa experiment
vyhodnocoval naposledy (vtedy 3/6 vs. 1/6). Tech-first hook „tvoj web nefunguje" má navyše krátku
trvanlivosť a majiteľ ho vie odbiť — poznatok #4 v [[cold-outreach-pipeline]]. Kombinovaná správa
(variant B) zatiaľ nemá ani jednu odpoveď, ale 4 správy staré 1 deň nič nedokazujú.

### Podľa kanála

| Kanál | Odoslané | Odpovede | RR |
|---|---|---|---|
| Instagram DM | 64 | 18 | 28 % |
| Email | 5 | 0 | 0 % |

⚠️ Email je zatiaľ **neotestovaný**, nie zlý — 5 správ je príliš málo na záver. Jediná emailová odpoveď
v celom vaulte prišla od Nino Rostomashvili z nezaznamenaného batchu 5.

### Podľa jazyka/trhu

| Trh | Odoslané | Odpovede | RR |
|---|---|---|---|
| EN (US/UK/EU) | 57 | 14 | 25 % |
| SK/CZ | 12 | 4 | 33 % |

### Podľa dávky

| Dávka | Odoslané | Odpovede | Stav |
|---|---|---|---|
| [[outreach-batch-1]] | 5 | 0 | uzavretá |
| [[outreach-batch-2]] | 12 | 4 | uzavretá (tech/brand experiment) |
| [[outreach-batch-3]] | 6 | 4 | uzavretá — najlepšia dávka |
| [[outreach-batch-4]] | 2 | 0 | uzavretá |
| [[outreach-batch-5]] | ⚠️ ~21 nezaznamenané | 8 | odoslané, ale bez záznamu |
| [[outreach-batch-6]] | 15 | 3 | uzavretá |
| [[outreach-batch-7]] | 0 (2 pripravené) | — | ⏸️ zmrazená |
| [[outreach-batch-8]] | 18 (z 20, 2 blokované) | 4 | Nick Anger, Local Branch, Iron Grove odpísali (k 21.7.) |
| [[outreach-batch-9]] | 4 | 1 | Pekne odmietol mailom 20.7. (zaznamenané 3.8.) |
| [[outreach-batch-10]] | 3 (odoslané 20.–21.7., zaznamenané 3.8.) | 0 | čaká sa — odoslané napriek výhrade proti forme (variant B) |
| [[outreach-batch-11]] | 0 (3 kvalifikované, žiadne správy) | — | pripravená na písanie správ |
| [[outreach-batch-12]] | **5** z 37 (vlna 1, 21.–22.7.) | 1 | Ember odpísal; bulk, vlny 2 (20 🟡) a 3 (12 🔴) v príprave; pauza overridnutá Markom |
| Disciple Designed (18.6., pred vlnou) | 1 | 1 | živé vlákno |
| Drop Dead Candles (vlastný, 15.7.) | 1 | 1 | živé vlákno |

## 2. Prompt varianty

| Variant | Stránka | Odoslané | Odpovede | Stav |
|---|---|---|---|---|
| **A v2 — dvojfázový + skills** | [[opener-dvojfazovy-v2]] | 5 | 0 | ✅ **LIVE** — prvé odoslania 21.7. (batch 12 vlna 1) |
| A v1 — dvojfázový otvárač | [[opener-dvojfazovy-v1]] | 60 | 14 | baseline |
| B — kombinovaná správa | [[kombinovana-v1]] | 7 | 0 | ⚠️ needs rewrite |

Rozhodnuté v [[run-2026-07-21-zmrazene-spravy|run 2]] (21.7.) Markovým slepým zoradením 12 verzií.
Katalóg: [[wiki/outreach/prompts/index|prompts/index]].

## 3. Skills (pravidlá písania)

| Skill | Rieši | Stav |
|---|---|---|
| [[pis-ako-clovek]] | hlas — dlhá pomlčka, „Curious:", intenzifikátory, šablónové lichôtky | ✅ platí od 21.7. |
| [[citatel-nema-cas]] | štruktúra — háčik prvý, jedna otázka, dĺžka podľa kanála | ✅ platí od 21.7. |

Aplikujú sa na každú správu vrátane odpovedí v živých vláknach počas pauzy. Prehľad: [[wiki/outreach/skills/index|skills/index]].

## 4. Eval

| | |
|---|---|
| Metodika a behy | [[wiki/outreach/evals/index\|evals/index]] |
| Rubrika | [[rubric]] — 6 kritérií, max 12, seedované z poznatkov #1–#11 |
| **Run 1** — rubrika vs. realita | ✅ hotový: rubrika **nepredpovedá odpovede** (8,1 vs. 8,0 na 17 správach) → prehodená na podlahu kvality |
| **Run 2** — slepý výber | ✅ hotový: **A+skills vyhral** → [[opener-dvojfazovy-v2\|v2]] je `live`. Rubrika trafila najhoršiu verziu 4/4, najlepšiu 2/4 |
| Kľúčové číslo | **88 % odoslaných správ nesie aspoň jeden AI signál**, 41 % tri a viac |
| Najväčšie riziko | akútnosť pain pointu = **0** pri oboch SK leadoch v run 2 (poznatok #1) |

## 5. Živé vlákna (pauza sa ich netýka)

| Lead | Posledný krok | Čaká sa na | Priorita |
|---|---|---|---|
| [[chuck-richards-knives]] | follow-up napísaný 3.8., **čaká ako DRAFT v Gmaile** (Gmail API neposiela) | **Marko: kliknúť Send na drafte** | 🔥 **qualified** — sám si vypýtal email |
| [[wiki/projects/by-alisha|by-alisha]] | Marko dal svoje číslo 21.7., ona „Napíšem 😉" | jej WhatsApp správu (lopta u nej) | 🔥 cenová námietka rozpracovaná |
| [[gudslip]] | email 20.7. + telefón (WhatsApp draft) | jeho odpoveď | 🔥 jediný ICP v2 s priamym kontaktom |
| [[wiki/projects/orox-leather-co|orox-leather-co]] | fáza 2 odoslaná 3.8. (priznanie + ponuka na rodinný príbeh) | jeho odpoveď | vysoká — neobranná reakcia |
| [[wiki/projects/gems-of-california|gems-of-california]] | fáza 2 odoslaná 3.8. (otázka na fragmentáciu web+eBay+Etsy) | jeho odpoveď | vysoká |
| [[wiki/projects/biorythme|biorythme]] | fáza 2 odoslaná 3.8. (priznanie naviazané na jej „hacking") | jej odpoveď | vysoká — CEO reagovala sama |
| [[nick-anger-knives]] | reframe 24.7. (supply-constraint → waitlist, nie viac dopytu) | jeho odpoveď | vysoká — ⚠️nože (HIGH-RISK platby) |
| [[ember-coffee]] | priznanie + reframe 24.7. (subscription) | jeho odpoveď | stredná — ⚠️redesign 2025 |
| [[iron-grove-tool-co]] | ⏸️ draft odpovede pripravený, NEODOSLANÝ (čaká schválenie) | Markovo rozhodnutie | nízka — web má funkčný, ⚠️nože |
| [[the-local-branch]] | „Why don't you use it that much?" 22.7. | ⏸️ Seen, nepingovať | nízka — slabý fit (retail-first) |
| [[gollik-knives]] | otázka na platby 20.7. | jeho odpoveď | stredná — CZ maker |
| [[wiki/projects/sweet-nothings-studios|sweet-nothings-studios]] | mäkký CTA 20.7. | jej odpoveď | stredná |
| [[workaday-handmade]] | diagnostická otázka 20.7. | jej odpoveď | stredná |
| [[ban-tang-knives]] | overovacia otázka 20.7. | jeho odpoveď | stredná |
| [[wiki/projects/drop-dead-candles|drop-dead-candles]] | push follow-up 20.7. (pitch odmietla) | jej odpoveď | nízka |
| [[jason-fry]] | vyjasnené „si bot?" 20.7. | jeho odpoveď | referral node (Guild president) |
| [[wiki/projects/saint-jewellry|saint-jewellry]] | fáza 2 odoslaná 15.7., seen | jej odpoveď | doznieva |
| [[wiki/projects/sperky-richterova|sperky-richterova]] | priznanie 16.7. | jej odpoveď | doznieva |
| [[disciple-designed]] | follow-up 15.7. | jeho odpoveď | doznieva |
| [[wiki/projects/rebecca-d-enamel|rebecca-d-enamel]] | 20.7. len lajk | ⏸️ nepingovať (manžel stavia web) | pauza |
| [[fitnessmenu]] | — | Borisov návrat z dovolenky | mimo outreachu |

**Presunuté zo živých vlákien:** [[lobo-gun-leathers]] definitívne odmietol („No we are good", ~28.7.) →
`status: done`. [[wiki/projects/pekne|Pekne]] odmietol mailom 20.7. → `status: done`.

**⚠️ Otvorený akčný bod:** [[sacha-carlos-raps]] si vypýtala komunikáciu mailom — **mail na
hello@sacharaps.com stále nie je odoslaný**, na IG bol len prisľúbený (visí od 20.7.).

## 6. Posledné odpovede (verbatim)

| Dátum | Lead | Čo napísal/a | Čo to znamená |
|---|---|---|---|
| 27.7. | [[wiki/projects/gems-of-california\|gems-of-california]] | „I don't do pop ups anymore... I focus on mining and custom orders! ...let me know I can work with you on prices" | web opravený (starý hook mŕtvy), predaj fragmentovaný na web+eBay+Etsy, ceny cez DM |
| ~28.7. | [[lobo-gun-leathers]] | „No we are good" (na priamu otázku „Do you need an eshop?") | definitívne odmietol → `done` |
| 25.7. | [[wiki/projects/orox-leather-co\|orox-leather-co]] | „We are a small team... thank you we should integrate it more to each page specially the front" | potvrdil pain point bez obrany, malý tím |
| 25.7. | [[wiki/projects/biorythme\|biorythme]] | „web se snažíme pořád vylepšovat, jede bohužel na krabici... každá změna je tak trochu hacking" | CEO sama potvrdila zastaranú/ťažko upravovateľnú platformu |
| 20.7. | [[wiki/projects/pekne\|Pekne]] | „Ďakujeme za ponuku, zatiaľ ju nebudeme potrebovať" (mail, objavené 3.8.) | odmietol rýchlo, priateľsky, bez priestoru na ďalší kontakt |
| 20.7. | [[chuck-richards-knives]] | „Thanks! 🙏" (email, po reframe) | vlákno uzavreté v teplom bode, CTA nikdy nezopakovaný |
| 24.7. | [[nick-anger-knives]] | „I can only make so many" | supply-constrained maker. Marko 24.7. reframe: store = manažment dopytu (waitlist), nie viac dopytu |
| 22.7. | [[ember-coffee]] | „They are roasted fresh by our roastery team and shipped out the same week 😊☕️" | odpovedal ako predajca (pattern #2). Marko 24.7. reframe na subscription |
| 22.7. | [[lobo-gun-leathers]] | „Phone works very well... first time people... their style of carry and body type" | vecná námietka (telefón = hodnota). Marko 24.7. reframe: form = pred-filter |
| 22.7. | [[the-local-branch]] | „mostly an in person business, online side is a fraction. Hope you can visit!" | slabý fit (retail-first). Naša otázka ostala na Seen |
| 21.7. | [[nick-anger-knives]] | „I have a few pieces with Eatingtools... Was there something you were interested in?" | odpovedal ako predajca (pattern #2). Marko 24.7. priznanie + hook |
| 21.7. | [[lois-gore-hampton-gem]] | „I will keep you in mind if I want to build a store. I like when someone searches and finds me." | **informované nie** (preferuje discovery model). Marko 24.7. slušný close |
| 21.7. | [[colin-shannon-shannon-steel-labs]] | „👍 Thanks man i appreciate it!" | priateľské uzavretie, výroba pozastavená. Nurture |
| 21.7. | [[wiki/projects/by-alisha\|by-alisha]] | „Napíšem 😉" | prijala Markovo číslo, presun na WhatsApp. Lopta u nej |
| 21.7. | [[iron-grove-tool-co]] | „you can find our work... irongrovetoolcompany.com. Links in bio change based on collections/events." | hook mimo (funguje iná doména). Draft odpovede neodoslaný |
| 20.7. | [[chuck-richards-knives]] | „Not one single person says to me they think they're out of stock. Ok. Email to me. Link in bio" | **qualified** — námietka + explicitná žiadosť o email |
| 20.7. | [[chuck-richards-knives]] | „The FreeBird is on sale now and available in all options" | odpovedal ako predajca zákazníkovi (pattern, pozn. #2) |
| 20.7. | [[nino-rostomashvili]] | „Many Thanks. Will think about this." | 2× soft-close → nurture, re-touch ~09/2026 |
| 20.7. | [[wiki/projects/drop-dead-candles|drop-dead-candles]] | „I'm ok, thanks though" | pitch odmietnutý, push follow-up poslaný |
| 20.7. | [[wolf-ceramics]] | „not looking for help at this time" | uzavreté |
| 20.7. | [[gollik-knives]] | custom cez FB; na .cz plánuje galériu + dostupné kusy + katalógové modely | vecná odpoveď, konverzácia beží |
| 20.7. | [[wiki/projects/rebecca-d-enamel|rebecca-d-enamel]] | (len lajk, žiadny text) | vlákno na pauze |

Kompletný archív odpovedaných konverzácií: [[wiki/outreach/fixtures/index|conversations/index]].

## 7. Čo dashboard zatiaľ nevie

Poctivé medzery, nie vynechané čísla:

1. **[[outreach-batch-5]] (21 otváračov) nemá záznam o odoslaní.** V logu je len založenie dávky
   (16.7.) s poznámkou „nič nebolo odoslané". Napriek tomu 8 leadov z tejto dávky odpovedalo
   (Gollik, Nino, Jason Fry, Lobo, Lois Gore, Don Hanson, Colin Shannon, Ban Tang) — dávka teda
   evidentne odišla okolo 16.–17.7., ale **počet ani presný dátum nie sú overené**. Preto sú v
   tabuľke dve response rate čísla. → Marko vie potvrdiť, koľko z 21 reálne poslal.
2. **Disciple Designed sa počíta dvakrát.** [[outreach-batch-2]] ho vedie medzi svojimi 12 správami,
   ale [[cold-outreach-pipeline]] datuje jeho oslovenie na **18.6.** — mesiac pred vlnou. Denný
   prehľad [[outreach-day-2026-07-15]] preto hlási „17 EN odoslaných 15.7.", čo ho zrejme ráta znova.
   Tu je vedený ako pred-vlnový kontakt a 18. EN správou z 15.7. je Drop Dead Candles — takto to
   sedí s vlastným číslom pipeline „EN 5/18".
3. **Čas do odpovede sa nemeria.** Vieme dátumy, nie hodiny — „same-day reply" u Chucka je jediný
   presný údaj. Metrika z plánu zberu dát zatiaľ nezbieraná.
4. **Nevieme, koľko z odpovedí je reálna príležitosť.** 22 odpovedí, ale 0 podpísaných dealov;
   viacero odpovedí sú zdvorilé odmietnutia alebo nekvalifikovaní (Hazel, Wolf, darcekove_kytice).
5. **Kanál „Email" v §1 tabuľke „Podľa kanála" je podhodnotený.** Gmail (3.8.) ukázal desiatky
   odoslaných mailov, ktoré v tejto stránke neboli počítané: celé Chuck Richards vlákno malo správne
   len 1 z 2 odoslaných mailov zaznamenaných (poradie navyše obrátené), batch 10 (3 maily) bol vedený
   ako neodoslaný, pekne.eu malo email popri IG DM bez záznamu. Pravdepodobne existujú ďalšie
   nezapísané emaily zo 16.7. dávky (napr. duálny kanál email+IG pre Jason Fry, Lobo, Don Hanson —
   tieto tri majú email potvrdený v Gmaile, ale stránky ich nespomínajú). **Presné číslo vyžaduje
   samostatný lint pass cez celú Gmail schránku, nie je súčasťou tohto ingestu.**
6. **[[outreach-batch-10]] odišiel napriek explicitnej výhrade na vlastnej stránke** („v tomto znení
   ani neposielať" — variant B, akútnosť pain pointu 0). Nie je jasné, či to bolo vedomé rozhodnutie
   Marka poslať aj tak, alebo omyl (napr. poslané predtým, než bola výhrada napísaná — časovo sa to
   prekrýva: mail 20.7. 14:20, výhrada pravdepodobne pridaná neskôr v ten istý deň). Stojí za to sa
   Marka spýtať, aby sa vedelo, či sa má rovnaký vzorec (odoslať aj cez výhradu) opakovať alebo nie.

## Zdroje

- [[cold-outreach-pipeline]] — riadková tabuľka všetkých prospektov, poznatky #1–#11
- [[outreach-batch-1]] … [[outreach-batch-10]] — plné znenia odoslaných správ
- `wiki/projects/*` — `## Komunikácia` sekcie (verbatim prepisy odpovedí)
- [[wiki/outreach/fixtures/index|conversations/index]] — archív 9 odpovedaných konverzácií
- [[outreach-day-2026-07-15]] — denný prehľad prvého veľkého dňa
- [[cold-outreach-manual]] — variant A, Origami benchmark
