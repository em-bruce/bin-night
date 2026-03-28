# Bin Night — Project Context

## What this is
A single-file web app (`index.html`) that tells the user which bins to put out for their weekly council collection. Hosted on GitHub Pages, saved to iPhone home screen for quick access.

## Owner
- **Address:** 15 Myers Street, Sans Souci, NSW
- **Council:** Georges River Council
- **Collection zone:** Wednesday Zone 2

## Bin schedule
- **Red (General Waste):** every Wednesday without exception
- **Yellow (Recycling) / Green (Garden Waste):** alternate each week
  - Even weeks from anchor: Red + Green
  - Odd weeks from anchor: Red + Yellow

### Anchor date
`1 April 2026 = Red + Green`

All schedule logic derives from this anchor. See `getBinsForWednesday()` in `index.html`.

### Verified example dates
| Date | Bins |
|------|------|
| Wed 1 Apr 2026 | Red + Green |
| Wed 8 Apr 2026 | Red + Yellow |
| Wed 15 Apr 2026 | Red + Green |
| Wed 22 Apr 2026 | Red + Yellow |

## App behaviour
- **Any day:** always shows the next upcoming Wednesday's bins
- **Tuesday only:** adds a "🌙 Put the bins out tonight" heading as a reminder
- Shows the collection date and a "View full calendar" button

## Council calendar PDF
https://www.georgesriver.nsw.gov.au/StGeorge/media/Documents/Services/Waste%20and%20Recycling/WasteCalendars/Waste-Calendar-2026-Wed-Zone-2.pdf

## Deployment
- **Repo:** `bin-night` (public GitHub repo)
- **Live URL:** `https://YOUR-USERNAME.github.io/bin-night`
- **Platform:** GitHub Pages, served from `main` branch root
- **To deploy changes:** edit `index.html`, then `git add . && git commit -m "..." && git push`

## Tech stack
- Plain HTML/CSS/JS — no build step, no dependencies, no framework
- Google Fonts: Syne (headings) + DM Sans (body)
- All logic is in a single `<script>` block in `index.html`

## Design
- Dark theme (`#0f1117` background)
- Coloured bin SVGs: red / yellow / green matching physical bin colours
- Animated entrance, colour glow behind active bins
- Responsive, mobile-first — designed to be used on iPhone home screen
