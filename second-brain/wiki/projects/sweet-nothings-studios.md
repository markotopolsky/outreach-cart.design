---
type: project
status: active
created: 2026-07-16
updated: 2026-07-16
aliases: [Sweet Nothings Studios, sweetnothingsstudios]
tags: [cart-design, cold-outreach, lead, en]
---

# Sweet Nothings Studios — lead (EN, SSL diagnóza odoslaná)

US makerka (@sweetnothingsstudios, 25.4K IG) — soft soldered šperky a vitráže, predaj cez Big Cartel „web drop" formát. Tech-first otvárač z [[outreach-batch-2]] (#2). **Reagovala 15.7.: „Shop is up and running, perhaps try refreshing your browser!"** — ale overenie 16.7. našlo skutočný, presne pomenovateľný problém.

## Profil

- **Kto:** solo makerka (US), predaj cez drops („web drop 5PM CT")
- **Publikum:** 25.4K IG (Tier 2)
- **Web:** Big Cartel. **Technický nález (overené 16.7., openssl/curl):**
  - `https://sweetnothingsstudios.com` (bez www) → **TLS handshake zlyhá** (alert internal error, server nemá certifikát pre apex doménu)
  - `https://www.sweetnothingsstudios.com` → funguje; certifikát kryje **len** `www.sweetnothingsstudios.com`
  - Dôsledok: kto zadá doménu bez www v prehliadači, ktorý vynucuje HTTPS, dostane chybu — presne to trafil otvárač 15.7. Jej to „funguje", lebo používa www/bookmark.

## Stav konverzácie (k 2026-07-16)

1. **Otvárač odoslaný 15.7. 12:48** (tech-first: „site's not loading — is it down for you too?").
2. **Reagovala 15.7. 15:54:** obchod beží, skús refreshnúť. Hook z jej pohľadu vyvrátený.
3. **Odpoveď s SSL diagnózou odoslaná 16.7.** — presný nález (apex bez certifikátu, www funguje) + jemné priznanie „staviam obchody pre tvorcov". Čaká sa na odpoveď.

## Komunikácia (IG DM, plný prepis)

Prekopírované Markom z IG inboxu 2026-07-16 (`ig-status167`).

**Marko (otvárač, 15.7. 12:48):**
> Hey! The "web drop 5PM CT" format is such a smart way to create urgency. Tried checking out sweetnothingsstudios.com just now though and it's not loading at all. Is the site down for you too, or is it just me?

**Sweet Nothings Studios (15.7. 15:54):**
> Hi! Shop is up and running, perhaps try refreshing your browser!

**Marko (SSL diagnóza, 16.7.):**
> That's the funny part — it *is* up, but only the www version. It bugged me so I dug a little: sweetnothingsstudios.com without the "www" throws a security error (the certificate only covers www.). So anyone typing the bare domain gets a scary warning instead of your shop. Should be a quick fix on Big Cartel's side — worth pinging their support.
>
> (I build stores for makers, so I notice this stuff compulsively 😅)

## Ďalší krok

- [ ] Čaká sa na jej odpoveď na SSL diagnózu (odoslané 16.7.). Najsilnejšia záchrana hooku z celej dávky.

## Zdroje

- `raw/cart.design/cold-outreach/ig-status167.md` — IG inbox prepis (16.7.)
- Verifikácia SSL: curl + openssl 2026-07-16 (apex bez certifikátu; www cert kryje len www)
- [[outreach-batch-2]] (#2 — otvárač)
- [[cold-outreach-pipeline]]
