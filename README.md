# progfi-website

Static site for **progfi.xyz**, deployed via GitHub Pages.

## Structure
- `index.html` — root placeholder (homepage). **Replace this** when the real homepage is ready; the root is intentionally minimal for now.
- `ai-readiness/index.html` — the **AI Readiness Check**: a self-contained, client-side maturity assessment (10 dimensions, governance/security gating, level + gaps + safe-autonomy ceiling, ending in a contact CTA). No backend, no keys, nothing leaves the browser.
- `.nojekyll` — tells GitHub Pages to serve files as-is (no Jekyll processing).

## URLs
- Test (before DNS): `https://demirelo.github.io/progfi-website/ai-readiness/`
- Live (after DNS): `https://progfi.xyz/ai-readiness/`

## Configuring the check
In `ai-readiness/index.html`, near the top of the `<script>`:
- `BOOKING_URL` — set to your Cal.com / Calendly link to show a "Book a working session" button. Leave `""` for email-only.
- `CONTACT_EMAIL` — currently `omer@progfi.xyz`.

## Custom domain (progfi.xyz)
Add these DNS records at your registrar, then set the custom domain in the repo's Pages settings (adds a `CNAME` file):
- Apex `progfi.xyz` → four A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `www` → CNAME `demirelo.github.io`
