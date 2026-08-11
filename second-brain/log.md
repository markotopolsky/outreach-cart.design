
## [2026-07-20] ingest | Chuck Richards — email fáza 3 odoslaný (reframed)
Marko odoslal reframed email na sales@chuckrichardsknives.com (predmet „The FreeBird — from Instagram").
Verzia 1 (draft): argue with his premise. Verzia 2 (sent): počúvať — zdvojenie jeho vety „Not one single
person says to me..." a otázka „Which is it?" — nechá Chucka vysvetliť, ako jeho operácia funguje, bez
tlaku. Bez CTA, bez argumentu; len príslub. Aktualizovaná [[chuck-richards-knives]] (Email section,
Ďalší krok: čaká sa na odpoveď).

Append-only journal. Formát: `## [YYYY-MM-DD] akcia | názov` — `grep "^## \[" log.md | tail -5` pre posledné záznamy.

## [2026-07-13] bootstrap | Inštanciácia wiki systému

Vytvorená schéma (CLAUDE.md), index.md, log.md a prvotný ingest všetkých existujúcich raw zdrojov. Nové stránky: [[fitnessmenu]], [[pevne-zuby]], [[boris]], [[katarina-silna]], [[otec]], [[konkurencia-fitnessmenu]]. Raw súbory nezmenené. Nálezy pre budúci lint: 3 prázdne placeholder súbory vo Fitnessmenu raw; rozpor v návratnosti klientov DH (80 % vs 30 %); visual brief prázdny.

## [2026-07-15] lint | Presun raw zdrojov pod `raw/`

Marko presunul `cart.design/`, `merge.build/`, `other/` do `raw/`. Aktualizovaná CLAUDE.md (layout, hard rules), index.md (nadpisy sekcií) a stránky [[fitnessmenu]], [[otec]] (cesty k raw súborom). Ostatné wiki odkazy (`pevne-zuby.md`, `katarina-silna.md`) už používali `raw/...` prefix — bez zmeny.

## [2026-07-15] ingest | Cold outreach systém (raw/cart.design/cold-outreach)

Zanalyzované 3 raw súbory (Outreach_System, Prospect_Template, prompt-ai — posledný je EN duplicita). Nová stránka [[cold-outreach-manual]] (type: answer) — kombinovaný manuál: workflow, checklist pred odoslaním, follow-up, kam ukladať prospect poznámky. index.md doplnený o raw sekciu cold-outreach.

## [2026-07-15] setup | Dropdown polia + auto-dátum pre cold outreach

Nainštalované 2 community pluginy: **Metadata Menu** (dropdown pre `pozicia`, `kanal`, `jazyk`, `ton`, `typ_klienta`, `status`, scoped na `raw/cart.design/cold-outreach/prospects/`) a **Templater** (nový súbor v priečinku `prospects/` automaticky dostane šablónu + dnešný dátum do `datum_oslovenia`). Nová pracovná šablóna `raw/cart.design/cold-outreach/templates/Prospect_Template_Templater.md` (pôvodná `Prospect_Template.md` nedotknutá). [[cold-outreach-manual]] a index.md aktualizované o nový postup a nastavenie.

## [2026-07-15] update | Dvojfázový outreach (otvárač → pitch)

Marko preorganizoval `cold-outreach/` (prompty do `system/`, šablóna do `templates/`, Templater verziu zrušil — plugin sa nepodarilo rozbehnúť, Templater vypnutý). Nový prístup podľa Markovej skúsenosti: prvá správa len otvára konverzáciu pain pointom, pitch až po reakcii. Šablóna doplnená o návod v sekcii „Ako začať konverzáciu", [[cold-outreach-manual]] prepísaný na 2 fázy + nový opener prompt. Prvý prospect: `biorythme.cz.md`. index.md zosúladený s novými cestami.

## [2026-07-15] ingest | Biorythme.cz — fáza 1 (otvárač)

Marko presunul cold outreach do `raw/cart.design/cold-outreach-system/` (prompty, šablóna) a `raw/cart.design/cold-outreach-clients/` (klientske poznámky). Spracovaná research poznámka `biorythme.cz-raw.md` (zastaraný eshop, silný produkt čo sa šíri samo, ťažké objednávanie, konkurencia ben-anna.de). Nová stránka [[biorythme]] (type: project, active) so syntézou situácie a 2 návrhmi otváracej správy (fáza 1 — bez predaja, cieľ vyvolať reakciu). Návrhy sú vo wiki, nie v raw `-sprava.md` súbore (ten zostáva prázdny/pre Markove vlastné poznámky). index.md aktualizovaný.

## [2026-07-15] setup | Cold outreach pipeline

Nová stránka [[cold-outreach-pipeline]] (type: project) — centrálna tabuľka všetkých prospektov (stav, kanál, hook, dátumy), workflow Marko↔Claude (kto čo robí v každom kroku) a plán zberu dát po 1. vlne ~20 mailov (response rate podľa hooku/kanála/typu klienta). Biorythme zapísané ako prvý riadok. Subject pre biorythme finalizovaný Markom: „Výborný produkt a postreh k vášmu eshopu". index.md aktualizovaný.

## [2026-07-15] ingest | Origami cold email playbook

`document-origami.md` presunutý z rootu do `raw/cart.design/cold-outreach-system/`. Kľúčové princípy zapracované do [[cold-outreach-manual]] (nová sekcia: 5–8 viet, mobile-first, pain point nie features, priamosť, ~5 % response rate, ICP > text správy, call = 90 % discovery) a do [[cold-outreach-pipeline]] (kalibrácia očakávaní: 20 mailov ≈ 1 odpoveď; TODO definovať ICP). Manuál zároveň očistený od zastaraných ciest (prospects/, Templater). index.md aktualizovaný.

## [2026-07-15] ingest | Cart Leads databáza (38 leadov)

`Cart Leads - Sheet1.csv` (US/EN handmade makers, research k 2026-06-15) triážovaná do [[cold-outreach-pipeline]]: Tier 1 (12 leadov — veľké publikum + rozbitý predaj), Tier 2 (stredné/redesign), Tier 3 (nože, HIGH-RISK platby). Flagnuté časovo kritické: Shannon Steel Labs (doména expiruje 20.7.), Gollik (2.8.). ICP hypotéza potvrdená databázou. Otvorené: rozdelenie owner Marek/Adam, EN jazyk správ. index.md aktualizovaný (aj nové cesty po Markovom presune do `cold-outreach/`).

## [2026-07-15] query | Batch 1 — prvých 5 otváračov

Marko posiela všetko sám (aj Adamove leady). Nová stránka [[outreach-batch-1]] — 5 EN otváračov fázy 1: Drop Dead Candles, LadyBuQ Art, Optimistic Soap, Kamari Candle (IG DM) + Jenny Topolski (email so subjectom). Všetky bez pitchu, hook = overiteľný technický problém ich webu. Pipeline tabuľka doplnená o 5 riadkov (stav: správa pripravená). index.md aktualizovaný.

## [2026-07-15] lint | Verifikácia hookov batch 1 (curl)

Markova otázka „čo ak sú fakty zlé?" → overené všetky weby z batch 1. Výsledok: 3 z 5 hookov STALE (Drop Dead — nový Shopify beží; Optimistic Soap — Wix store pridaný; Kamari — /shop existuje). Batch 1 prepísaný na overenú päťku: LadyBuQ, Topolski, iamrachel, Creations That Rock (web zomrel po 15.6. — najčerstvejší hook), Pierre Laborde (demand leak uhol). Hazel vyradená (hook neistý). Nové pravidlo v [[outreach-batch-1]] aj manuáli: hook sa overuje v deň odoslania („over batch"). Pipeline aktualizovaná.

## [2026-07-15] update | ICP v1 definované

Podľa Origami step 1 („figure out who you're selling to first") sformalizované ICP do [[cold-outreach-pipeline]]: handmade maker s preukázaným dopytom (10K+ followers / 1K+ Etsy sales / sellouts) a rozbitým predajným kanálom (mŕtvy web / bez košíka / Etsy-dependent / DM-only); persóna = majiteľ-remeselník topiaci sa v operatíve. Z ICP odvodená logika správy: uznanie dopytu → postreh o kanáli → otázka. Iterácia ICP po 1. vlne podľa toho, kto odpovedal. Otvorený experiment: brand-first vs. tech-first hook mix.

## [2026-07-15] query | Batch 2 — 12 správ + tech/brand-first experiment

Marko poslal Drop Dead Candles priamo (vlastná verzia) — pipeline updatnutá na „oslovený". Nová stránka [[outreach-batch-2]] — 12 EN IG DM otváračov, fakty overené 15.7. (curl): The Low Key Co (doména teraz parkovaná), Sweet Nothings (web timeout), Forest Nine (password-locked), Miners Ink (mŕtva DNS), Kamari a Macrame (pôvodné hooky z CSV boli stale — prerobené na aktuálny stav). Zvyšných 6 je zámerne brand-first (Disciple Designed, Rebecca D Enamel, Hazel Hand Engraving, Jake Newell, DoubleK, Optimistic Soap) — spúšťa Markov navrhnutý experiment tech-first vs. brand-first, vyhodnotenie v [[cold-outreach-pipeline]] po 1. vlne. Pipeline a index.md aktualizované.

## [2026-07-15] query | Tabuľka odkazov pre Claude in Chrome

Žiadny browser-automation MCP nie je v tejto (CLI) session pripojený — Claude in Chrome je samostatný nástroj mimo tohto prostredia. Namiesto toho nová stránka [[outreach-links]] — IG + web link pre všetkých 38 leadov z CSV, na manuálne použitie s Claude in Chrome (kontrola + odoslanie). index.md aktualizovaný.

## [2026-07-15] ingest | Disciple Designed — IG DM konverzácia (18.-19.6.) + follow-up
Marko vložil výmenu s Jacobom (otvárač 18.6., odpoveď 19.6. — prvý respondent v pipeline). Vytvorená [[disciple-designed]] s prepisom, analýzou odpovede a pripraveným follow-upom. Pipeline riadok → "reagoval", index doplnený.

## [2026-07-15] ingest | Potenciálni klienti SK — e-shopy + IG leads
Marko poslal tabuľku 29 SK e-shopov (handmade, remeslo, kreatívne potreby, šperky, keramika, drevené výrobky; stav verifikovaný) a 3 IG leads bez webu (badynco, darcekove_kytice, mc_remeselnik). Uložené do `raw/cart.design/cold-outreach/potentional-clients/eshops-and-ig-leads.md`. Primárny database pre SK outreach fázu 1 — ďalší krok: research hookov a kategorizácia podľa rozbitého predaja.

## [2026-07-15] ingest | SK Instagram leady — Firecrawl + Kimi WebBridge hybrid
Nová metóda: Firecrawl `site:instagram.com` search (rýchlejšie objavovanie kandidátov ako hashtag crawling) → Kimi WebBridge overil bio/link-in-bio. Pridané 4 nové kvalifikované leady bez e-shopu k pôvodným 3 (badynco, darcekove_kytice, mc_remeselnik): by_alisha.sk (25.3K, najsilnejší lead), saint.jewellry (1,4K, predáva cez sashe.sk marketplace), sperkyrichterovahandmade (439, len fyzická adresa), handmadebyluvela (47, len Threads link). Zistenie: čistý Firecrawl web search bez `site:instagram.com` väčšinou nájde firmy s existujúcim e-shopom (Google ich indexuje) — sociálni-only predajcovia sú tak neviditeľní. Uložené do `raw/cart.design/cold-outreach/ig-sk-leads-2026-07-15.md`, zosumarizované v [[cold-outreach-pipeline]]. index.md aktualizovaný.

## [2026-07-15] query | Batch 3 — 6 SK otváračov z hĺbkového IG researchu
Kimi WebBridge prečítal posledné posty + komentáre všetkých 7 SK leadov. Kľúčové nálezy: by_alisha.sk má 8+ nezodpovedaných "cena prosím?" komentárov pod 5-dňovým postom (najsilnejší hook — demand leak); darcekove_kytice robí urgency marketing bez okamžitého nákupu; saint.jewellry spí 43 týždňov (vysoké riziko); mc_remeselnik vyradený (služby → merge.build ICP). Nová stránka [[outreach-batch-3]] — 6 personalizovaných SK otváračov podľa pravidiel z [[cold-outreach-manual]] (postreh/otázka, bez pitchu, 20-40 slov), zoradené podľa sily hooku. Pipeline + index aktualizované.

## [2026-07-15] ingest | saint.jewellry REAGOVALA + by_alisha nedostupná
saint.jewellry (batch 3, tier C "možno mŕtvy účet") odpovedala na otvárač: "Ahoj, vieš mi poslať konkrétny šperk, prosím?" — druhý respondent v pipeline. Firecrawl scrape jej sashe obchodu: 0 vecí v ponuke / 81 predaných — vypredaná, nedoplnená ponuka. Pripravená odpoveď (náhrdelník z posledného reelu + postreh 0/81, stále bez pitchu). by_alisha.sk (tier A) sa nedá osloviť — DM nedostupné. [[outreach-batch-3]] aktualizovaný.

## [2026-07-15] ingest | darcekove_kytice REAGOVALA — tretí respondent
Odpovedala na otvárač: "Keď je viacej záujemcov spravím ešte take iste kytice. Máte záujem o kyticu?" Potvrdila pain point (ručné spracovanie každého záujemcu cez DM) a považuje Marka za zákazníka. Fáza 2 pripravená v 2 variantoch (vykanie, bez pomlčiek), odporúčaný B s mäkkým CTA. Batch 3 má zatiaľ 2 reakcie z 2 odoslaných SK správ v prvý deň. [[outreach-batch-3]] aktualizovaný.

## [2026-07-15] update | darcekove_kytice — fáza 2 odmietnutá
Na pitch (variant B, mäkký CTA) odpovedala "Ďakujem za ponuku, nie nepotrebujem." Uzavreté slušnou bodkou bez follow-upu podľa manuálu. Dáta pre iteráciu: otvárač zafungoval (reakcia < 1 deň), pitch neprešiel — možný dôvod: malá značka (2.1K), DM proces jej zatiaľ stačí, pain point nebol dosť akútny. saint.jewellry konverzácia beží ďalej (poslaný screen + priznanie + 0/81 postreh). [[outreach-batch-3]] aktualizovaný.

## [2026-07-15] update | Prvé dáta z SK batch 3 zapísané do pipeline
Tri poznatky do sekcie Zber dát v [[cold-outreach-pipeline]]: (1) akútnosť pain pointu rastie s objemom dopytu — malé účty s fungujúcim DM procesom pitch odmietnu aj po reakcii na otvárač; ICP posun k leadom s viditeľným dôkazom nestíhania; (2) otvárač znejúci ako zákaznícky záujem núti prospekta odpovedať predajným módom a fáza 2 potom pôsobí ako bait-and-switch; (3) ručné úpravy faktov v správach treba overovať proti zdroju (manuál §3c). SK response rate 2/3 v prvý deň vs. Origami benchmark ~5 %.

## [2026-07-15] query | Batch 4 — 2 SK e-mail otvárače z e-shop listu
Hĺbkový research 6 kandidátov z e-shop listu (Firecrawl: kontaktné stránky, sashe štatistiky, produktové stránky). Kvalifikované 2: AC keramika / Anna Čičková (sashe 8 v ponuke / 68 predaných / 38 hodnotení — dopyt > ponuka; priamy e-mail) a Umelecká keramika (svojpomocný web so šablónovými URL, aktívny blog). Vyradené 4: Ladybead (funkčný Shopify), Mliečne remeslo (družstvo — iný ICP), Dekupáž + Biela Duha (zásobovacie obchody). Nová stránka [[outreach-batch-4]] — prvý e-mail test na SK trhu. Index aktualizovaný.

## [2026-07-15] update | Prvý veľký deň odosielania — 24 správ, denný prehľad
Marko potvrdil odoslanie: batch 1 (5 EN) + batch 2 (12 EN) + batch 3 (5 SK IG: saint, darcekove, luvela, badynco, richterova) + batch 4 (2 SK email cez Gmail drafty: AC keramika, Umelecká keramika). Nová stránka [[outreach-day-2026-07-15]] — kompletný denný prehľad s obsahom všetkých správ a číslami (24 odoslaných, 2 SK reakcie deň 1, SK response rate 29 % vs. EN zatiaľ 0 — US pásmo). Pipeline tabuľka: všetkých 24 → "oslovený" s dátumom. Follow-up okno: 18.–20.7. Index aktualizovaný.

## [2026-07-15] ingest | Reakcia: Optimistic Soap (Molly Lee)
Prvá EN reakcia (batch 2, brand-first). Molly: rok stuck v migrácii na Shopify, double hosting, Wix billing-name bug; spomenula lead Clover Soapworks (Nathan). Fáza 2 navrhnutá (2 varianty, mäkké CTA). Aktualizované: outreach-batch-2, cold-outreach-pipeline, index.

## [2026-07-15] ingest | Fáza 2 poslaná: Optimistic Soap (Molly Lee)
Finálny pitch odoslaný (custom code framing, mäkké CTA, Nathan P.S.). Text zapísaný v outreach-batch-2; pipeline stav → fáza 2 poslaná. Poučenie: cart.design = custom code, nie Shopify.

## [2026-07-15] refactor | merge.build (DH / Pevné zuby) vyňaté z wiki
DH presunuté von z LLM wiki: `raw/merge.build/dh/` → `/second-brain/dh/` (mimo raw aj wiki). Zmazané wiki stránky [[pevne-zuby]] a [[katarina-silna]]. Aktualizované: index.md (odstránený projekt, osoba, raw sekcia), CLAUDE.md (raw layout bez merge.build, poznámka o `dh/` mimo wiki, príklad odkazu). Wiki je odteraz čistý cart.design. Kontextové zmienky o „merge.build ICP" v outreach stránkach ponechané (triáž leadov, nie odkazy na DH).

## [2026-07-15] lint | oprava zaradenia stránok podľa schémy
`outreach-day-2026-07-15.md` mal `type: topic`, ale ležal v `wiki/projects/` → presunutý do `wiki/topics/`. Index aktualizovaný (presunutý z Projekty do Témy). Ostatné outreach stránky (batch-1..4, pipeline) ponechané — držia reálny per-lead research, nie sú duplicitné.

## [2026-07-15] refactor | wiki reorganizovaná do funkčných foldrov
Pridané foldre `wiki/outreach/` (pipeline + batch-1..4 + links + prospekti biorythme, disciple-designed) a `wiki/feedback/` (outreach-day). `projects/` teraz len reálne pokročilé deals (fitnessmenu). Wikilinky nedotknuté (Obsidian ich rieši podľa mena súboru). Index sekcie a CLAUDE.md layout/workflow aktualizované; nové pravidlo: prospekt žije v outreach/, do projects/ „povýši" keď je reálny deal.

## [2026-07-15] refactor | teplé leady povýšené do projects/
Do `wiki/projects/` pridaní všetci, čo odpísali a majú s nami komunikáciu: [[disciple-designed]] (presunutý z outreach/), nové entity stránky [[optimistic-soap]] (Molly, fáza 2 odoslaná), [[saint-jewellry]] (reagovala, odpoveď pripravená), [[darcekove-kytice]] (reagovala, odmietla → done/mŕtve). Batch-2/#12 a batch-3/#2,#5 dostali odkaz na svoje lead stránky (jeden zdroj, prepojené). Index sekcia Projekty rozšírená (deals + teplé leady), disciple-designed odobraný z outreach sekcie. Pravidlo: prospekt povýši z outreach/ do projects/ keď reálne odpovie.

## [2026-07-15] ingest | Optimistic Soap: pitch odmietnutý, push follow-up poslaný
Molly pitch zdvorilo odmietla („too many choices"). Marko poslal push follow-up: prerámovanie + nula práce + lacnejšie + 20-min call CTA. Ak nič → žiadny ďalší push, dlhodobý touch ~10/2026. Aktualizované: optimistic-soap, cold-outreach-pipeline, index. (Pozn.: prispôsobené novej folder štruktúre wiki/outreach + wiki/projects per-prospekt.)

## [2026-07-15] ingest | IG DM prepisy leadov (Kimi WebBridge)
Stiahnuté 4 vlákna z Instagramu (markotopolsky): optimistic-soap, saint.jewellry, darcekove_kytice, disciple-designed. Do každej lead stránky pridaná sekcia „Komunikácia" s plným prepisom. Nové fakty: Molly definitívne odmietla (status done), saint.jewellry fáza 2 odoslaná + seen, Jacobovi follow-up odoslaný 15.7. Aktualizované: 4 projekty, index.md, CLAUDE.md (konvencia Komunikácia).

## [2026-07-16] ingest | IG inbox prepis ig-status167 — 6 nových reakcií
5 nových reakcií z 15.-16.7. (Rebecca „renovujem web", Hazel nekvalifikovaná, Richterová ako zákazníkovi, Drop Dead + Sweet Nothings „works for me") + korekcia by_alisha (oslovená bola, pýta sa „ako riešiť?"). 6 nových project stránok, update [[outreach-batch-2]], [[outreach-batch-3]], [[cold-outreach-pipeline]] (skóre EN 5/18, SK IG 4/6; poznatok #4 o site-down hookoch; Sweet Nothings apex-SSL diagnóza overená curl/openssl 16.7.).

## [2026-07-16] update | Odpovede pre 6 respondentov odoslané

Marko odoslal fázu 2 / follow-up všetkým 6 respondentom z ig-status167 (konverzácie otvorené v Kimi WebBridge, texty podľa návrhu): [[by-alisha]] (priznanie + riešenie na mieru — HOT), [[sperky-richterova]] (priznanie pred pondelkovými fotkami), [[rebecca-d-enamel]] (zvedavá otázka na renováciu), [[sweet-nothings-studios]] (SSL diagnóza), [[drop-dead-candles]] (čestná záchrana + Etsy pivot), [[hazel-hand-engraving]] (slušné uzavretie, status → done — nekvalifikovaná). Všetky prepisy doplnené v projektových stránkach, index.md aktualizovaný.

## [2026-07-16] ingest | by_alisha — cenová námietka na fázu 2

Alisha odpísala na fázu 2: funguje takto 11 rokov, e-shop mala, 3–4 tis. € doň znova nedá. Marko odpísal prijatím námietky (znenie približné). Aktualizované: [[by-alisha]] (profil, stav, prepis, ďalší krok = reframe dopytový flow ≠ starý e-shop), [[cold-outreach-pipeline]] tabuľka, index.md.

## [2026-07-16] query | Aká je úspešnosť (response rate) outreachu?
Odpoveď z [[cold-outreach-pipeline]] (dáta k 16.7. ráno): EN 5/18 (28 %), SK IG 4/6 (67 %), SK email 0/2, spolu ~35 %; brand-first 3/6 vs. tech-first 1/6. Bez zápisu do wiki (živá metrika, nie durable answer).

## [2026-07-16] query | Batch 5 — 21 otváračov pre zvyšok Cart Leads CSV
Marko chcel pôvodne poslať správy „všetkým" 39 leadom z CSV naraz, automaticky cez Kimi WebBridge. Kontrola pipeline tabuľky odhalila, že **18/39 už bolo oslovených** (batch 1+2, niektorí reagovali) — automatický blast by ich zdvojil. Namiesto toho: nová stránka [[outreach-batch-5]] — 21 otváračov (fáza 1, bez pitchu) pre nekontaktovaných leadov: 6 non-knife (Jamie Noelle, Sharp & Fiery, Pam Farren, Lois/Hampton Gem, Lobo Gun Leather, Nino Rostomashvili) + 15 knife makerov. Knife sekcia označená ⚠️ HIGH-RISK — platobný procesor treba overiť pred odoslaním čohokoľvek. Owner (Adam/Marek) uvedený pri každom leade. Nič nebolo odoslané — čaká na Markovu kontrolu a manuálne odoslanie. Aktualizované: cold-outreach-pipeline, index.md. Odložené: research 35 nových US leadov cez Firecrawl+Kimi (samostatná úloha, na povel).

## [2026-07-16] setup | wiki/conversations/ — archív odpovedaných konverzácií
Nový priečinok `wiki/conversations/` s 9 kurátorskými kópiami IG DM konverzácií, kde prospect skutočne odpovedal (saint-jewellry, rebecca-d-enamel, darcekove-kytice, hazel-hand-engraving, by-alisha, sperky-richterova, drop-dead-candles, optimistic-soap, sweet-nothings-studios) + `index.md` s prehľadovou tabuľkou. Zdrojom pravdy zostávajú `## Komunikácia` sekcie na project stránkach — tieto sú len kópia/link naspäť. Otvorená otázka od Marka: prístup pre kolegov (Obsidian Publish / shared repo) — **zatiaľ nenastavené**, obsah je citlivý a podľa hard rule v CLAUDE.md nemá opustiť vault bez explicitného pokynu na mechanizmus. Aktualizované: index.md.

## [2026-07-16] ingest | Batch 6 — 15 nových US leadov (discovery + verifikácia)
Discovery cez WebSearch/Google (Firecrawl mal invalid token — treba `firecrawl login`), verifikácia curl 2× + Kimi WebBridge IG. 17 overených, top 15 vybraných (10 brand-first / 5 tech-first). Nové: `raw/.../us-leads-batch6-2026-07-16.md`, [[outreach-batch-6]]; pipeline +15 riadkov, index updatnutý. Lint nález: `ig-sk-leads-2026-07-15.md` referencovaný v indexe už v raw neexistuje.

## [2026-07-16] ingest | Rebecca D Enamel — 2. odpoveď (manžel-inžinier renovuje web)
Rebecca odpísala: web jej vyhovoval, renováciu inicioval a robí jej manžel (computer engineer). Nie odmietnutie, ale in-house DIY — pitch proti manželovi by bol kontraproduktívny; zvolený resource angle (opýtať sa na stack, ponúknuť referenčné príklady). Aktualizované: projects/rebecca-d-enamel, conversations/rebecca-d-enamel, index.md. Návrh follow-upu odovzdaný Markovi v sedení.

## [2026-07-16] update | Batch 6 — všetkých 15 správ odoslaných
IG DM cez Kimi WebBridge (Markov účet), každá overená vo vlákne po odoslaní. 10 brand-first / 5 tech-first. Pipeline: 15 riadkov na `oslovený 2026-07-16`; [[outreach-batch-6]] + index updatnuté. Poznámka k metóde: automat s @e refmi zlyhal na 2/9 profiloch (tlačidlo Message sa nenašlo v snapshote) — spoľahlivejšie je otvoriť taby a doposlať cez find_tab.

## [2026-07-16] ingest | Gollik Knives — reakcia (Jakub Golla, CZ)
Prvá reakcia z knife Tier 3: .com už kúpil niekto iný (CSV odhad expirácie 2.8. bol stale — poznamenané v pipeline), kúpil .cz ktorá nefunguje, robí custom orders, predaj cez FB/BladeForums. Nová stránka [[gollik-knives]] s prepisom; batch-5 #21 a pipeline aktualizované. Ďalší krok: fáza 2, prechod do SK/CZ.

## [2026-07-16] ingest | Nino Rostomashvili — reakcia + follow-up odoslaný
Reakcia na batch-5 #6 otvárač: enamel-arts.com hook potvrdený (skutočne mŕtva), presunutá na Carrd (cloisonneenamel.carrd.co) + Etsy (EnamelArtsByNino). Marko odoslal follow-up sondujúci Etsy-závislosť (rovnaký pattern ako Jenny Topolski). Nová stránka [[nino-rostomashvili]] s prepisom; outreach-batch-5, cold-outreach-pipeline a index.md aktualizované.

## [2026-07-16] update | Gollik Knives — rapport správa odoslaná
Marko odoslal vlastnú EN rapport otázku na CZ/SK moment („So that must mean, that you are based in Czech Republic? (I am from Slovakia"). Prepis na [[gollik-knives]] doplnený; navrhnutý follow-up (custom-order flow + plán s .cz) uložený na stránke ako rezerva. Čaká sa na Jakubovu odpoveď.

## [2026-07-16] update | by_alisha.sk — fáza 3 (reframe cenové námietky + videohovor)
Marko adresoval cenovú námietku vecne: jej starý katalógový e-shop 3–4k € zlyhal preto, že 90 % zákaziek je na mieru — presne preto nenavrhuje klasický e-shop. Nový flow bez platobnej brány, bez vstupnej investície (mesačne bez záväzkov). Ponúka 15–20 min videohovor na diagnostiku reálneho workflow. Prepis konverzácie + stav aktualizované v [[by-alisha]], pipeline doplnený o fázu 3. Reframe držal konverzáciu otvorenú bez ústupu.

## [2026-07-20] update | IG inbox — 13 odpovedí odoslaných cez Kimi WebBridge

Prešiel sa celý IG inbox (@markotopolsky) a Marko odpovedal **všetkým 13 leadom**, ktorí odpísali od 16.7. Odoslané cez Kimi WebBridge, každá správa overená vo vlákne.

**Pokrok v konverzácii:** [[drop-dead-candles]] (sama pomenovala prichádzajúci pitch → priamy pitch na Etsy fees + ownership), [[sweet-nothings-studios]] (SSL diagnóza prijatá → mäkký CTA), [[nino-rostomashvili]] (Etsy/PayPal/Payoneer pain point → pivot na ownership platieb), [[gollik-knives]] (potvrdil Prahu → follow-up prepnutý do SK), [[rebecca-d-enamel]] (hravá odpoveď o manželovi → ponuka referencií, bez tlaku).

**Nové stránky (8):** [[lois-gore-hampton-gem]], [[lobo-gun-leathers]], [[workaday-handmade]], [[jason-fry]], [[ban-tang-knives]], [[wolf-ceramics]], [[sacha-carlos-raps]], [[colin-shannon-shannon-steel-labs]], [[don-hanson-sunfish-forge]].

**Poznatky:**
- **Poznatok #5 — geografická diskriminácia platieb je silnejší pain point než discovery.** Nino (Gruzínsko) nezaujíma, ako ju zákazníci nájdu, ale Etsy jej zablokoval PayPal a cez Payoneer dostáva ~polovicu predajnej ceny. U leadov mimo US/EU sondovať platby, nie fees všeobecne.
- **Poznatok #6 — duplicitný kanál (mail + IG) poškodzuje dôveryhodnosť.** Jason Fry (Guild president, referral node) sa priamo spýtal „Are you real person?". Jeden lead = jeden kanál, alebo priznať dvojitý kontakt hneď v druhej správe.
- **Potvrdenie poznatku #2** (otvárač ako od zákazníka): Lois Gore odpovedala dlhým predajným procesom ako zákazníkovi — priznanie bolo nevyhnutné, riziko bait-and-switch.
- **Tier 3 (nože) je z veľkej časti mŕtvy nie kvôli platbám, ale kvôli kapacite:** Don Hanson (backlog 6–8 rokov), Colin Shannon (výroba pozastavená, hľadá dielňu) — dopyt extrémny, ale nemajú čo predávať.

**Otvorený akčný bod pre Marka:** [[sacha-carlos-raps]] chce komunikovať mailom — **mail na hello@sacharaps.com ešte nebol odoslaný**, na IG bol len prisľúbený.

## [2026-07-20] ingest | Batch 7 — nová niche: drevo/nábytok (discovery)
Marko chcel otestovať novú nišu mimo doterajších cez Firecrawl + Kimi WebBridge. Firecrawl token bol znovu neplatný (401) — vyriešené `firecrawl logout` + `firecrawl login` (browser flow, Marko dokončil manuálne). Discovery: 5 `site:instagram.com` search queries (custom furniture, live edge, cutting boards/DM-to-order, wood turning waitlist, hand carved spoons) + 2 doplnkové lookupy. Z ~20 preverených kandidátov (Kimi WebBridge bio/followers + Firecrawl scrape na nav webu) kvalifikovaní len 2: Raina Nicole Woodworks (248K IG, web bez shopu) a Doucette and Wolfe/Matthew Wolfe (25.2K IG, starý statický web bez cart). TK Fareed (346K IG) vylúčená — má funkčný e-shop. Nižší strike rate než koža/šperky — poznatok: drevári skôr nemajú e-shop vôbec než majú rozbitú doménu. Nové: `raw/.../wood-furniture-leads-batch7-2026-07-20.md`, [[outreach-batch-7]]; pipeline +2 riadky, index.md aktualizovaný. Nič neodoslané — čaká na Markovu kontrolu.

## [2026-07-20] update | Batch 7 — doplnený úplný zoznam kandidátov
Marko chcel vidieť všetkých ~20 (reálne 28) kandidátov zo search výsledkov, nielen filtrovaný výber. Doplnená tabuľka do `wood-furniture-leads-batch7-2026-07-20.md`: 2 kvalifikovaní, 10 individuálne overených a vylúčených (s dôvodom), 16 zatiaľ neoverených (meno/firma zo snippetu, handle/web nekontrolovaný — treba doplniť pred kontaktom), + 2 mimo niche (šum v search výsledkoch). Index.md aktualizovaný na presný počet.

## [2026-07-20] update | Drafty na manuálne odoslanie: Sacha (mail), biorythme (fáza 1) — Jason Fry vyjasnený

Na Markovu žiadosť pripravené dva drafty, ktoré posiela manuálne sám:
- **[[sacha-carlos-raps]]** — návrh mailu na hello@sacharaps.com (nadväzuje na IG konverzáciu, pýta sa na komisný proces, mäkký CTA). Doplnené do stránky, neodoslané.
- **[[biorythme]]** — finálny návrh otvárača: zlúčenie Variantu A (silnejšia záverečná otázka) s Markovým vlastným rozpisom (osobnejší opener); vypustená veta „vyzerá pekne, bez chýb", ktorá si protirečila s pain point pitchom aj researchom. Starý neusporiadaný draft na konci stránky vyčistený.

**[[jason-fry]] vyjasnené:** Marko potvrdil, že mail aj IG správu poslal zámerne sám — nejde o chybu v procese. Označené ako vyriešené na stránke.

## [2026-07-20] ingest | Jakub Golla (Gollik Knives) reply — custom flow + .cz plan
Jakub odpovedal na Markov follow-up: custom objednávky rieši cez FB, na gollikknives.cz plánuje galériu, sekciu na aktuálne voľné/dostupné kusy a pár „štandardnejších" (katalógových) modelov. Aktualizované [[gollik-knives]] (Komunikácia + Stav konverzácie), index.md.

## [2026-07-20] outreach | Gollik Knives — odpoveď odoslaná
Marko odoslal odpoveď Jakubovi Gollovi cez Kimi WebBridge (IG DM): mirror jeho 3 bodov (galéria/dostupné kusy/štandardné modely) + otázka na platobný spôsob (karta vs. prevod) pred custom-order pitchom. Aktualizované [[gollik-knives]], index.md.

## [2026-07-20] outreach | by_alisha.sk — WhatsApp pokus
Marko sa neďaleko dostáva na IG (videohovor CTA bez odpovede od 16.7.), skúsil WhatsApp: "Úplne chápem. Kľudne som za aj ten WhatsApp. Dáte mi prosím Vaše číslo." — pokus aktivácie na iný kanál. Aktualizované [[by-alisha]] (ďalší krok), index.md.

## [2026-07-20] ingest | Batch 8 — nová niche: nože + kožené výrobky (discovery)
Marko chcel nájsť 18–20 leadov na knife makers + handmade leather goods makers (US/UK/CA). Discovery cez Google search (« best handmade knife makers instagram USA », « artisan leather goods makers instagram USA ») + Instagram hashtag #knifemaker. Zbierané: knife makers (Jordan Davis, Rob Ball, + z Reddit diskusií výskytnuté handles @allstarknives, @draugrsteel, @steelsmithnothings, @highwood.knives, @bladesmith, @primitiveknives), leather goods makers (Odin Leather Goods @codeLeather — Dallas, Lost Dutchman Leather, Somos @rosioleatherco — Portland). Metodika: podobná batch-7, Kimi WebBridge verifikácia pending (followers, bio link, web presence). Nové: `raw/.../knife-leather-leads-batch8-2026-07-20.md`, [[outreach-batch-8]]; tabuľka 22 kandidátov (5 Known z pipeline + 17 Research/TBD). Pipeline tabuľka neupdatnutá (žiada sa Markova kontrola pred odoslaním). Index.md + log.md aktualizované. Poznámka: knife makers majú vyšší median followersov než drevo (viac influencer faktor), leather goods mix solo craftspeople + malé branding teams; obe niche majú nižší e-shop adoption → hook rovnaký ako batch-7 („chýbajúci online ordering", nie „web nefunguje").

## [2026-07-20] ingest | Batch 8 — nože + koža, overený research (20 kvalifikovaných)
Marko žiadal 18–20 kvalifikovaných leadov (nože + kožené výrobky) cez Firecrawl s Kimi WebBridge verifikáciou, vrátane leadov, ktoré eshop majú, ale oplatí sa ho prerobiť. Discovery: 9 Firecrawl queries → 47 unikátnych IG handles. Verifikácia: Kimi WebBridge (followers/bio/link — **Firecrawl instagram.com nescrapuje**) + curl/DNS + Firecrawl scrape webov (platforma, sold-out počty). Výsledok: **20 kvalifikovaných z 47 (~43 %)** — 10 nožiarov, 10 kožiarov; ~35 vylúčených s dôvodmi. Všetkých 20 otváračov brand-first (dáta: 3/6 vs. tech-first 1/6). Nové: `raw/.../knife-leather-leads-batch8-verified-2026-07-20.md`, [[outreach-batch-8]]; 20 riadkov pridaných do [[cold-outreach-pipeline]] ako `pripravený`. Predošlý neoverený raw súbor batch-8 ponechaný nedotknutý (hard rule) a označený ako nepoužiteľný. Nič neodoslané — čaká na Markovu kontrolu. Poznatky: nože = vypredaný eshop (demand leak), koža = schovaný predaj (bio vedie na blog/linktree/Notion); #5 spiaci účet ≠ lead (margigaba: mŕtva doména, ale posledný post 2021); #6 Firecrawl nevie IG. index.md + log.md aktualizované.

## [2026-07-20] outreach | Batch 8 — 18/20 otváračov odoslaných cez Kimi WebBridge
Na Markov pokyn "send it" odoslané všetkých 20 pripravených IG DM z [[outreach-batch-8]]. Prvý pokus cez profilovú stránku (Message button) fungoval na leade #1, no pri #2/#3 tlačidlo prestalo byť nájditeľné — Marko usmernil na spoľahlivejší flow: `instagram.com/direct/new/` → search handle → Chat → Send. Tento postup fungoval bez zlyhania na zvyšku dávky. **Výsledok: 18/20 doručených** (potvrdené screenshotom modrej odoslanej bubliny v každej konverzácii), **2/20 zablokované Instagramom** — Dark Timber Customs (Peter Kohler) a Lord Leathercraft (Geoffrey) obmedzujú DM len na followerov/mutuals, IG vrátil systémovú správu namiesto doručenia (rovnaký jav ako Raina Nicole Woodworks v batch 7). Aktualizované: [[cold-outreach-pipeline]] (20 riadkov: 18× oslovený s dátumom, 2× označené ako nedoručené), [[outreach-batch-8]] (sekcia Stav odoslania + poznatok #7 o nespoľahlivosti profilového Message tlačidla), index.md.

## [2026-07-20] outreach | Drop Dead Candles — pitch odmietnutý, push follow-up odoslaný
Na priamy pitch (odoslaný 20.7.) odpovedala „I'm ok, thanks though" — odmietnutie. Namiesto zdvorilého uzavretia Marko zvolil druhý, hravejší push follow-up (ironizuje jej „I'm ok", nízkonákladová 15-min ponuka) + link na cart.design ako referenciu práce. Prepis doplnený do [[drop-dead-candles]], stav konverzácie a ďalší krok aktualizované, index.md aktualizovaný. Čaká sa na reakciu.

## [2026-07-20] query | Nový ICP pre SK/CZ DTC značky (nosky.cz, pekne.eu)
Marko chcel osloviť "slovenské brandy ako nosky.cz / pekne.eu". Overenie oboch webov (curl + /products.json)
ukázalo, že nejde o dizajnové značky, ale o priamych konkurentov v nike nosných pások/biohackingu — spoločný
menovateľ je obchodný model, nie estetika. Založený [[icp-dtc-znacky-sk-cz]] (ICP v2: DTC značky s funkčným
Shopify e-shopom, ktorý ich brzdí) + trojvrstvová research infra (Firecrawl discovery → curl kvalifikácia
zadarmo → Kimi WebBridge verifikácia). Nálezy: pekne.eu má prázdny <title>, 111 script tagov; nosky.cz 65
scriptov + produkty za 0 Kč v katalógu. Do [[cold-outreach-pipeline]] pridané poznatky #7 a #8. Leady zatiaľ
nehľadané — čaká sa na Markov pokyn spustiť discovery.

## [2026-07-20] ingest | Batch 9 — DTC značky spánok/dýchanie SK/CZ
Discovery podľa [[icp-dtc-znacky-sk-cz]]: Firecrawl (9 dotazov) + curl kvalifikácia. 3 leady v [[outreach-batch-9]]:
Hevi (hevisleep.sk/.cz), Gudslip (gudslip.cz), Resty (feelresty.com). Správy fázy 1 pripravené, nič neodoslané.
KOREKCIA: nález "pekne.eu má prázdny <title>" z predošlej session je VYVRÁTENÝ — bola to chyba greplu
(titulok pokračoval na ďalšom riadku), nie chyba webu. Falošne označilo 4 z 5 Shopify webov. Head parsovať
Pythonom s re.S, nie riadkovým greplom. Podobne "gudslip je pomalý" (2.22s) bol artefakt paralelného behu,
pri troch samostatných meraniach 0.23s. Vylúčení: naturdrop.cz (HTTP 402, zmrazený Shopify), resellery.
⚠️ Zapísaný konflikt záujmov: nosky/pekne/gudslip/hevi/resty sú navzájom konkurenti.

## [2026-07-20] ingest | Pekne.eu pridané do batch 9, hooky opravené
Nájdený overený hook pre pekne.eu: 111 <script> tagov na homepage (overené 2× nezávisle). Pôvodný vyvrátený
title-hook definitívne nahradený. Zároveň opravená chyba fázy 1 v Hevi správe — draft obsahoval "Robíme
e-shopy" (zmienka o službe), čo porušuje pravidlo cold-outreach-manual (fáza 1 = žiadna zmienka o ponuke);
odstránené. [[outreach-batch-9]] teraz má 4 leady (Pekne, Hevi, Gudslip, Resty), pre každý email aj IG DM
verziu (kde mail existuje). Nič neodoslané, čaká sa na Marka.

## [2026-07-20] ingest | Nino Rostomashvili — mäkké áno s odkladom, follow-up pripravený
Na pivot k „ownership platobných možností" odpísala „Well yes, I think about this option", ale posunula námietku
na **drahé export/poštovné z Gruzínska** + odklad („in nearest future"). Prepis doplnený do
[[nino-rostomashvili]], stav prepnutý na warm/odložené. Pripravený (NEODOSLANÝ) follow-up: oddeliť poštovné od
platformy — je rovnaké nech predáva kdekoľvek, mení sa len to, čo jej zostane po poplatkoch; bariéra znížená
z 15-min callu na konkrétny artefakt (prepočet marže na 2–3 jej reálnych kusoch). Aktualizované:
[[cold-outreach-pipeline]] (riadok Nino), index.md.

## [2026-07-20] ingest | Nino Rostomashvili — soft-close, stopa presunutá do nurture
Na follow-up (oddelenie poštovného od platformy + ponuka prepočtu marže) odpísala „Many Thanks. Will think
about this." — druhé mäkké odloženie za sebou, bez novej námietky a bez otázky. Vyhodnotené ako dojazdené
kolo: **ďalší push zastavený**, status prepnutý `active` → `waiting`/nurture. Zapísaný plán re-touchu
(~09/2026, len s novým dôvodom: prepočet marže z verejných Etsy cien / precedens remeselníka mimo EU-US /
zmena politiky Etsy voči Gruzínsku). Pain point zostáva overený a hodnotný aj do budúcna.
⚠️ Nezrovnalosť: follow-up bol v predošlom zápise vedený ako neodoslaný, no Marko hlásil jej odpoveď naň —
označený ako odoslaný, presný čas a kanál NEOVERENÉ. Aktualizované: [[nino-rostomashvili]],
[[cold-outreach-pipeline]], index.md.

## [2026-07-20] ingest | Batch 9 — variant B (kombinovaná správa) podľa reálneho precedensu Nosky
Marko ukázal skutočnú správu poslanú Jakubovi (Nosky.cz): rapport + technický nález + ponuka prvého
vylepšenia zadarmo + CTA na 15min call, všetko v jednej správe (nie dvojfázovo ako [[cold-outreach-manual]]).
Zapísané ako Variant B v [[outreach-batch-9]] — 4 správy (Pekne, Hevi, Gudslip, Resty), rovnaká kostra,
personalizované overenými hookmi z tejto session. Variant A (fáza 1) ponechaný pre porovnanie, nič nezmazané.
⚠️ Mená zakladateľov neoverené pre všetky štyri (na rozdiel od Jakuba) — správy oslovujú bez mena.

## [2026-07-20] ingest | Chuck Richards Knives — odpoveď na otvárač (batch 8 #1)
Odpísal ako predajca zákazníkovi: „The FreeBird is on sale now and available in all options" — neriešil otázku,
opravil predpoklad o vypredanosti. Tretí výskyt patternu „otvárač ako od zákazníka" ([[lois-gore-hampton-gem]],
[[darcekove-kytice]]). Nový uhol: jeho odpoveď je sama dôkazom hooku — web komunikuje vypredané, pravdu sa
Marko dozvedel až v DM. Vytvorená [[chuck-richards-knives]] s prepisom a pripraveným (NEODOSLANÝM) priznaním
+ reframom. Aktualizované: [[cold-outreach-pipeline]] (riadok Chuck), [[outreach-batch-8]] (#1), index.md.
⚠️ Pred pitchom overiť platobný procesor (nože = high-risk).

## [2026-07-20] ingest | Don Hanson III — druhá odpoveď Marka (IG DM)
Do [[don-hanson-sunfish-forge]] doplnený verbatim follow-up (waitlist/pre-order page + explicitné „I build exactly
this kind of thing for makers", soft close). Donovo poďakovanie medzi správami zatiaľ nezaznamenané — doplniť z IG.
Stav ostáva **waiting**, ďalší krok nezmenený (touch okolo októbra).

## [2026-07-20] ingest | Chuck Richards — fáza 2 odoslaná
Marko odoslal (20.7.) poznanie + reframe: „I went through the site the way a customer would and came away
thinking the FreeBird was gone. You just told me in a DM it's on sale in every option. Everyone landing there
today reads it the way I did — and almost none of them will message you to check." Napísaná krátšia verzia
bez ospravedlnení (Chuck odpísal len jednu vetu, neprispel čas ako Lois). Čaká sa na odpoveď.
Aktualizované: [[chuck-richards-knives]] (stav fázy 2, komunikácia), [[cold-outreach-pipeline]].

## [2026-07-20] ingest | Batch 9 odoslaný — všetky 4 leady
Marko potvrdil odoslanie variantu B (kombinovaná správa) všetkým štyrom leadom z [[outreach-batch-9]]:
Pekne (IG DM), Hevi (email), Gudslip (email), Resty (IG DM). Stavové tabuľky updatnuté v batch-9,
[[cold-outreach-pipeline]] aj index.md — dátum odoslania 2026-07-20, čaká sa na reakcie.

## [2026-07-20] ingest | Gudslip — priamy telefonický kontakt
Marko získal osobné číslo na Gudslip: +420 722 287 570 (WhatsApp/SMS). Píše tam osobne, mimo emailovej
správy odoslanej skôr. Zapísané do [[outreach-batch-9]] ako dodatočný kanál — obsah tejto konverzácie
zatiaľ mimo vaultu, Marko ju rieši sám.

## [2026-07-20] ingest | Chuck Richards — druhá reply, move to email funnel
Chuck odpovedal (same-day) na Markovo poznanie + reframe: „Not one single person says to me they think they're
out of stock. Ok. Email to me. Link in bio" — **qualified signal**. Čistá komunikácia, bez defenzivy, explicitne
žiada email kanál (Link in bio = email v IG bio). Aktualizovaná [[chuck-richards-knives]] (Komunikácia, Stav,
Ďalší krok: extrahovať email a poslať email pitch), [[cold-outreach-pipeline]] a index.md.
Priorita: získať email z IG bio, poslať pitch cez email.

## [2026-07-20] ingest | Gudslip projekt — presun z batch do projects/
Gudslip má teraz vlastný projekt stranku: [[gudslip]]. Info, hooky, stav konverzácie (email odoslaný 20.7.,
WhatsApp draft pripravený), návrhy fázy 1 — všetko zapísané ako projekt, nie len ako položka v batch-9.
Prepojené v index.md a [[cold-outreach-pipeline]].

## [2026-07-20] ingest | Rebecca D Enamel — lajk bez odpovede na správu z 20.7.
Na Markovu poslednú správu (hravá reakcia + ponuka referencií) Rebecca odpovedala len lajkom, žiadny text.
Vlákno prepnuté na pauzu — manžel stavia web sám, ďalší ping sa neodporúča skoro. Aktualizované:
[[rebecca-d-enamel]] (Stav konverzácie #8, Ďalší krok, Zdroje), [[cold-outreach-pipeline]], index.md.

## [2026-07-20] update | Chuck Richards — email draft pripravený v Gmaili
Marko doplnil kontakt: **sales@chuckrichardsknives.com**. Vytvorený Gmail draft (predmet „The FreeBird —
from Instagram") — **neodoslaný**, čaká na Markovu kontrolu. Jadro mailu: potvrdiť Chuckovu námietku
(„nikto mi nepovie, že som vypredaný") a obrátiť ju — zákazník, ktorý odíde, sa neozve, takže absencia
sťažností nie je dôkaz. Marko sám ako dôkaz (ani on to nepovedal, kým sa nepozrel profesionálne).
CTA = walkthrough zadarmo, nie hovor. Aktualizovaná [[chuck-richards-knives]] (Návrh mailu, Ďalší krok).

## [2026-07-20] ingest | Batch 10 — zastarané SK e-shopy (Markov podnet: "maily do SK, horšie eshopy")
Nová línia popri ICP v1/v2: etablované SK firmy s reálnym obratom a zastaraným webom (redesign grade, email).
Metodika: Firecrawl discovery (7 dotazov, 7 kategórií) → kvalifikácia čistým Pythonom/`curl` (skript `qualify.py`,
rozšírenie `stack.sh` o viewport, SSL, charset, jQuery, tables, og). ~50 domén preverených, 4 kvalifikovaní.
Kvalifikovaní: Tatramodel (žiadny viewport = web bez mobilnej verzie, najsilnejší), Vcelo (3.7–4.2 s mobile),
Konvička (2.3–4.2 s), Neoprot (pozdržaný — možno nepredáva online).
Zamietnuté falošné hooky: windows-1250 charset (korektne deklarovaný, chyba dekódovania nie webu),
jQuery 1.11.3 (default Shoptetu, 12 webov), jednorazové meranie rýchlosti (e-luma, ortokomplet vypadli po 4 meraniach).
Vyradený rybarskepotreby-poprad.sk — SEO satelit, nie e-shop.
Nové poznatky #9 (doorway page nie je lead), #10 (platformový boilerplate nie je nález), #11 (rýchlosť merať 4×).
Dotknuté: wiki/outreach/outreach-batch-10.md (nová), cold-outreach-pipeline.md, index.md.
Stav: 3 správy pripravené, **nič neodoslané** — čaká na Markovo schválenie.

## [2026-07-21] setup | Outreach dashboard — jedna stránka s reálnymi číslami
Adamov feedback („nevidím, ako to ide s leadmi a čo ľudia odpisujú") → nová [[dashboard]] v `wiki/outreach/`.
Postavená čisto sčítaním existujúcich batch a project stránok, nič nové sa nezbieralo. Obsah: celkové čísla,
response rate podľa **typu hooku** (SK hyper-personalizovaný 4/6 = 67 % · brand-first 8/35 = 23 % ·
tech-first 1/16 = 6 % · variant B 0/4), podľa kanála (IG 14/59, email 0/5), podľa jazyka (EN 10/52, SK/CZ 4/12),
podľa dávky; tabuľka prompt variantov A/B; stav evalu (nespustený); 16 živých vlákien s ďalším krokom;
7 posledných odpovedí verbatim.

**Overená báza: 64 odoslaných / 14 odpovedí = 21,9 %.** S nezaznamenaným batchom 5 (~21 správ, +8 odpovedí)
vychádza ~26 % — preto sú v dashboarde obe čísla.

**Dve nezrovnalosti nájdené pri zbere (zapísané do sekcie „Čo dashboard zatiaľ nevie", neopravené):**
1. [[outreach-batch-5]] (21 otváračov) **nemá v logu záznam o odoslaní** — posledný zápis hovorí „nič nebolo
   odoslané", no 8 leadov z dávky odpovedalo (Gollik, Nino, Jason Fry, Lobo, Lois Gore, Don Hanson,
   Colin Shannon, Ban Tang). Dávka evidentne odišla ~16.–17.7.; počet a dátum čakajú na Markovo potvrdenie.
2. **Disciple Designed sa počíta dvakrát** — [[outreach-batch-2]] ho vedie medzi svojimi 12 správami, ale
   pipeline datuje oslovenie na 18.6. Denný prehľad preto hlási „17 EN 15.7." pravdepodobne vrátane neho.
   V dashboarde vedený ako pred-vlnový kontakt, 18. EN správou z 15.7. je Drop Dead Candles — sedí to
   s vlastným číslom pipeline „EN 5/18".

Ďalej pripomenutý visiaci akčný bod: mail pre [[sacha-carlos-raps]] (hello@sacharaps.com) stále neodoslaný.
Dotknuté: `wiki/outreach/dashboard.md` (nová), [[cold-outreach-pipeline]] (banner o pauze + link),
index.md (dashboard na prvom mieste v sekcii Outreach). Ďalší krok: skill files na písanie.

## [2026-07-21] setup | Skills na písanie správ — pis-ako-clovek + citatel-nema-cas
Druhý bod Adamovho feedbacku („skills na písanie, nech správy neznejú ako AI; každý lead, ktorý znie
ako AI = horšia reputácia a stratený lead"). Adam poslal dva repozitáre ako vzor — oba naklonované
a prečítané (`github.com/JuliusBrussee/caveman` → `skills/caveman/SKILL.md`,
`github.com/ayghri/i-have-adhd` → `skills/i-have-adhd/SKILL.md`).

Nový priečinok `wiki/outreach/skills/` s tromi stránkami:
- **[[pis-ako-clovek]]** — hlas/textúra, 8 pravidiel + kontrola pred odoslaním. Adaptované z cavemanu
  („umiera len vata, substancia zostáva"). Konkrétne zakázané: dlhá pomlčka `—` (Markov vlastný pokyn,
  `raw/cart.design/flow-outreach.md` r. 27), formulka „Curious:"/„Quick question though:" (máme ju
  skoro v každej EN správe), intenzifikátory (genuinely/seriously/rare/no joke), šablónové lichôtky,
  symetrické vety a triády, emoji ako korenie. Všetky pred/po príklady sú **naše reálne odoslané správy**.
- **[[citatel-nema-cas]]** — štruktúra/dĺžka, 6 pravidiel + kontrola. Adaptované z i-have-adhd
  (tvaruj podľa čitateľa). Háčik v prvom riadku namiesto pozdrav+kompliment, jedna otázka, tvrdé
  limity dĺžky (IG DM 25–50 slov, email 40–80), ľahko zodpovedateľné CTA, nič na dohľadávanie.
- **[[wiki/outreach/skills/index|skills/index]]** — prehľad, pôvod z repozitárov, čo sa zámerne nepreberá.

**Kľúčové zistenie z dát:** skills tlačia EN správy k štýlu, ktorý u nás už vyhráva — SK dávka
(krátke, jeden konkrétny citát z ich postu, jedna otázka) má 4/6 = 67 %, EN dávky (dlhšie, otvárací
kompliment, „Curious:", dlhé pomlčky) 10/52 = 19 %. Nie je to čistý dôkaz (iný trh, malá vzorka),
ale smeruje rovnako ako Origami playbook.

Zámerne **nepreberáme** samotný caveman štýl (vypúšťanie členov, fragmenty) — cold správa cudziemu
človeku nesmie znieť telegraficky. Kontrola hookov (poznatky #3, #4, #9–#11) zámerne **nie je** v
skills — je to kontrola pravdivosti, nie štýlu, patrí do rubriky evalu.

Skills platia **okamžite**, nečakajú na eval — používajú sa na odpovede v živých vláknach počas pauzy.
Zapojené do write flow: [[cold-outreach-manual]] (banner na začiatku + kontrola pred odoslaním v §3b),
[[dashboard]] (nová sekcia 3, sekcie prečíslované), index.md. Ďalší krok: eval (rubrika → fixtures → run A/B).

## [2026-07-21] setup | Automatizácia outreachu — skills /scrape a /send
Outreach flow, ktorý sa doteraz písal ručne v každej session, prevedený do dvoch spustiteľných
Claude Code skills v `.claude/skills/`:
- `/scrape` — trojvrstvový research (Firecrawl discovery → curl/python kvalifikácia → Kimi WebBridge
  verifikácia), dedupe proti vaultu, výstup = nová batch stránka s overenými pain pointmi. Nepíše správy.
- `/send` — brzda pauzy → re-verifikácia hookov v deň odoslania → písanie podľa live variantu A
  + skills (citatel-nema-cas → pis-ako-clovek) → schválenie Markom → doručenie (IG DM cez WebBridge
  `direct/new` flow, email ako Gmail draft) → zápis do batch/pipeline/dashboard/index/log.
Zakódované poznatky: #3 (over v deň odoslania), #5 (spiaci účet), #6 (Firecrawl nescrapuje IG),
#7 (direct/new flow), #11 (rýchlosť 4×), title parsovať v Pythone s `re.S`, brand-first > tech-first,
mail+IG nie ten istý deň.
Dotknuté: `.claude/skills/scrape/SKILL.md`, `.claude/skills/send/SKILL.md`, [[CLAUDE|CLAUDE.md]] (nový
workflow + layout), [[index]] (sekcia Príkazy).

## [2026-07-21] eval | Eval infraštruktúra + prvé dva behy
Tretí bod Adamovho feedbacku („prestaň posielať, skús rôzne prompty, vyber najlepší, iteruj").
Nové: `wiki/outreach/prompts/` (index + [[opener-dvojfazovy-v1]] variant A + [[kombinovana-v1]] variant B,
oba extrahované z manuálu a batch-9 so známymi slabinami) a `wiki/outreach/evals/` (index, [[rubric]],
dva runy). Prompty tým prvýkrát majú ID, verziu a výsledky na jednom mieste.

**Rubrika:** 6 kritérií × 0–2 (konkrétnosť, nevyvrátiteľnosť, akútnosť, anti-AI-smell, formát, rola),
každé naviazané na poznatok #1–#11 alebo pravidlo zo skills.

**Run 1 — [[run-2026-07-21-rubrika-vs-realita]] (hotový).** Oskórovaných 17 reálne odoslaných správ
s uzavretým výsledkom (batch 2 EN + batch 3 SK). **Rubrika NEPREDPOVEDÁ, kto odpíše:** odpovedané 8,13
vs. neodpovedané 8,00 z 12. V SK dávke oddelila čisto (9,0 vs. 6,0), v EN dávke **opačne** (7,6 vs. 8,57).
Dve najlepšie správy (Jake Newell, Forest Nine, 11/12) nedostali nič; najhoršia (Rebecca, 5/12) dala
najsilnejší timing signál vlny. Dôsledok: rubrika prehodená z „predikcia odpovede" na **podlahu kvality**.
Vedľajší nález, ktorý priamo podopiera Adama: **88 % správ (15/17) nesie aspoň jeden AI signál, 41 % tri
a viac** — anti-AI-smell sa nedalo korelovať, lebo nemá varianciu. Ďalší nález: kritérium „rola" ≤1
predpovedalo všetky 3 prípady poznatku #2 (prospekt odpovie ako predajca zákazníkovi).
⚠️ Limit runu priznaný na stránke: skóroval som ja **so znalosťou výsledkov**, nie naslepo — preto je
naplánovaný run 3 (preskórovanie naslepo v novej session).

**Run 2 — [[run-2026-07-21-zmrazene-spravy]] (čaká na Marka).** 4 zmrazené neodoslané leady
(Tatramodel, Vcelo z batch 10; Raina, Doucette z batch 7) × 3 verzie: originál, A-skills, B-skills.
Verzie sú **neoznačené**, kľúč skrytý pod `<details>`. Rubrika favorizuje A-skills 4:0 (10, 10, 12, 11),
originály variantu B padli na 4/12 — nie kvôli hooku, ale kvôli dĺžke, fráze „Nebudem chodiť okolo
horúcej kaše", pomlčkám a pitchu vo fáze 1. **Markov výber prebíja rubriku.**

**Najdôležitejší nález mimo zadania:** akútnosť pain pointu je **0** pri oboch SK leadoch v run 2 —
máme technickú chybu webu, ale žiadny dôkaz, že im dopyt prerastá cez kanál. Presne na tomto zomrela
darcekove_kytice (poznatok #1). Týka sa celej línie [[outreach-batch-10]]. Riziko väčšie než výber promptu.

Dotknuté: prompts/ (3 nové), evals/ (4 nové), [[dashboard]] (sekcie 2 a 4 prepísané), index.md.
Ďalší krok: Markov slepý výber v run 2 → víťaz sa stane `live` variantom pre skill `send`.

## [2026-07-21] lint | Oprava wikilinkov — nejednoznačné a rozbité cesty
Po pridaní `skills/`, `prompts/` a `evals/` sa zvýraznil starší problém: `wiki/conversations/` má 9 stránok
s **rovnakými názvami** ako stránky v `wiki/projects/`, takže holé odkazy typu `[[by-alisha]]` boli
nejednoznačné a Obsidian si vyberal cieľ sám.

**Opravené:**
- **38 nejednoznačných odkazov** (9 mien: by-alisha, darcekove-kytice, drop-dead-candles, hazel-hand-engraving,
  optimistic-soap, rebecca-d-enamel, saint-jewellry, sperky-richterova, sweet-nothings-studios) prepísaných
  na path odkazy `wiki/projects/<meno>` v index.md, dashboard, cold-outreach-pipeline, batch 2, batch 3
  a lois-gore-hampton-gem. Cieľom je vždy **projects/**, lebo conversations/ sú podľa vlastnej hlavičky len
  kurátorské kópie a zdroj pravdy je project stránka. Zobrazované texty zachované.
- **20 rozbitých relatívnych odkazov** ``../projects/x`` vo všetkých 9 conversations stránkach + ich indexe.
  Obsidian **nepodporuje `../` vo wikilinkoch** — tieto odkazy nefungovali od založenia priečinka (16.7.).
  Prepísané na ``wiki/projects/x``. Rovnako ``../../CLAUDE.md`` a ``../outreach/...``.
- **Príklad v CLAUDE.md** (sekcia Konvencie) mal v path wikilinku chýbajúci prefix `raw/` — opravené, aby
  sa podľa neho nekopírovala chyba ďalej.

**Nedotknuté zámerne:**
- **log.md** — append-only žurnál, historické odkazy ponechané tak, ako boli zapísané.
- **Interné odkazy v conversations/** na súrodencov v rovnakom priečinku — Obsidian ich rieši správne
  (same-folder má prednosť).

**Zostávajú 4 visiace odkazy** (neriešené, treba rozhodnutie): `log.md` → `katarina-silna`, `pevne-zuby`
(historické, stránky nikdy nevznikli; pevne-zuby je zámerne mimo wiki v `dh/`);
`nino-rostomashvili` → `jenny-topolski` (stránka neexistuje);
`icp-dtc-znacky-sk-cz` → `cart-design-custom-code` (odkaz mieri na memory súbor mimo vaultu).

Stav po oprave: **0 nejednoznačných, 4 visiace** odkazy v celom vaulte.

## [2026-07-21] eval | Run 2 uzavretý — Markovo slepé zoradenie, vznikol live prompt v2
Marko zoradil všetkých 12 verzií (4 leady × 3) od najlepšej po najhoršiu, bez znalosti kľúča.
Poradia: Tatramodel 1A>1C>1B · Vcelo 2A>2B>2C · Raina 3A>3C>3B · Doucette 4B>4C>4A.

**Výsledok (body 3/2/1):** A-skills 10 b / 4 výskyty (priemer 2,50; 2 prvé miesta, ani raz posledný) ·
A-originál 5 b / 2 (2,50) · B-skills 7 b / 4 (1,75) · **B-originál 2 b / 2 (1,00) — posledný vždy.**

**Tri závery:**
1. **B-originál prehral vždy** — a to sú reálne pripravené maily z [[outreach-batch-10]]. Označené
   na prepis, neposielať v tomto znení.
2. **Rubrika trafila najhoršiu verziu 4/4, najlepšiu 2/4.** Nezávislé potvrdenie záveru z run 1:
   rubrika je podlaha, nie rebríček. V oboch rozporoch bola rubrikina jednotka Markovou dvojkou,
   nikdy nie posledná — smer sedí, rozlišovacia schopnosť na vrchu chýba.
3. **A-skills celkový víťaz** → vznikol [[opener-dvojfazovy-v2]], `status: LIVE`, so skills
   zapracovanými priamo v texte promptu (nie ako druhý prechod).

**Dva rozpory Marko vs. rubrika a čo z nich vzniklo:**
- **Vcelo:** Marko uprednostnil verziu **s predstavením a ponukou** pred holou otázkou, hoci rubrika
  ju trestá za pitch vo fáze 1. → do v2 pridaná výnimka: pri studenom maile etablovanej firme smie
  byť jedna veta „kto som". Dvojfázové pravidlo teda nie je absolútne.
- **Raina:** Marko uprednostnil **originál s komplimentom** (248K, Makita, BRUNT) pred prečistenou
  verziou s tromi AI signálmi menej. → do v2 pridané pravidlo: uznaj status jednou vetou s konkrétnym
  údajom, keď je lead veľký.

⚠️ **Priznaná metodická chyba:** verzie v run 2 menili viac premenných naraz (AI signály + kompliment
+ znenie otázky), takže sa nedá povedať, či za výhrou A-skills stojí odstránenie AI signálov alebo
niečo iné. Naplánovaný **run 3 ako priorita** — izolovaný test, kde sa verzie líšia len v anti-AI-smell
úpravách. Zároveň bola narušená slepota (Marko pred výberom vedel, že rubrika favorizuje A-skills).
Obe limitácie zapísané na stránke behu.

Dotknuté: [[run-2026-07-21-zmrazene-spravy]] (výsledky + limity), [[opener-dvojfazovy-v2]] (nová, live),
[[wiki/outreach/prompts/index|prompts/index]] (stavy: v2 live, v1 baseline, B needs rewrite),
[[wiki/outreach/evals/index|evals/index]] (poznatky #4, #5, prečíslované plánované behy),
[[dashboard]], [[outreach-batch-10]] (varovanie pred odoslaním + akútnosť 0), index.md.

## [2026-07-21] refactor | Prestavba štruktúry — všetko z dnešného dňa konsolidované
Marko: „scrape every data we did today, re-evolve the whole thing, nech máme jasnú štruktúru projektu."
Dokončená migrácia, ktorú som pri prvom pláne zámerne odložil, plus konsolidácia dnešnej práce.

**Presuny (`git mv`, obsah nedotknutý):**
- `wiki/outreach/outreach-batch-{1..10}.md` → `wiki/outreach/batches/`
- `biorythme`, `gollik-knives`, `nino-rostomashvili`, `outreach-links` → `wiki/outreach/prospects/`
- `wiki/conversations/` → **`wiki/outreach/fixtures/`** (9 konverzácií + index; sú to eval fixtures,
  nie archív — pomenovanie teraz zodpovedá funkcii)
- `wiki/feedback/flow-feedback.md` → `raw/cart.design/flow-feedback.md` (Markove surové poznámky
  patria do raw vrstvy; **nie je to duplikát** — prvých 66 riadkov je zhodných s `flow-outreach.md`,
  ale každý súbor má vlastný záver, takže sú to dva snapshoty a oba ostávajú)

**Nové stránky:**
- **[[insights]]** — kanonický domov poznatkov #1–#17. Pri zbere sa ukázali **tri kolízie v číslovaní**:
  „#5" a „#6" z `log.md` 20.7. (geografické platby, duplicitný kanál) a „#7" z [[outreach-batch-8]]
  (Message tlačidlo) kolidovali s existujúcimi. Čísla #1–#11 ponechané bez zmeny (odkazuje sa na ne
  z manuálu, rubriky aj skills), kolidujúce prečíslované na #12–#14, dnešné poznatky pridané ako
  #15–#17. Na stránke je prekladová tabuľka starých odkazov.
- **[[icp-handmade-makers]]** (ICP v1) a **[[icp-zastarane-sk-eshopy]]** (ICP v3) — dovtedy žili len
  ako sekcie v pipeline, hoci v2 mal vlastnú stránku od začiatku. Teraz sú všetky tri porovnateľné.
- **[[outreach-day-2026-07-21]]** — denný prehľad: Adamove tri body a čo z nich vzniklo, čísla, dva
  evaly, čo sa prestavalo, štyri veci, ktoré ostali nedokončené.

**[[cold-outreach-pipeline]] zoštíhlená z 276 na 211 riadkov** — ostala tabuľka prospektov a stav,
ICP a poznatky nahradené ukazovateľmi. Nič sa nestratilo, všetko má nový domov.

**[[CLAUDE|CLAUDE.md]] aktualizovaný:** nový strom `wiki/outreach/` (batches, prospects, fixtures,
prompts, skills, evals), **nový workflow Eval** (fixtures → varianty → rubrika → slepý výber →
zápis; „Markov výber prebíja rubriku", „meň jednu premennú naraz"), doplnená konvencia o path
wikilinkoch vrátane varovania, že Obsidian nepodporuje `../`. Štyri nové hard rules: každá správa
cez skills + `live` variant · žiadne nové otvárače počas pauzy · každá outreach zmena updatne
dashboard · poznatky sa neprečíslovávajú.

**index.md** — sekcia Outreach prepísaná podľa novej štruktúry (dashboard prvý, potom prompts/
skills/ evals/ batches/ prospects/ fixtures/), doplnené insights, denný prehľad a obe nové ICP.

Kontrola odkazov po migrácii: **0 nejednoznačných, 4 visiace** (nezmenené: `katarina-silna`,
`pevne-zuby` v log.md, `jenny-topolski`, `cart-design-custom-code`).

## [2026-07-21] scrape | staré SK e-shopy, západné Slovensko — 3/31 kvalifikovaných

[[outreach-batch-11]] — pokračovanie [[icp-zastarane-sk-eshopy|ICP v3]] s geografickým filtrom
(Trnavský, Nitriansky, Trenčiansky, Bratislavský kraj). Firecrawl (8 dotazov) → `qualify.py`
(curl, zadarmo) na 31 kandidátoch. Kvalifikovaní: **IMI Nitra** (iminitra.sk + sesterská
modelarstvoimi.sk — žiadny viewport, jQuery 1.7.2, konzistentne pomalý mobile, katalóg 10 075
produktov), **RehaCARE** (2.47–2.67 s na mobile 4×, 20+ výdajných miest po SK) a **Rybárstvo
Trnava** (platforma sama deklaruje `is_responsive_layout = false`; ⚠️ slabší fit, biznis
neoverený). Cestou objavená a opravená chyba v `qualify.py`: `subprocess` s `text=True` padal na
windows-1250 stránkach a tri žive domény nahlásil ako mŕtve — bez opravy by dávka prišla o
najsilnejší nález. Žiadne správy napísané, nič odoslané. Dedupe overený — žiadny z troch leadov
nebol predtým oslovený. Zápis: [[outreach-batch-11]], raw
`zapadne-slovensko-eshopy-batch11-verified-2026-07-21.md`, [[dashboard]], [[cold-outreach-pipeline]],
[[icp-zastarane-sk-eshopy]], `index.md`.

## [2026-07-21] scrape | US ~5-ročné builder e-shopy (bez ICP) — 5/37 kvalifikovaných

[[outreach-batch-12]] — Markov podnet: „5 year old shopify or other builder platforms Eshops based
in USA with active business and social media sites. Don't use icp." Firecrawl (16 dotazov
`"established 2020/2021" + nika`, --country us) → 37 kandidátov → `qualify.py` (curl + whois/RDAP
vek domény) → Kimi WebBridge (15 IG profilov). Kvalifikovaní: **Home Bound Custom Decor** (39,1K,
Dawn Copy default šablóna), **Corn Crib Candles** (31K, 33/238 vypredaných), **Earth Berry
Apothecary** (14,1K, story brand na Dawn), **Bounding Main** (3 predajne CA, Copy of Dawn + 83
scriptov), **Ember Coffee** (89 scriptov; ⚠️ theme názov naznačuje redesign 2025). Metodické
nálezy: whois `created:` vracia TLD záznam (nutný `Creation Date:` + RDAP); prvý IG post býva
pripnutý (dátum aktivity = max z prvých 4); `Shopify.theme` JSON s theme_store_id 887 = lacný
tvrdý dôkaz default šablóny; „est. 2020" branding ≠ vek domény (4× rozpor). Žiadne správy
napísané, nič odoslané. Zápis: [[outreach-batch-12]], raw
`us-5yr-builder-eshops-batch12-verified-2026-07-21.md`, [[dashboard]], `index.md`.

## [2026-07-21] ingest | Batch 12 prepnutá do bulk režimu (Markov pokyn)

[[outreach-batch-12]] prepísaná: nesie všetkých 37 kandidátov namiesto len kvalifikovanej pätice.
Štruktúra per lead: ✅ overení (5, pripravení pre /send) · 🟡 na doverenie pri odoslaní (20, so
stĺpcom „čo doveriť") · ⛔ nepoužiteľní (12 — vek domény mimo ~5 rokov, mimo USA, mŕtve/odhadnuté
domény). Aktualizované: [[dashboard]] (riadok dávky), `index.md`. Žiadne správy, nič neodoslané;
pauza outreachu platí.

## [2026-07-21] ingest | Batch 12: všetkých 37 do send queue, pauza overridnutá (Markov pokyn)

Tretia iterácia batch 12: Marko — „Ešte raz všetkých 37. Kľudne môžeme aj toto skúsiť." + pokyn
vytvoriť a poslať správy. [[outreach-batch-12]] prerobená na send queue s vlnami: ✅ 5 overených
(písať hneď) · 🟡 20 doveriť pri príprave · 🔴 12 mimo pôvodného zadania (vek/US/mŕtve domény) —
vedomé rozhodnutie skúsiť, kontakty treba dohľadať. Pauza outreachu pre túto dávku overridnutá
Markom; podmienka obnovenia splnená (live variant [[opener-dvojfazovy-v2]] = víťaz eval run 2).
Schvaľovacia brána platí. Aktualizované: [[dashboard]], `index.md`. Nasleduje /send fáza.

## [2026-07-21] send | batch 12 vlna 1 — 5 odoslaných, 0 zablokovaných

Marko schválil varianty 1A 2B 3B 4B 5A. Odoslané cez IG DM (Kimi WebBridge, direct/new flow,
screenshoty bublín ako dôkaz, 12:16–12:27): Home Bound Custom Decor, Corn Crib Candles, Earth
Berry Apothecary, Bounding Main, Ember Coffee. Prvé reálne odoslania live promptu
[[opener-dvojfazovy-v2]]. Hooky overené v deň odoslania (viď scrape zápis vyššie). Zapísané:
[[outreach-batch-12]] (plné znenia), [[cold-outreach-pipeline]] (+5 riadkov),
[[dashboard]] (69 odoslaných, brand-first 40, IG 64, EN 57, variant v2 5/0), `index.md`.
Popri odosielaní videné nové odpovede v IG inboxe: Nick Anger, Lois Gore, Colin Shannon,
by Alisha, Daniel Collier (Iron Grove) — čakajú na ingest.

## [2026-07-24] ingest | IG inbox seen/responded sweep (Kimi WebBridge) + 4 odpovede odoslané

Marko: „analyzuj cez Kimi WebBridge všetky chaty, ktoré videli/odpovedali na správu, a ak treba
napíš im správu." Prešiel IG inbox. **Odpovedali (spracované):** Ember Coffee, Lobo Gun Leathers,
Nick Anger, Lois Gore, Colin Shannon, by Alisha, The Local Branch, Iron Grove (Daniel Collier).
**Nevidené (mimo scope):** Bounding Main, Earth Berry, Corn Crib, Home Bound (batch 12, bez Seen).

Marko schválil a **odoslané 4 odpovede v živých vláknach** (cez WebBridge, overené na stránke):
Ember (reframe subscription), Lobo (form = pred-filter), Nick Anger (priznanie + hook 107K),
Lois Gore (slušný close). Všetky písané podľa [[pis-ako-clovek]] + [[citatel-nema-cas]], live variant
[[opener-dvojfazovy-v2]]. **The Local Branch pozdržaný** (Markovo rozhodnutie: slabý fit + otázka na
Seen). **Iron Grove draft neodoslaný** — nebol v schválenej päťke, hook bol mimo (funguje iná doména
irongrovetoolcompany.com), čaká na schválenie.

Nové/aktualizované stránky: [[nick-anger-knives]], [[ember-coffee]], [[the-local-branch]],
[[iron-grove-tool-co]] (nové); [[lobo-gun-leathers]], [[lois-gore-hampton-gem]] (→ done),
[[colin-shannon-shannon-steel-labs]], [[wiki/projects/by-alisha|by-alisha]] (doplnený chýbajúci
mid-negotiation blok + presun na WhatsApp, Marko dal číslo 21.7.). Dashboard: +4 respondenti
(18/69 = 26,1 % RR; brand-first 12/40 = 30 %; batch 8 → 4 odpovede, batch 12 → 1). Pipeline riadky
Nick/Iron Grove/Local Branch/Ember aktualizované. `index.md` doplnený.

Pozn.: batch 12 vlna 1 má IG timestamp 22.7 (log dávku datoval 21.7) — zaznamenané na [[ember-coffee]].

## [2026-08-03] ingest | IG inbox (Kimi WebBridge) + Gmail audit — 10-dňová medzera

Marko: „niekoľko ľudí odpovedalo, pozri to a spracuj, pozri aj mail." Kimi WebBridge extenzia sa
najprv nepripájala (`no extension connected`), po retry (na Markov pokyn) fungovala. Prešitý celý IG
inbox (žiadne pending message requests) a Gmail (`in:inbox`/`in:sent` za posledných ~14 dní +
cielené thread lookupy).

**Nové odpovede (IG DM):**
- [[wiki/projects/orox-leather-co|orox-leather-co]] (nová stránka) — reagoval pozitívne 25.7.,
  potvrdil pain point bez obrany („small team... should integrate it more").
- [[wiki/projects/gems-of-california|gems-of-california]] (nová stránka, ex-„Miners Ink" z
  [[outreach-batch-2]]) — reagoval 27.7. po 12 dňoch ticha; pôvodný hook (mŕtva DNS) je teraz stale,
  web opravil; predaj fragmentovaný web+eBay+Etsy, ceny cez DM.
- [[wiki/projects/biorythme|biorythme]] — reagovala na IG 25.7., CEO sama potvrdila „hacking" custom
  platformy pri každej zmene. **Presunutá z `outreach/prospects/` do `wiki/projects/`** (graduuje ako
  teplý lead) — pôvodná stránka predpokladala, že správa ešte nebola odoslaná; v skutočnosti bola
  odoslaná duálne (email + IG) už 15.7.
- [[lobo-gun-leathers]] — definitívne odmietol na priamu otázku „Do you need an eshop?" → „No we are
  good" (~28.7.). Status → `done`.

**Nové zistenia (email, Gmail):**
- [[chuck-richards-knives]] — celé emailové vlákno malo **nesprávne poradie aj neúplný obsah**.
  V skutočnosti: (1) prvý mail 13:04 mal CTA (walkthrough zadarmo) a argument, nie „len počúvanie" ako
  tvrdil predchádzajúci log záznam z 20.7.; (2) Chuck odpovedal 13:06 „take another look, what's your
  solution"; (3) Marek odpovedal 13:52 verziou „Which is it?" (tá, ktorú predošlý zápis mylne označil
  za jediný/prvý mail); (4) Chuck odpovedal 14:53 „Thanks! 🙏" — **táto štvrtá správa vôbec nebola
  zaznamenaná**. Vlákno je uzavreté v teplom bode, CTA nikdy nezopakovaný — otvorený follow-up.
- [[wiki/projects/pekne|pekne]] (nová stránka) — email na info@pekne.eu (20.7., adresu [[outreach-batch-9]]
  označoval za nenájdenú) dostal odpoveď ten istý deň: odmietol. Zatvára otvorenú medzeru z batch-9
  („Marko uvádza, že už oslovil — vo vaulte o tom nie je záznam").
- [[outreach-batch-10]] — 3 pripravené maily (Tatramodel, Vcelo, Konvička) boli **v skutočnosti
  odoslané** 20.–21.7., napriek výslovnej výhrade na stránke dávky („v tomto znení ani neposielať").
  Žiadna odpoveď zatiaľ (13–14 dní). Nejasné, či šlo o vedomé rozhodnutie alebo časový súbeh (mail
  odišiel skôr, než bola výhrada dopísaná) — otvorená otázka pre Marka.
- Kanál „Email" v [[dashboard]] je celkovo podhodnotený — Gmail obsahuje viac odoslaných mailov, než
  bolo kedy zapísané do batch stránok (pravdepodobne aj Jason Fry/Lobo/Don Hanson duálny kanál).
  Presné číslo si vyžaduje samostatný lint pass, nebolo súčasťou tohto ingestu.

**Aktualizované stránky:** [[chuck-richards-knives]], [[lobo-gun-leathers]] (→ done),
[[outreach-batch-2]], [[outreach-batch-8]], [[outreach-batch-9]], [[outreach-batch-10]],
[[cold-outreach-pipeline]], [[dashboard]] (73/22, ~30 % RR), `index.md`. Nové: [[wiki/projects/orox-leather-co|orox-leather-co]],
[[wiki/projects/gems-of-california|gems-of-california]], [[wiki/projects/pekne|pekne]]. Presunutá:
[[wiki/projects/biorythme|biorythme]] (z `outreach/prospects/`).

## [2026-08-03] send | Fáza 2 — odpovede 4 živým vláknam, ktoré reagovali

Marko schválil 4 návrhy (napísané podľa [[pis-ako-clovek]] + [[citatel-nema-cas]], live variant
[[opener-dvojfazovy-v2]]) a povedal odoslať. **3 doručené cez Kimi WebBridge (IG DM), 1 ako Gmail
draft** (API vie len draft, nie send):

- [[wiki/projects/orox-leather-co|orox-leather-co]] — IG DM odoslaná a doručená (screenshot overený).
- [[wiki/projects/gems-of-california|gems-of-california]] — IG DM odoslaná a doručená.
- [[wiki/projects/biorythme|biorythme]] — IG DM odoslaná, „Seen" takmer okamžite.
- [[chuck-richards-knives]] — **draft vytvorený v Gmaile** (reply v pôvodnom vlákne), **čaká na
  Markovo kliknutie Send** — Gmail MCP nedokáže odoslať priamo.

Aktualizované stránky (Komunikácia/Ďalší krok), [[cold-outreach-pipeline]] (dátum follow-upu),
[[dashboard]] (§5 živé vlákna).

## [2026-08-04] scrape | CREATIVE sites klienti — 11/35 kvalifikovaných

Nová discovery metóda na Markov podnet: hľadanie SK firiem podľa pätičkového kreditu
`"Created by CREATIVE sites"` (klienti agentúry creativesites.sk) namiesto hľadania podľa niky.
Firecrawl search (2 dotazy) + scrape `creativesites.sk/referencie` → **35 kandidátov**, 0 kolízií
s existujúcim pipeline.

Kvalifikácia `curl` (prahy zo `stack.sh`) ukázala, že väčšina webov je technicky zdravá — klasický
"web je rozbitý" hook z [[icp-zastarane-sk-eshopy|ICP v3]] väčšinou neplatí. Marko po medzipristátí
zvolil overiť všetkých 35 do hĺbky cez Kimi WebBridge (skutočný prehliadač) namiesto zúženia na
najsilnejších ~10. Výsledok: **2 s priamou technickou chybou** (rebelkids.sk úplne nedostupný,
zuppashop.com neplatný SSL — "Privacy error" v Chrome) + **9 so statickým copyright rokom v
pätičke** (7–13 rokov starý, potvrdené celotextovým skenom proti falošným nálezom — jeden
kandidát, lull.sk, bol takto odhalený a vyradený napriek `© 2015`, lebo mal aktívne blogové
príspevky z 2026). Nový poznatok #18 v [[insights]].

**Nové stránky:** [[outreach-batch-13]], `raw/cart.design/cold-outreach/creative-sites-sk-batch13-verified-2026-08-04.md`.
**Aktualizované:** [[dashboard]], [[icp-zastarane-sk-eshopy]], [[insights]] (#18), `index.md`.
Žiadne správy napísané ani odoslané — čaká na `/send`.

## [2026-08-04] send | Batch 13 — 1 odoslaný, 9 draftov, 1 vyradený

Marko overridol pauzu explicitne pre batch 13. Re-verifikácia v deň odoslania (bez výnimky):
všetkých 11 hookov ešte platilo, okrem **ZUPPA** — jej Instagram bio vedie na `zuppa.sk`, funkčnú
doménu mimo CREATIVE shop, čiže firma sa medzičasom presunula preč zo `zuppashop.com` (odtiaľ
neplatný SSL). Hook zahodený, ZUPPA vyradená z dávky bez náhrady.

Napísaných 11 správ podľa [[pis-ako-clovek]] + [[citatel-nema-cas]], live variant
[[opener-dvojfazovy-v2]]. Marko schválil všetko naraz.

- **Rebel Kids** — IG DM odoslaná a doručená cez Kimi WebBridge (`@rebelkids_slovakia`), screenshot
  potvrdený.
- **9 emailov** (AFG.sk, Prezuvky.sk, Robel, DATES MOBILE, Reconvel, Alice & Alice, JohnGarfield.sk,
  PROFIO Electronics, Moe4Kids) — vytvorené ako **Gmail drafty** (MCP nevie odoslať priamo), čakajú
  na Markovo kliknutie Send.

**Aktualizované:** [[outreach-batch-13]] (plné znenia + stav doručenia), [[cold-outreach-pipeline]]
(11 nových riadkov), [[dashboard]] (§1 čísla, §2 hook/kanál/jazyk, banner), `index.md`.

## [2026-08-05] scrape | DTC kozmetika/doplnky/káva SK-CZ — 5/27 kvalifikovaných

`/scrape` na Markov povel „dalsi batch /scrape". ICP a nika zvolené cez otázku Markovi: **ICP v2**
(DTC značky SK/CZ), nová nika (kozmetika, doplnky výživy, pražiarne kávy) — zámerne mimo klastra
nosky.cz/pekne.eu/Hevi/Gudslip/Resty z [[outreach-batch-9]] (nosné pásky/biohacking), aby sa
predišlo konfliktu záujmov.

**Discovery:** Firecrawl search, 12 dotazov → 27 unikátnych kandidátov po dedupe proti celému
`wiki/`+`raw/` (0 kolízií; Biorythme sa objavila vo výsledkoch, ale je to už živý lead, vylúčená).

**Kvalifikácia (curl + `/products.json`, `stack.sh` z [[icp-dtc-znacky-sk-cz]]):** 6 prežilo prah
(scripty>80 alebo čas>1,5s, 4× overené pri hraničných prípadoch — poznatok #11 potvrdil falošný
nález na brainmax.cz).

**Verifikácia (Kimi WebBridge, Instagram):** 5 kvalifikovaných — **Facederma** (109 scriptov, 33,6K
followerov), **Panakeia** (93 scriptov, 14,4K), **Zlaté Zrnko** (138 scriptov, 10,9K), **Flow
nutrition** (107 scriptov, 22,3K, ⚠️ recency neistá), **Androrganics** (dve nezávislé domény
.eu/€ a .cz/Kč, vlastný jQuery/Bootstrap kód; len 833 followerov, ale demand doložený partnerstvom
s FC Nitra a HK Nitra). **Medisin** zamietnutý napriek potvrdenému pain pointu (4× meraná pomalosť
2,25–2,63s) — len 467 followerov, pod ICP v2 prahom 5K bez iného dôkazu dopytu.

Ďalšie zamietnutia s dôvodom: cosibella.sk (multibrandová drogéria, nie DTC značka), brainmax.cz
(falošný nález rýchlosti + je to podstránka resellera BrainMarket), vjem.sk (chybný odhad domény —
stránka je nesúvisiaci Lovable-generovaný projekt).

Žiadne správy napísané, nič odoslané — čaká na `/send`.

**Založené:** [[outreach-batch-14]], `raw/cart.design/cold-outreach/dtc-sk-cz-batch14-verified-2026-08-05.md`.
**Aktualizované:** [[cold-outreach-pipeline]] (6 nových riadkov), [[dashboard]] (banner + §1 tabuľka
podľa dávky), `index.md`.

## [2026-08-05] send | batch 14 — 5 napísaných, 5 Gmail draftov (čakajú na Send)

`/send` na Markov povel. Krok 0: cold outreach bol `PAUSED` od 21.7. — Marko explicitne
potvrdil override pre celý batch 14 (otázka + odpoveď "Ano, poslat cely batch 14").

**Krok 1 — re-verifikácia (v deň odoslania):** všetkých 5 script-count hookov sa zhodovalo presne
s hodnotami zo scrape ráno (Facederma 109, Panakeia 93, Zlaté Zrnko 138, Flow nutrition 107).
Androrganics dual-doména potvrdená ešte čistejšie: .eu = 38× €/0× Kč, .cz = 0× €/47× Kč — žiadne
krížové meny, hook silnejší než pri scrape.

**Krok 2 — správy** napísané podľa [[citatel-nema-cas]] + [[pis-ako-clovek]], live variant
[[opener-dvojfazovy-v2]] (brand-first vsuvka + jeden overený fakt + jedna otázka, 41–49 slov).

**Krok 3 — schválenie:** Marko schválil všetkých 5 naraz vrátane Flow nutrition, napriek ⚠️ neistej
IG recency (najnovší jasne datovaný post 7.7., 29 dní — hranica poznatku #5).

**Krok 4 — doručenie:** kanál email pre všetkých 5 (ICP v2 sekvencia, deň 0). Gmail MCP vie len
vytvoriť draft, nie odoslať — všetkých 5 vytvorených ako drafty, čakajú na Markovo kliknutie Send:
Facederma (ondrik.filip@facederma.sk), Panakeia (panakeia@panakeia.sk), Zlaté Zrnko
(objednavky@zlatezrnko.sk), Androrganics (info@androrganics.eu), Flow nutrition
(tym@flow-nutrition.cz).

**Aktualizované:** [[outreach-batch-14]] (plné znenia + stav), [[cold-outreach-pipeline]] (5 riadkov
na `status: osloveny`), [[dashboard]] (banner, §1 „Pripravené, neodoslané" 11→16, tabuľka podľa
dávky), `index.md`.

## [2026-08-05] scrape | Ad Library SK/CZ DTC — 5/13 kvalifikovaných (batch 15)

`/scrape` na Markov podnet („vieme ich nájsť ešte viac, napr. shopify / creative sites?"). Namiesto
Shopify fingerprintu alebo CREATIVE-sites tricku (mimo scope pre ICP v2) zvolený **FB/IG Ad Library**
— dokument [[icp-dtc-znacky-sk-cz]] ho odporúčal ako najlepší zdroj pre ICP v2 od 20.7., ale doteraz
nepoužitý (batch 9 aj 14 išli cez Firecrawl search).

**Discovery:** Kimi WebBridge na facebook.com/ads/library, 3 dotazy (kozmetika SK ~1600 výsledkov,
doplnky výživy SK ~160, kosmetika CZ ~2700). 13 kandidátov po vyradení veľkých/multibrandových
hráčov priamo pri prezeraní (Notino, Vilgain, Dermacol, Glamot.sk, Elnino, Protein.sk, Fitham.sk,
NANAcare) a dedupe (0 kolízií).

**Kvalifikácia + verifikácia:** **5/13 kvalifikovaných (38 % strike rate, najvyšší v ICP v2)** —
**Bloom Robbins** (115K followerov, tri nezávislé Shopify obchody .sk/.cz/.com, najsilnejší hook
zatiaľ v celom vaulte), **Doktorka Sandra** (47,4K, web konzistentne 3,1–6,4s pri 4× meraní, MD
PhD dermatologička), **InaEssentials.SK** (12,2K, 95 scriptov), **StretchFit Slovensko** (8,8K,
88 scriptov + samostatná .cz doména, ⚠️ IG posledný organický post 17 mesiacov starý, ale aktívna
platená reklama = alternatívny dôkaz dopytu), **Tomas Arsov** (35,2K, 82 scriptov).

**Metodický nález:** StretchFit prípad ukázal, že pri Ad-Library-sourced leadoch treba poznatok #5
(spiaci účet) čítať inak — bežiaca platená reklama je priamejší dôkaz dopytu než organický posting.
Navrhnuté ako budúci poznatok v [[insights]], zatiaľ len zaznamenané v batch stránke.

**Vzorec:** 3 z 5 kvalifikovaných v tejto dávke majú duplicitnú SK/CZ (alebo viac) doménovú
infraštruktúru — tretí výskyt po Hevi (batch 9) a Androrganics (batch 14).

Žiadne správy napísané, nič odoslané — čaká na `/send`.

**Založené:** [[outreach-batch-15]], `raw/cart.design/cold-outreach/ad-library-sk-cz-batch15-verified-2026-08-05.md`.
**Aktualizované:** [[cold-outreach-pipeline]] (5 nových riadkov), [[dashboard]] (banner + tabuľka
podľa dávky), `index.md`.

## [2026-08-10] scrape | Ad Library, široký záber (ktokoľvek s aktívnou reklamou) — 12/281 kvalifikovaných

Marko zadal cieľ 50 leadov, niku uvoľnil úplne — jediná podmienka: aktívne bežiaca reklama. Namiesto
jednej kategórie prehľadaných 20 kľúčových slov naprieč SK aj CZ v FB/IG Ad Library (kabelky, obuv,
šperky, hračky, bytový textil, zvieratá, outdoor, darčeky, hodinky, plavky, bielizeň, matrace,
bicykle, záhrada, kancelária + CZ ekvivalenty).

352 unikátnych domén → 281 po vyradení veľkých reťazcov/marketplace pri triedení (Alza, Notino,
Decathlon, GymBeam, Northfinder, Sashe, Biano, atď.) → dedupe proti vaultu (2 kolízie: maluna.sk,
miraoffice.sk, už v pipeline) → **44 prekročilo prah bolesti** po voľnej kvalifikácii (`stack.sh`) →
26 z 44 overených cez Kimi WebBridge (čas) → **12 kvalifikovaných**, 14 zamietnutých, 18 v rezerve.

**Prečo len 12, nie 50:** široký záber bez cielenej niky naráža hlavne na resellerov/distribútorov
cudzích značiek (dohor.sk, outdoormania.sk, puls.cz, attractiv.sk, najnosice.sk — 5 z 14 zamietnutí,
tvrdý diskvalifikátor ICP v2) a príliš veľké/medzinárodné značky, ktoré technicky prešli scriptovým
prahom, ale nesedia na personu mladého zakladateľa (lelosi.sk 148K, snuggs.sk 107K followerov).
Cielené niky majú vyšší strike rate práve preto, že sú užšie.

**Najsilnejší hook zatiaľ v celom vaulte:** Vera Italy (dámske kabelky, duálna .sk/.cz doména) —
**1 893 duplicitných inline `<script>` blokov** na homepage, stránka 2,7 MB. Ďalší: Agátin svet
(11,1K, 2,97s odozva), Gardj (5,04s odozva, sauny/skleníky), Šperky od Petry, Alori.cz (32,2K
followerov, nano kozmetika), Vitapur, Amarost (výrobca matracov), Historické darčeky (⚠️ IG mlčí 9
mes., ale aktívna reklama), Muzza ⚠️, Profitent ⚠️, Fotodeky.cz ⚠️ (0 organických postov), KKTKY
(registrovaná ochranná známka, 6K followerov, post dnes).

Žiadne správy napísané, nič odoslané — čaká na `/send`. 18 preverených-ale-neoverených kandidátov je
pripravená rezerva pre ďalšiu session, ak treba dohnať bližšie k 50.

**Založené:** [[outreach-batch-16]], `raw/cart.design/cold-outreach/ad-library-broad-batch16-verified-2026-08-10.md`.
**Aktualizované:** [[cold-outreach-pipeline]] (12 nových riadkov), [[dashboard]] (banner + 2 tabuľky),
`index.md`.

## [2026-08-10] ingest | Nosky.cz — celý emailový prepis s Jakubom Cahom
Marko dodal doslovné znenie celého vlákna (6 správ), ktoré vo vaulte dovtedy chýbalo — poznali sme
len parafrázu kostry v [[outreach-batch-9]] („precedens variantu B"). Realita je oveľa ďalej než
vault tvrdil: Jakub odpísal **3×**, dostal report na `nosky.cart.design`, prešiel ho („má to hlavu
a patu"), sám ponúkol referenciu a požiadal **„ozvěte se pls na konci července, to budu ready
to začít řešit"**. Marko potvrdil. Koniec júla uplynul, follow-up neodišiel → Nosky je najteplejší
lead ICP v2 a je po termíne.

Overené 10.8. (`curl` + `/products.json`): nosky.cz má **67 `<script>` tagov** (20.7. ich bolo 65),
23 produktov, dva stále za 0,00 Kč, homepage 0,48 s. UX/UI prepracovanie, o ktorom Jakub písal, sa
na homepage technicky neprejavilo. `nosky.cart.design` je stále online (HTTP 200).

⚠️ **Oprava eval záznamu:** variant B ([[kombinovana-v1]]) bol evidovaný ako 7 odoslaných / 0
odpovedí. Nosky sa doň nikdy nezapočítalo, hoci je to jeho zdrojový precedens **a jediná jeho
správa, ktorá odpoveď dostala** → **8 / 1 (13 %)**. Verdikt „needs rewrite" zostáva (Marko ho
v run 2 zoradil naslepo posledný), ale prepis na `kombinovana-v2` má vychádzať z doslovného znenia.

⚠️ Dátumy jednotlivých správ nie sú overené (prepis prišiel bez timestampov) — doplniť z Gmailu.

Follow-up napísaný podľa [[citatel-nema-cas]] + [[pis-ako-clovek]], dve verzie, **neodoslaný,
čaká na Markovo schválenie**.

**Založené:** [[wiki/projects/nosky|nosky]] (info, celý prepis, technický stav, draft follow-upu).
**Aktualizované:** [[cold-outreach-pipeline]] (nový riadok), [[dashboard]] (banner),
[[wiki/outreach/prompts/index|prompts/index]] (čísla variantu B), `index.md`.

## [2026-08-10] send | Nosky — follow-up po uplynutí termínu (schválený, nedoručený)
Marko schválil verziu A s úpravou: **celé po slovensky**. Prvý draft zrkadlil Jakubove české slová
(„budeš ready to začít řešit"); Marko to zamietol → nový poznatok: zrkadlenie formulácií leadu
nesmie prekročiť jazykovú hranicu, píšeme po slovensky aj českému leadu.

Finálne znenie (na [[wiki/projects/nosky|nosky]]): pripomenutie jeho vlastného záväzku + link na
`nosky.cart.design` + jedna otázka s ľahkým únikom.

⚠️ **Nedoručené odtiaľto.** Gmail hľadanie (`nosky`, `jakub@nosky.cz`, `in:anywhere`) nevrátilo nič
— pripojená schránka je `marko@merge.build`, ale vlákno je podpísané `marek@cart.design`. Draft sa
tu nedá založiť ako odpoveď do vlákna, ani sa nedajú doplniť chýbajúce dátumy správ. Čaká sa na
Markovo rozhodnutie, z ktorej schránky ide.

## [2026-08-10] send | Batch 15 + 16 — 15 správ napísaných, 2 doručené naživo, 13 draftov

Marko: „send... ako najviac správ [na oboch platformách]." Spracované [[outreach-batch-15]] (5 leadov,
qualifikované 5.8., ešte nemali správy) a [[outreach-batch-16]] (12 leadov, qualifikované dnes ráno)
spolu, 17 leadov celkovo, override pauzy.

**Krok 1 — re-verifikácia (bez výnimky, curl 4×, poznatok #11):** batch 15 hooky všetkých 5 prežili
(Bloom Robbins ×3 domény, Doktorka Sandra medián 2,5s, InaEssentials 97 scriptov, StretchFit ×2
domény, Tomas Arsov 87 scriptov). Batch 16: **2 hooky neprežili** — Alori.cz (pôvodne 1,74s, dnes
medián 0,81s zo 4 meraní, len 23 scriptov) a Fotodeky.cz (pôvodne 1,86s, dnes medián 1,36s, pod
prahom 1,5s). Podľa pravidla skillu („hook ktorý neprežil sa zahodí, nevymýšľa sa náhrada") oba
vypadli zo zoznamu na odoslanie. Gardj's rýchlostný hook tiež nesedel (5,04s → dnes 0,2–0,3s,
zrejme jednorazový výkyv servera), prerámovaný na script count (94), ktorý držal nezávisle.

**Krok 2–3 — písanie a schválenie:** 15 správ napísaných podľa [[opener-dvojfazovy-v2]] (live) +
[[citatel-nema-cas]] + [[pis-ako-clovek]], brand-first. Marko schválil všetkých 15 v plnom znení
bez úprav.

**Krok 4 — doručenie:**
- **IG DM (2, doručené naživo cez Kimi WebBridge):** InaEssentials.SK (@inaessentials.sk, 9:21) a
  Vitapur (@vitapur_home.sk, 9:22). Screenshoty s odoslanou bublinou ako dôkaz.
- **Email (13, Gmail drafty — API nevie odoslať priamo):** Bloom Robbins, Doktorka Sandra,
  StretchFit, Tomas Arsov (batch 15); Vera Italy, Agátin svet, Gardj, Šperky od Petry, Amarost,
  Historické darčeky, Muzza, Profitent, KKTKY (batch 16). Čakajú na Markovo kliknutie Send.

⚠️ **InaEssentials.SK odpovedala do 1 minúty** — po preskúmaní ide o **automatizovaného bota**
(formálny tón, ponuka konkrétnych produktov Hydrolina/RoutINA™, presmerovanie technickej otázky na
tím), nesedí s neformálnym IG hlasom skutočnej osoby. Nepočítané ako kvalifikovaná ľudská reakcia
v dashboarde, zaznamenané ako dátový bod.

**Založené:** nič nové (rozšírenie existujúcich [[outreach-batch-15]] a [[outreach-batch-16]]).
**Aktualizované:** [[outreach-batch-15]], [[outreach-batch-16]] (odoslané správy, stav), 
[[cold-outreach-pipeline]] (17 riadkov), [[dashboard]] (banner, §1 čísla, kanál/trh/dávka tabuľky),
`index.md`.

✅ **Follow-up text schválený, Marko ручne odošle z marek@cart.design:**

> Ahoj Jakub,
>
> vravel si, že koncom júla budeš pripravený pustiť sa do toho, tak sa ozývam podľa dohody.
>
> Poznámky k Noskám sú stále na https://nosky.cart.design/.
>
> Hodí sa ti tento týždeň 15 minút na call, alebo to ešte nie je ten čas?
>
> Marek

**Poznatok:** zrkadlenie formulácií leadu nesmie prekročiť jazykovú hranicu — píšeme po slovensky aj
českému leadovi.

## [2026-08-10] scrape | ICP v2 — druhá vlna širokého záberu (outreach-batch-17) — 6/33 kvalifikovaných

Marko: „naprieč čo najviac produktovými kategóriami bez obmedzenia na jednu niku, ber len značky
s aktívne bežiacou reklamou v FB/IG Ad Library". Rovnaké zadanie ako batch 16, preto dvojfázovo:
(1) doverenie 15 z 18 kandidátov ponechaných v rezerve z [[outreach-batch-16]] → **0 kvalifikovaných**
(takmer výhradne reselleri/retail reťazce s kamennými predajňami — hodinkovna.cz, mobilonline.sk,
velosvet.sk a i.); (2) čerstvý discovery v nových kategóriách (sviečky, dojčenské potreby, krmivo pre
psy, darčekové boxy, jóga, kozmetika, plánovače...) → 27 kandidátov po voľnej kvalifikácii → **6
kvalifikovaných**: Roses Kingdom, Purity Vision, Worshipster, Aura Decor, PsiBufet, Ariaz Baby.
2 zamietnutí po IG overení (svieckyslaskou.sk — spiaci účet napriek najsilnejšej bolesti v dávke;
cricksydog.sk — 8-krajinová operácia, príliš veľká). Nový poznatok: outdoor/bicykle/hodinky/nábytok/
obuv treba pri širokom zábere preskočiť, sú takmer výhradne resellery. Stránky: [[outreach-batch-17]],
raw `ad-library-broad-batch17-verified-2026-08-10.md`. Aktualizované: [[dashboard]],
[[cold-outreach-pipeline]], `index.md`. Žiadne správy napísané, žiadne odoslané — čaká na `/send`.

## [2026-08-10] send | outreach-batch-17 — 6/6 napísaných, 5 IG DM doručených naživo, 6 emailov ako Gmail drafty

Marko: „posli mi to aj cez ig + mail" (override pauzy). Hooky re-verifikované v deň odoslania
(Roses Kingdom: 4× meranie, medián 1,60s; ostatné scripty stabilné), žiadny nezomrel. Marko prvýkrát
explicitne povolil odoslanie **oboma kanálmi tomu istému leadu v ten istý deň** — bežne zakázané
kvôli riziku pôsobiť ako bot. Sekundárny kanál v každej dvojici priznáva duplicitu („písal som aj
mailom, neviem či prešiel"). 5 z 6 leadov dostalo IG DM aj email (Ariaz Baby len email, žiadny IG).
Pri prvom pokuse (Roses Kingdom) sa správa omylom odoslala dvakrát — screenshot bol zachytený skôr,
než sa UI prekreslilo, oprava cez Unsend. Nový poznatok #19 v [[insights]] (over textbox pred Send,
thread po Send). Zvyšné 4 IG DM prešli bez chyby. Aktualizované: [[outreach-batch-17]] (plné znenia
správ), [[cold-outreach-pipeline]], [[dashboard]] (§1 čísla, kanál, trh, dávka), [[insights]]
(poznatok #19), `index.md`. **6 Gmail draftov čaká na Markovo kliknutie Send.**

## [2026-08-10] asset | Discovery dotazník pre Maťa (B2B zdravotnícke pomôcky)

Vytvorený `wiki/assets/Dotaznik-B2B-system-Mato.csv` — 78 otázok v 15 oblastiach (firma, aktuálny
stav, B2B cenníky, proces objednávky, sklad vrátane šarží/expirácií/FEFO/konsignácie, regulácia a
dohľadateľnosť podľa MDR/UDI/ŠÚKL, nákup, fakturácia, doprava, role, reporting, migrácia dát,
must/nice priority, čas a rozpočet). Nový adresár `wiki/assets/` pre súbory určené klientom.
Aktualizovaný `index.md`. Dotazník zatiaľ neodoslaný a nevyplnený; Maťo nemá zatiaľ wiki stránku.

## [2026-08-10] asset | Dotazník pre Maťa aj v markdowne

Pridaný `wiki/assets/Dotaznik-B2B-system-Mato.md` — rovnakých 78 otázok ako CSV verzia, len na
vypĺňanie v texte (úvodný odsek pre Maťa, pri každej otázke `Odpoveď:` a `Priorita:`). Bez
frontmatteru zámerne: je to súbor pre klienta, nie wiki stránka. Aktualizovaný `index.md`.

## [2026-08-10] asset | Presun dotazníkov do ~/wiki/assets

Oba súbory (CSV a MD verzia) presunuté z `second-brain/wiki/assets/` do `~/wiki/assets/` — tam
patria, nie do second-brain. Adresár `second-brain/wiki/assets/` odstránený. Aktualizovaný
`second-brain/index.md` (časť Assets odobraná).

## [2026-08-10] ingest | PsiBufet email — odpoveď bota, draft reakcie

Email na kontakt@psibufet.com dostal odpoveď z bark@butternutbox.com — Intercom AI Agent "Fin",
nie človek. Pýta sa na zariadenie/prehliadač/meradlo za 121 scriptami. Pripravená a schválená
formálna reakcia (vykanie), uložená ako Gmail draft v tom istom vlákne, čaká na Markovo Send.
Aktualizované: outreach-batch-17, cold-outreach-pipeline, dashboard.

✅ Odpoveď poslana 10.8.2026 — vysvetľuje curl meranie, HTML zdroják, nezávislé od zariadenia.

## [2026-08-11] scrape | craft makers + nože batch-18 — 51/98 kvalifikovaných, 51 napísaných správ

Marko uvoľnil kvalifikačnú latku pre objem („nemusí byť každý totálne kvalifikovaný, len potrebujem
50 leadom poslať email/IG správu dnes"). Discovery cez 8 Firecrawl dotazov (nože/šperky/koža/keramika,
SK/CZ/EN) → 98 kandidátov preverených čisto cez `curl` (**bez Kimi WebBridge** — followers a dátum
posledného postu `neoverené` pri všetkých 51) → 51 kvalifikovaných (15 SK, 20 CZ, 16 EN; 37 email,
14 IG DM), 47 vylúčených. Prah znížený z 80 na 25+ `<script>` tagov pre kandidátov bez inej bolesti.
Najsilnejšie nálezy: river.sk neplatný SSL certifikát, BountyBoho.sk 154 scriptov. 9 leadov sú nožiari
⚠️HIGH-RISK platby (kapacita neoverená). Nové súbory: `raw/cart.design/cold-outreach/craft-knives-batch18-verified-2026-08-11.md`,
`wiki/outreach/batches/outreach-batch-18.md`. Aktualizované: dashboard, index.md. Žiadne správy
odoslané — čaká na Markovo schválenie a `/send`.

## [2026-08-11] send | batch-18 re-verifikácia hookov — 46/51 prežilo, 5 mŕtvych

Krok 1 `/send batch-18`, popoludní, ten istý deň ako pôvodná kvalifikácia. Metóda: `curl` 4× na
lead (medián, poznatok #11 — nie 1× ako pri pôvodnej dávke), počet `<script>` tagov cez Python
`re.S`, `curl -v` pre river.sk SSL. **46/51 hookov prežilo** (väčšina script-count hookov sedí na
presne rovnaké číslo ako pri kvalifikácii; river.sk SSL mismatch reprodukovaný identickou chybou).

**5 mŕtvych** (response-time hooky, čas klesol pod prah 1,5s): Nasha Keramika (2,19s → medián
1,45s), MHKNIVES (2,20s → 1,20s), Keramika Patrik Daič (1,76s → 0,14s — pôvodné 1× meranie bolo
studený štart, presne past z poznatku #11), Tomáš Linger (1,79s → 0,37s), Moss Bags (1,90s →
0,52s). Žiadny nahradený vymysleným hookom; 3 z 5 majú NOVÝ script-count hook nájdený počas
re-checku (Nasha 53, Tomáš Linger 26 slabý, Moss Bags 63), zapísaný len ako kandidát na prepis
správy, nie tichým doplnením. 4 hooky s výrazne zmeneným číslom, ale prahom stále prekonaným:
Keramická dílna Petra Raisová (3,50s→1,71s), MontMat (1,41s→medián ~12,9s, zhoršené), Kovářství
Čurda (1/4→2/4 timeout, zhoršené), river.sk (nezmenené). Batch-18 stránka: Status stĺpec doplnený
o ✅/❌ marker pri všetkých 51 riadkoch, mŕtve hooky ponechané viditeľné (nie zmazané), nová sekcia
„Re-verifikácia hookov v deň odoslania". Dashboard/pipeline/index zatiaľ nedotknuté — čakajú na
krok doručenia.

## [2026-08-11] send | batch-18 — 34 email drafty + 3 IG doručené naživo, 9 IG zastavené (throttle)

`/send batch-18` doručenie: **34 Gmail drafty vytvorené** (SK 10, CZ 17, EN 7 — čakajú na Markovo
kliknutie Send). **3 IG DM odoslané naživo cez Kimi WebBridge** (Lady Bead Jewelry, AP Jewellery,
Janelit.sk — SK), každý overený screenshotom sent-bubliny. **Lady Bead Jewelry odpovedala do 5 minút**
(„mala som človeka ktorý mi stránku robil..."), treba napísať fázu 2. Pri 4. IG DM (MOOYYY, CZ)
vyhľadávanie v IG composeri zaseklo na 30+ sekúnd po sérii rýchlych searchov — možný throttle signál;
žiadny duplikát ani chybné odoslanie, len sa nedalo pokračovať. Marko rozhodol zastaviť IG na dnes
namiesto tlačenia cez throttle. **9 IG DM (1 CZ + 8 EN) zostáva nedoslaných**, zapísané ako pripravené
v batch-18. Aktualizované: `outreach-batch-18.md` (status stĺpec všetkých 46 riadkov), `dashboard.md`
(§1 čísla, batch tabuľka, nový dated bullet), `cold-outreach-pipeline.md` (3 nové riadky, Lady Bead
Jewelry ako reagovala).
