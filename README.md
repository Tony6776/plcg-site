# PLCG marketing site

Static single-page marketing site for plcg.com.au — Property · Land · Construction Group, the SDA construction arm of the Homelander group.

## Deployment

Single `index.html` deployed via Vercel. No build step. CSP-locked, security headers via `vercel.json`.

## Form

Contact form posts to `https://bqvptfdxnrzculgjcnjo.supabase.co/functions/v1/website-form-direct` with `form_type='plcg_quote'`, `website='plcg.com.au'`. Lead lands in `leads` table with `category='general'` (or specific based on product_hint), tied to a `persons` row, fires SMS/email/Telegram cascade.

`form-progress-capture` fires on email/phone field blur for partial-form recovery.

## Built 2026-04-30
