# Japan trip, February 2027

A single-page trip plan — route, budget, day-by-day itinerary and a pre-departure checklist.

**Live site:** https://f3nici.github.io/japan-trip/

## Editing

The whole site is one self-contained file: [`index.html`](index.html). No build step, no
dependencies — open it in a browser to preview changes locally.

Every push to `main` redeploys the site via
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml), which usually takes under a
minute. The workflow can also be run by hand from the **Actions** tab.

The first run switches Pages on by itself, so there is nothing to configure in the repository
settings.
