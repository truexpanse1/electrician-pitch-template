# Electrician Pitch Template — Project Status

## Repo & Deploy
- GitHub: `truexpanse1/electrician-pitch-template`
- Netlify: `electrician-pitch.netlify.app`
- Netlify Project ID: `75ac2ce2-4a78-4919-9229-746c4a4903c2`
- Latest deploy: `main@97af8d8` (2026-05-20)

## Purpose
Single-page demo template for 4 Monterey-area electrician sales appointments on 2026-05-20. Each prospect gets their own brand-swapped view via URL hash. Pitch ends with 5 value-add pages explaining the full TrueXpanse stack (GHL, MAT, Coaching, Quantum AI Command, Summary).

## Inspiration
- `rpcourtneypainting.com` — Ryan Courtney Painting, currently ranking well for San Mateo painting queries. Lifted the structure, color palette (dark navy `#1f1e26` / orange `#ff471d`), fonts (Audiowide + Inter), JSON-LD pattern, and conversion architecture.
- Schema type swapped: `HousePainter` → `Electrician`.

## Routes
| Hash | Brand | License | Reviews |
|------|-------|---------|---------|
| `/` or `#home` | TrueXpanse Electric (default) | — | none |
| `#e1` | AF Electric (Andres Flores) | — | 4 real |
| `#e2` | Point Break Electric | CA #1092452 | placeholder |
| `#e3` | Aragon Electrical Services | CA #1116511 | 4 real |
| `#e4` | Oscar's Electric Services | — | placeholder |
| `#ghl` | GoHighLevel CRM pitch | — | — |
| `#mat` | Massive Action Tracker pitch | — | — |
| `#truexpanse` | TrueXpanse Coaching pitch | — | — |
| `#qac` | Quantum AI Command pitch | — | — |
| `#summary` | Full-stack summary + CTA | — | — |

## Direct Pitch URLs (paste in appointments)
- AF Electric: https://electrician-pitch.netlify.app/#e1
- Point Break: https://electrician-pitch.netlify.app/#e2
- Aragon Electrical: https://electrician-pitch.netlify.app/#e3
- Oscar's Electric: https://electrician-pitch.netlify.app/#e4
- Stack summary: https://electrician-pitch.netlify.app/#summary

## Data Integrity Rules Followed
- **Real reviews only** — AF (4) and Aragon (4) verbatim from their live sites. Point Break and Oscar's get "Reviews coming soon" placeholder (no fabrication).
- **License numbers only when published** — Point Break #1092452, Aragon #1116511 from their live sites; AF and Oscar's site didn't show a number so generic "C-10 Licensed" used.
- **Brand colors are defensible placeholders** — Final colors to be confirmed with each owner if they sign. Currently chosen to match each business's existing tone.
- **No invented offers, no fabricated guarantees.**

## Tech Notes
- Single `index.html`, vanilla HTML+CSS+JS, Tailwind CDN
- `BRANDS` object at bottom of `index.html` is the single source of truth
- Hash router applies brand colors as CSS vars + swaps `data-bind` content
- 2 Netlify forms wired: `hero-quote`, `contact-quote` (both include hidden `brand` field)
- JSON-LD `Electrician` schema regenerated per brand for SEO

## Footer Credit
Dofollow link to truexpanse.com in utility bar + footer (per `feedback_truexpanse_footer_backlink.md`).

## Pending / Post-Appointment
- If a prospect signs: spin out a dedicated repo, get owner's real logo + brand hex codes, get real testimonials, get exact street address + Google Place ID, swap stock hero image for a real job photo, wire up GHL webhook to receive form leads.
- Stock hero images currently from Unsplash — replace with real job photos as soon as each client provides them.

## Build Date
2026-05-20
