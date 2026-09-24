# knet.network — the gate

This repository is the page served at **https://knet.network**. It is a list of doors: one card per project, each card a link out. The page holds no content of its own, and it belongs to no project. It is not part of FRACTAL or of any FRACTAL instance; FRACTAL is one card among the doors.

Anyone — a person, Codex, Claude, any other agent — can add, change, or remove a card by following this file. Nothing else needs to be read.

## The one file

`index.html` is the whole site. Styles are inline; there is no build step, no framework, no dependency. GitHub Pages serves the `main` branch as-is; `CNAME` holds the domain.

## The card

A card is this block, copied verbatim and filled in:

```html
  <a class="card" href="https://…">
    <p class="card-name">Name <span class="go">&rarr;</span></p>
    <p class="card-info">One sentence: what it is and why it has a door here.</p>
  </a>
```

Three fields, one rule each:

- **Name** — the project's own name, as it calls itself. No tagline in the name.
- **Link** — an absolute URL to the project's home. A card never links to a page inside this repository; if a project needs a page, it gets its own home elsewhere and the card points there.
- **Sentence** — one sentence, at most about 35 words, in plain words. It says what the thing is. It does not praise it.

Cards sit inside `<main>`, one after another. The order is the owner's choice; when adding a card, put it last unless told otherwise. No badges, no icons, no dates, no counters — if a need for one is ever observed, add it then, not before.

## Adding a card, step by step

1. Edit `index.html`: paste the block below the last card, fill in the three fields.
2. Open the file in a browser, in light and in dark mode (the page follows the system scheme). The new card must look exactly like its neighbours.
3. Check the link resolves, for example `curl -sI <link> | head -1` must answer `200`.
4. Commit with the author being whoever wrote the bytes, message `[GATE] Add the card — <Name>`. Push to `main`.
5. The page updates within about ten minutes (GitHub's cache). Reload with the cache bypassed to confirm.

Removing a card is the same in reverse. Changing the page's design is a separate act: it changes every card at once and is the owner's decision, never a side effect of adding one.

## The look, if another page wants to match it

The page is system-font, hairline cards, no colour. The tokens, both schemes, are the `:root` variables at the top of `index.html`: `--bg`, `--ink`, `--muted`, `--faint`, `--hairline`, `--hairline-soft`. A project page that wants the same feel copies those six values; nothing here is meant to be linked from elsewhere.

## Two standing notes

- **An address, not a brand.** The page shows the domain as plain text and carries no logo or wordmark. The names KNET and K-NET are obstructed as trademarks in Germany and the EU (clearance findings of 2026-08-18); until a clearance says otherwise, no page under this address presents them as a brand.
- **The footer's two links** — the contact address and the legal notice — currently point at FRACTAL's. They work while FRACTAL's site is served. When the next card lands, or when FRACTAL's site goes away, this repository gets its own `legal.html` and its own contact line; that is the owner's act, and this note is its reminder.

## History

- 2026-08-18 — opened as the umbrella's address, FRACTAL the first card (built in FRACTAL's sessions).
- 2026-08-26 — the second card, The Shell.
- 2026-09-24 — made autonomous: the Shell card withdrawn (the Shell stays reachable inside FRACTAL's site), this file written, the page's description generalised. From here on the gate is edited outside FRACTAL, by anyone following this file.
