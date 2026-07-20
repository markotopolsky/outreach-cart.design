
## [2026-07-20] ingest | Chuck Richards — email fáza 3 odoslaný
Marko odoslal email na sales@chuckrichardsknives.com (predmet „The FreeBird — from Instagram"). Jadro:
potvrdiť Chuckovu námietku („nikdo mi nepovie, že som vypredaný") a obrátiť ju — zákazník, ktorý
odíde, sa neozve, takže absencia sťažností nie je dôkaz, že problém neexistuje. Marko sám ako osobný
dôkaz (ani on to nepovedal, kým sa nepozrel profesionálne). CTA = krátky walkthrough zadarmo, bez
záväzku. Aktualizovaná [[chuck-richards-knives]] (Ďalší krok: čaká sa na odpoveď).

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
