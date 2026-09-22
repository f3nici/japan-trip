# Japan trip, February 2027

A single-page trip plan: flights, budget, day-by-day itinerary and a pre-departure checklist.

**Live site:** https://f3nici.github.io/japan-trip/

## The trip

Perth to Tokyo Narita and back on Cathay Pacific, **Mon 1 Feb to Fri 19 Feb 2027**, 18 nights,
Narita both ways.

Tokyo-based: one twin room in Shinjuku for the whole stay, with days out to Daikoku, Ebisu
Circuit, Yokohama and Fuji-Q Highland.

## Do not publish personal details

This page is served publicly over GitHub Pages. Keep booking references, ticket numbers,
passenger names, passport details and card numbers out of it. A booking reference plus a
surname is enough for a stranger to view, change or cancel a flight on most airline sites.

Flight numbers, times, fares and baggage allowances are fine; they are not personally
identifying.

## Editing

The whole site is one self-contained file: [`index.html`](index.html). No build step, no
dependencies. Open it in a browser to preview changes locally.

A few things to know before changing it:

- **Prices are data, not text.** Inline costs use `<span data-yen="3250">` (or a range,
  `data-yen="500-1500"`, and `data-approx` for a `~`). Budget rows use
  `data-kind="base|extra"` plus `data-yen` or `data-aud`. The script totals them and
  converts to AUD, so edit the attribute and leave the rendering alone.
- **Budget totals are derived.** `Base trip`, `Everything` and `Left for shopping` are all
  computed. The A$14,000 budget cap is hardcoded in the script.
- **The budget table restyles itself below 640px** into stacked cards. New `td.num` cells
  need a `data-label` attribute or they will lose their heading on mobile.

Push to `main` and the site republishes itself, usually within a minute. That is GitHub's
own builder, configured under **Settings → Pages → Source: _Deploy from a branch_ →
`main` / `(root)`**. There is no workflow in this repository and none is needed.

Progress on the checklist and the exchange rate in the top bar are stored per-browser, so
they do not travel between devices and are not part of the repository.
