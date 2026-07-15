# SK Instagram leady — bez e-shopu (Firecrawl + Kimi WebBridge, 2026-07-15)

Metóda: Firecrawl `site:instagram.com` search na kľúčové slová (handmade, remeslo, sviečky, šperky, kozmetika + slovensko/rucne robene) → shortlist profilov → Kimi WebBridge (prihlásený browser) overil bio/link-in-bio na prítomnosť vlastného e-shopu.

Firecrawl hashtag crawling (#remeslo, #rucnavyroba, #remeselnik) bol skúšaný najprv, ale hashtagy vracajú prevažne nerelevantné príspevky (~20-30% relevancia) a vyžadujú si veľa manuálnych override — site:instagram.com search v Firecrawli bol rýchlejší spôsob objavovania kandidátov, WebBridge len na verifikáciu.

## Kvalifikovaní leadi (bez vlastného e-shopu)

| Username | Profil | Niche | Followers | Stav | Poznámka |
|---|---|---|---|---|---|
| by_alisha.sk | instagram.com/by_alisha.sk | šperky (handmade) | 25.3K | **žiadny e-shop** | Link v bio = tally.so objednávkový formulár, nie e-shop. "objednávky mi píšte do správy" — najsilnejší lead z dôvodu veľkosti publika |
| darcekove_kytice | instagram.com/darcekove_kytice | darčekové kytice (bonbóny/saténové ruže) | 2,133 | **žiadny e-shop** | Link v bio vedie na Facebook profil, nie e-shop. Aktívne "SKLADOM" príspevky — predáva čisto cez sociálne siete |
| saint.jewellry | instagram.com/saint.jewellry | šperky (handmade) | 1,424 | **žiadny vlastný e-shop** | Link vedie na sashe.sk (marketplace agregátor), nie vlastná doména. "Platba len prevodom", objednávka cez správu |
| sperkyrichterovahandmade | instagram.com/sperkyrichterovahandmade | šperky (Swarovski, autorská tvorba) | 439 | **žiadny e-shop** | V bio len fyzická adresa ateliéru (Martin), žiadny web link |
| mc_remeselnik | instagram.com/mc_remeselnik | remeselné služby (elektrika, kamerové systémy) | 367 | **žiadny e-shop/web** | Iná kategória (služby, nie produkty) — žiadny web vôbec |
| badynco | instagram.com/badynco | prírodná kozmetika (handmade) | 262 | **žiadny e-shop** | Bio: "Info/order DM" — žiadny odkaz na web |
| handmadebyluvela | instagram.com/handmadebyluvela | autorské šperky (beadweaving) | 47 | **žiadny e-shop** | Jediný externý odkaz v bio je Threads profil, žiadny e-shop |

## Overené, ale MAJÚ vlastný e-shop (vylúčené z targetingu)

| Username | Niche | Followers | E-shop |
|---|---|---|---|
| leora_sk | sójové sviečky | 4,875 | www.leora.sk |
| svieckyprevsetkych | sviečky | 78 | www.svieckyprevsetkych.sk |
| murka_hm | náušnice z polyméru | 5,415 | www.murkashop.sk |
| rozkvitnuta.sviecky | sójové sviečky | 641 | www.rozkvitnuta.sk |
| eulasercreations | laser engraving | 24.5K | laser-creations.eu (etablovaná značka) |

## Ďalšie kandidáti nájdení, neoverené (Firecrawl only, bio nekontrolované)

Z Firecrawl search výsledkov, čakajú na WebBridge verifikáciu: `remeselno`, `slovak_handmade_` (pôsobí ako komunitný/kurátorský účet, pravdepodobne nie individuálny predajca), `prirodno.sk`, `caltha.sk` (pravdepodobne značky s vlastným webom — "prirodno.sk", "caltha.sk" ako username naznačuje vlastnú doménu).

## Zdroje
- Firecrawl search: `.firecrawl/ig1.json` – `.firecrawl/ig4.json` (site:instagram.com + kľúčové slová)
- Kimi WebBridge: manuálna verifikácia bio/link-in-bio cez prihlásený Instagram účet (session `ig-no-eshop`)
- Predchádzajúci pokus: `firecrawl-test-batch-2026-07-15.csv` (Slovak e-shopy cez Firecrawl web search — ukázalo sa, že tento kanál väčšinou nájde firmy, ktoré e-shop UŽ MAJÚ, keďže Google indexuje najmä existujúce weby)
