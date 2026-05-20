# Electrician Pitch Template

Single-page SPA demo for 4 Monterey-area electrician sales appointments. Built as a TrueXpanse demonstration: shows what a conversion-grade electrician landing page looks like, brand-swapped via URL hash for each prospect.

## Routes

| Hash | View | Brand |
|------|------|-------|
| `#home` or `/` | Generic electrician landing page | TrueXpanse default |
| `#e1` | Electrician landing page | AF Electric (Andres Flores) |
| `#e2` | Electrician landing page | Point Break Electric |
| `#e3` | Electrician landing page | Aragon Electrical Services |
| `#e4` | Electrician landing page | Oscar's Electric Services |
| `#ghl` | GoHighLevel CRM value page | n/a |
| `#mat` | Massive Action Tracker value page | n/a |
| `#truexpanse` | TrueXpanse Coaching value page | n/a |
| `#qac` | Quantum AI Command value page | n/a |
| `#summary` | Full-stack summary + CTA | n/a |

## Inspired By

Structure / SEO patterns lifted from `rpcourtneypainting.com` (currently ranking well for San Mateo painting queries). Same visual identity (dark navy + orange accent, Audiowide + Inter), same JSON-LD pattern (LocalBusiness + AggregateRating + Review[] + hasCredential), same conversion architecture (hero with form, marquee, services grid, dark testimonial grid, contact form, license strip).

Schema type swapped from `HousePainter` → `Electrician`.

## Brand Config

All brand data lives in the `BRANDS` object inside `index.html`. To add a 5th electrician or update an existing one, edit that object — colors, phone, license, services, and reviews all swap from a single source of truth.

## Real-Data Rules Followed

- **Reviews**: Only verbatim reviews extracted from each electrician's live site are shown. If none were found (Point Break, Oscar's), a "Reviews coming soon — request samples" placeholder is shown instead. **No fabricated testimonials.**
- **License numbers**: Only shown when the live site publishes them (Point Break #1092452, Aragon #1116511). Otherwise generic "C-10 Licensed" used.
- **Brand colors**: Chosen as defensible placeholders matching the tone of each business. Final colors to be confirmed with each owner.

## Forms

Two Netlify forms wired:
- `hero-quote` — sidebar form on hero
- `contact-quote` — full form in contact section

Both include hidden `brand` field so submissions identify which demo the prospect filled out.

## Deploy

Static SPA. `netlify deploy --dir . --prod` or push to a Netlify-linked GitHub repo.
