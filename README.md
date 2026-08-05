# Economics of Transformative AI — event site

Single-page static site for the research sprint, 14–16 August 2026.

## Deploy

No build step, no dependencies. `index.html` sits at the repo root.

1. Push this repo to GitHub.
2. In Vercel, **Add New → Project**, import the repo.
3. Framework preset: **Other**. Leave build command and output directory empty.
4. Deploy.

Every push to the default branch redeploys. Pull requests get preview URLs.

## Before going live

Search the file for `TBD` — these still need filling:

- `[time TBD]` — intro session (12 Aug) and office hours (15 Aug)
- `$X,000` — prize amount, in the hero facts row
- `Judges announced soon` — replace with names and affiliations once confirmed
- `[contact TBD]` — appears in the conduct rule and the footer

Confirmed already: sprint runs 12:00 am Fri 14 Aug to 11:59 pm Sun 16 Aug, Pacific Time.

## Editing

Everything is in `index.html` — markup and styles in one file, no framework.

**Colours** are CSS custom properties in `:root` at the top:

| Variable | Use |
|---|---|
| `--green` | hero and closing sections |
| `--green-deep` | button hover |
| `--sprout` | small accents: numbers, weights, list marks |
| `--wash` | pale grey-green panel fill |
| `--line` | hairline rules |

**Fonts** are also in `:root`. `--display` and `--sans` are currently both Plus Jakarta Sans, matched by eye to the Match UI. If the product uses a different family, change those two variables and the Google Fonts `<link>` in `<head>` — nothing else references a family by name.

**The register link** is `https://try.mangrove.one/alpha`, in three places: hero, sticky nav, and closing section.

## Notes

- Responsive down to mobile; `prefers-reduced-motion` respected; focus states visible.
- FAQ uses native `<details>` elements — no JavaScript on the page at all.
- Open Graph tags are in `<head>`. Add an `og:image` before promoting anywhere that renders link previews.
