# Second Brain — Schema

This vault is Marko's second brain: an LLM-maintained wiki built on top of raw source notes. The LLM (Claude) writes and maintains the wiki; Marko curates sources, asks questions, and reads the results in Obsidian.

## Three layers

1. **Raw sources** — everything under `raw/`: `raw/cart.design/`, `raw/other/`. These are Marko's notes, briefs, feedback, transcripts, AI outputs. **Immutable for the LLM: read, never edit or delete.** New material lands here first. (Note: `dh/` at the vault root holds merge.build's Pevné zuby notes — deliberately **outside** the LLM wiki; do not ingest it.)
2. **The wiki** — `wiki/`. Entirely LLM-written and LLM-maintained: entity pages, project pages, topic pages, syntheses. Marko reads it; the LLM keeps it current.
3. **The schema** — this file. Conventions and workflows. Marko and the LLM co-evolve it as the vault grows.

## Layout

```
second-brain/
├── CLAUDE.md          ← this schema
├── index.md           ← catalog of the whole vault (wiki + raw), updated on every change
├── log.md             ← append-only journal of ingests/queries/lints
├── wiki/              ← LLM wiki, cart.design only
│   ├── projects/      ← real deals in an advanced stage (e.g. fitnessmenu)
│   ├── people/        ← one page per person
│   ├── outreach/      ← live cold-outreach pipeline: pipeline, batches, prospects
│   ├── feedback/      ← results & learnings from the pipeline (daily recaps, insights)
│   └── topics/        ← concepts, analyses, references, filed answers
├── raw/
│   ├── cart.design/   ← raw: cart.design client work (e-shops)
│   └── other/         ← raw: unsorted notes
└── dh/                ← merge.build Pevné zuby notes, OUTSIDE the wiki (not ingested)
```

## Conventions

- **Language:** wiki page content in **Slovak** (the language of the sources and of Marko's notes). Frontmatter keys, filenames, and this schema in English.
- **Filenames:** ASCII kebab-case (`katarina-silna.md`). Put the proper name (with diacritics) in `aliases` so Obsidian links resolve nicely.
- **Links:** Obsidian wikilinks `[[boris]]`, `[[fitnessmenu|FitnessMenu]]`. Link liberally — the graph view is a feature. For raw files with ambiguous names (there are several `Raw.md`), use path wikilinks: `[[cart.design/Fitnessmenu/FitnessMenu-demo-feedback/Feedback na demo-raw-v1|demo feedback]]`.
- **Frontmatter** on every wiki page:

  ```yaml
  ---
  type: project | person | organization | topic | answer
  status: active | waiting | done      # projects & outreach
  created: YYYY-MM-DD
  updated: YYYY-MM-DD
  aliases: []
  tags: []
  ---
  ```

- **Grounding:** every claim in the wiki traces to a source. Each page ends with a `## Zdroje` section listing the raw files it draws from. Mark uncertainty explicitly (`Markov subjektívny pocit`, `neoverené`). When a new source contradicts an existing claim, don't silently overwrite — note the contradiction with dates.
- **Dates matter:** this vault tracks live deals. Timestamp facts (`k 2026-07-06`) so stale claims are detectable.
- **Client communication:** every lead/project page with a live conversation carries a `## Komunikácia` section — a full verbatim transcript (date + who + exact text), appended as new messages happen. Transcripts can be pulled from Instagram DMs via Kimi WebBridge (browser) or pasted by Marko; note the retrieval date and method. The summary lives in `## Stav konverzácie`; the transcript is the ground truth.

## Workflows

### Ingest
When Marko drops a new source (or says "process X"):
1. Read the source fully (view referenced images separately if relevant).
2. Discuss key takeaways with Marko if he's active; otherwise proceed.
3. Update every wiki page the source touches (people, projects, outreach, feedback, topics). Create new pages for entities that earned one — a prospect/lead goes in `outreach/`; it graduates to `projects/` once it's a real advanced-stage deal.
4. Update `index.md`; append to `log.md`.

### Query
When Marko asks a question: read `index.md` first, drill into relevant wiki pages, then raw sources if needed. Answer with citations. **If the answer is durable (comparison, analysis, decision memo), file it into `wiki/topics/` as `type: answer` so it compounds** — ask Marko or use judgment.

### Lint
Periodically (or on request) health-check the vault: contradictions, stale claims on active deals, orphan pages, entities mentioned but missing a page, empty placeholder files in raw, missing cross-references. Report findings; fix what's approved. Log the pass.

## Log format

Append-only entries in `log.md`, newest last:

```
## [YYYY-MM-DD] ingest | Source title
## [YYYY-MM-DD] query | Question asked
## [YYYY-MM-DD] lint | Scope
```

One or two lines under each header: what changed, which pages were touched. `grep "^## \[" log.md | tail -5` gives the recent history.

## Hard rules

- Never edit or delete anything under `raw/`.
- Never delete a wiki page without asking; superseded content gets a note, not silent removal.
- Every wiki edit updates `updated:` in frontmatter, `index.md`, and `log.md`.
- Business notes here are sensitive (live negotiations, psychological profiles). Content stays in this vault — never publish or send it anywhere external without explicit instruction.
