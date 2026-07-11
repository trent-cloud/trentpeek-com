# trentpeek.com — deploy notes

Rebuilt 2026-07-11 from Richard's Claude Design direction ("Trent Peek & Richard Ardis Brand Websites" export, 2026-07-10). Four pages — index, biography, work, contact — sharing `assets/style.css` with richardardis.com (DM Sans, white, deep green #1E4D3B, sticky rail). The Fragility–Autonomy Matrix is a named interactive on the home page, wired to the playable approval-queue demo. Previous single-page build archived in `archive-2026-07-10/`.

Verified 2026-07-11: rendered desktop + 390px in-browser; approve/reject/reset paths DOM-tested; unprimed screenshot critique + 4-lens adversarial audit (facts vs SHARED-FACTS, vocabulary, code/a11y, links) — all confirmed findings fixed.

## Before it goes live — Trent's gates

1. **The candour sentence (D2).** Visible copy says only "We Are Fulfilment closed in March 2026." The locked administration sentence ships ONLY after joint sign-off — and as a copy replacement, not an HTML comment (a drafting comment that leaked it into page source was removed 2026-07-11; don't reintroduce).
2. **hello@trentpeek.com doesn't exist yet** — set up email routing at the registrar/Cloudflare before deploy.
3. **LinkedIn URL** assumed linkedin.com/in/trentpeek — confirm the custom URL (LinkedIn brief sets it).
4. **Awards wording** ("FEBE Growth 100 2024", "Entrepreneur of the Year (East Midlands, 2021)") comes from the founders' design brief but is still ⚠ unreconciled with SHARED-FACTS — confirm before deploy.

## Deploy (same pattern as the Woodlark site)

1. Register trentpeek.com (spend — Trent's action).
2. Cloudflare Pages/Workers static assets, point at this folder (all four .html + assets/).
3. Email routing for hello@ → Trent's inbox.
4. Post-deploy: Google Search Console + request indexing (JSON-LD Person + titles are set to win the bare-name search).
5. Allow reputable AI crawlers (some AI recruiter tools fetch pages; Woodlark's config 403s them).
