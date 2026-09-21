# Fishbrain — onboarding & paywall rebuild

A clickable prototype of a rebuilt Fishbrain onboarding flow and paywall, plus a
second-chance offer paywall on close. Built as a prospect-facing artefact.

## How to view it

There is no hosted link. GitHub renders `index.html` as source, not as a page, and
GitHub Pages needs a public repo on a free plan — so while this repo is private the
only way to open it is locally:

```bash
git clone https://github.com/bterzic123/fishbrain-flow-rebuild.git
open fishbrain-flow-rebuild/index.html
```

No build step, no dependencies, no network calls — one self-contained file, so it
works offline and straight off disk.

**To put it behind a URL** (e.g. to send a prospect something that outlives a
screen-share), make the repo public and turn on Pages:

```bash
gh repo edit bterzic123/fishbrain-flow-rebuild --visibility public --accept-visibility-change-consequences
gh api -X POST repos/bterzic123/fishbrain-flow-rebuild/pages -f 'source[branch]=main' -f 'source[path]=/'
```

That publishes to `https://bterzic123.github.io/fishbrain-flow-rebuild/` — and makes
the teardown, the pricing analysis and the prospect's name world-readable. Deliberate
call, not a convenience.

## What's in it

**Tab 1 — Prototype.** An iPhone frame with all 11 screens clickable and real
transitions. A side panel gives, per screen: the rationale, what was kept from the
live app, what it becomes in a shipping flow, and the expected impact range. Jump
chips under the phone drop you on any stage with answers pre-filled, including two
variants (saltwater angler, no species selected) and the offer paywall.

**Tab 2 — Before / after.** The shipping sequence beside the rebuilt one, each step
tagged KEPT / MERGED / CUT / MOVED, the ranked change table, the deliberate
omissions, the open asks, and a source table for every number on the screens.

## Design system

Extracted from recordings of the live app before anything was rebuilt — navy
`#13314C`, CTA green `#22C97A`, headline-highlight green `#3EE690`, savings-badge
magenta `#F5246B`. The distinctive controls are reused unchanged: the inverted
option rows, the circle-masked map picker with its scale bar and locate pill, the
three-column species grid, the segmented tab, the plan cards with the overlapping
badge, and the trial toggle row. Only the sequence changed.

## Grounding

Every price, rating, quote and partnership is Fishbrain's own published material —
US App Store listing, fishbrain.com and fishbrain.com/pro. Tab 2 carries the full
source table, including one claim that was found but deliberately **not** used
because it could not be verified first-hand.

## Known placeholders

The hero photography and the species illustrations are drawn stand-ins. The
controls and layout are the app's; the art is not.
