# Outreach Systém — Tvorba Eshopov

## Ako to celé funguje

```
[Obsidian poznámka o klientovi] → [Vlož do AI spolu s Master Promptom] → [Hotová správa]
```

Tvoja úloha je robiť dobrý research a zapisovať si ho štruktúrovane. AI potom z tých dát vyrobí personalizovanú správu. Čím lepšie dáta, tým lepší výstup.

---

## Krok 1: Research & zápis

Pre každého potenciálneho klienta vytvor novú poznámku v Obsidiane podľa šablóny `Prospect_Template.md`. Vyplň čo najviac polí. Minimum, čo potrebuješ:

- **Meno + firma** (komu píšeš)
- **Kanál** (kde mu píšeš)
- **Jazyk + tón** (ako mu píšeš)
- **Čo si si všimol** (aspoň 1 konkrétny pain point)
- **Osobný háčik** (aspoň 1 vec, aby správa nebola generická)

---

## Krok 2: Master Prompt

Skopíruj celý obsah svojej Obsidian poznámky a vlož ho do AI spolu s týmto promptom:

---

### PROMPT — začiatok (skopíruj odtiaľto)

```
Si expert na cold outreach pre freelancera / agentúru, ktorá sa špecializuje na tvorbu eshopov. Tvoja úloha je napísať jednu správu na oslovenie potenciálneho klienta.

## Moje služby
- Tvorba eshopov na mieru (Shopify / WooCommerce / custom riešenia)
- Redizajn a modernizácia existujúcich eshopov
- Optimalizácia konverzií, rýchlosti a mobilnej verzie
- Napojenie na platobné brány, dopravcov, ERP systémy

## Pravidlá pre správu

### Štruktúra:
1. OTVOR niečím o NICH — nie o sebe. Použi osobný háčik alebo konkrétny postreh z ich online prítomnosti. Nikdy nezačínaj "Dobrý deň, volám sa..." alebo "Ozvám sa vám, pretože..."
2. POMENUJ problém/príležitosť — konkrétne, čo im chýba alebo čo by mohlo byť lepšie. Použi info z poznámky. Buď špecifický, nie vágny.
3. NAVRHNI riešenie — krátko, 1-2 vety. Čo by sa dalo spraviť a aký by to malo dopad. Neponúkaj celý zoznam služieb.
4. UKONČI mäkkým CTA — žiadne "kúpte si." Skôr: "Stálo by vám za to sa o tom porozprávať?" / "Dalo by sa na 15 minút zavolať?" / "Čo hovoríte?"

### Tón a štýl:
- Prispôsob tón podľa poľa `ton` v poznámke (profesionálny / priateľský / priamy)
- Píš v jazyku podľa poľa `jazyk` (SK / CZ / EN)
- Buď autentický, nie salesy. Píš ako človek, nie ako šablóna.
- Žiadne klišé typu "vo svete digitalizácie...", "v dnešnej dobe...", "rád by som vám predstavil..."
- Nepoužívaj superlatívy o sebe ("najlepší", "top", "profesionálny tím")

### Prispôsob dĺžku kanálu:
- **Email:** 80-150 slov, môže mať predmet (subject line)
- **LinkedIn:** 50-100 slov, konverzačný tón
- **Instagram/Facebook DM:** 30-70 slov, neformálne, krátke
- **WhatsApp/SMS:** 30-50 slov, veľmi stručné a priame

### Čomu sa vyhni:
- Generické frázy, ktoré by sedeli na kohokoľvek
- Dlhé predstavovanie sa
- Zoznam všetkých služieb
- Agresívny predaj alebo urgentnosť ("len tento týždeň", "zľava")
- Prehnané sľuby ("zdvojnásobíme vám tržby")

## Dáta o klientovi
[SEM VLOŽ OBSAH SVOJEJ OBSIDIAN POZNÁMKY]

## Výstup
Napíš 2 varianty správy:
- **Variant A** — tvoj hlavný tip, čo by podľa teba fungovalo najlepšie
- **Variant B** — alternatívny prístup (iný uhol pohľadu alebo iný háčik)

Pri každej variante napíš 1 vetu prečo si zvolil daný prístup.
```

### PROMPT — koniec

---

## Krok 3: Follow-up prompt

Ak klient neodpovedal do 3-5 dní, použi tento prompt:

```
Napíš follow-up správu pre klienta, ktorému som už písal. Tu je:

1. Pôvodná správa, ktorú som poslal:
[VLOŽ PÔVODNÚ SPRÁVU]

2. Poznámka o klientovi:
[VLOŽ OBSAH OBSIDIAN POZNÁMKY]

Pravidlá pre follow-up:
- Neopakuj pôvodnú správu
- Pridaj novú hodnotu — nový postreh, tip, alebo relevantný príklad
- Buď kratší ako pôvodná správa
- Nebuď pasívno-agresívny ("len sa chcem uistiť, že ste dostali môj email")
- Zachovaj rovnaký tón a kanál
- Mäkký CTA — daj im ľahký spôsob ako odpovedať
```

---

## Tipy pre Obsidian organizáciu

### Odporúčaná štruktúra priečinkov:
```
📁 Outreach/
  📁 Nový/           ← prospects na oslovenie
  📁 Oslovený/       ← čaká sa na odpoveď
  📁 V kontakte/     ← prebiehajúca komunikácia
  📁 Klient/         ← uzavretý deal
  📁 Archív/         ← nezáujem / neaktuálne
```

### Užitočné Obsidian tagy:
```
#kanal/email  #kanal/linkedin  #kanal/instagram  #kanal/whatsapp
#typ/lokalny  #typ/online  #typ/redizajn  #typ/novy
#priorita/vysoka  #priorita/stredna  #priorita/nizka
#jazyk/sk  #jazyk/cz  #jazyk/en
```

### Dataview query (ak používaš Dataview plugin):
```dataview
TABLE meno, firma, kanal, status, datum_oslovenia
FROM "Outreach"
WHERE status = "novy"
SORT datum_oslovenia ASC
```

---

## Príklad vyplnenej poznámky

```markdown
---
meno: "Jana Kováčová"
firma: "Domáce Sviečky JK"
pozicia: "Majiteľka"
kanal: "instagram"
jazyk: "SK"
ton: "priatelsky"
typ_klienta: "online_znacka"
status: "novy"
datum_oslovenia: ""
---

## Online prítomnosť
- **Web:** nemá vlastný web
- **Sociálne siete:** Instagram @domacesvieckyjk, 3.2k followerov, aktívna 3-4x týždenne
- **Existujúci eshop:** Nie, predáva cez Instagram DM a občas cez Sashe
- **Počet followerov / veľkosť:** malý biznis, 1 osoba

## Čo som si všimol
- Predáva výlučne cez DM — musí manuálne odpisovať každému zákazníkovi
- Na stories často píše "vypredané" — pravdepodobne nestíha dopyt
- Nemá žiadny katalóg ani cenník online
- Fotky produktov sú kvalitné — vizuál by sa dal rovno použiť na eshop

## Osobný háčik
- Minulý týždeň postla story, že nestíha odpisovať na všetky správy
- Robí limitované kolekcie podľa sezóny — jesenná kolekcia ide von o mesiac

## Konkurencia
- candle-factory.sk — slovenský eshop so sviečkami, pekný dizajn, plne funkčný
- sojasviecky.sk — jednoduchý ale efektívny eshop

## Prečo práve ja
- Jednoduchý eshop s napojením na Instagram by jej ušetril hodiny denne
- Mohla by predávať aj keď spí — automatické objednávky
- Limitované kolekcie = ideálne pre countdown / "sold out" funkciu

## Poznámky
- Nájdená cez Instagram explore, hashtagy #handmadesviecky
- Pôsobí priateľsky a neformálne v stories
```
