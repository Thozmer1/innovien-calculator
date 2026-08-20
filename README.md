# Innovien Solutions — Spread & Commission Calculator

Internal tool for calculating weekly spread and commission across domestic, federal, and nearshore placements.

**Live URL:** _(add after first Vercel deploy)_

## What's here

- `index.html` — The entire calculator. Self-contained, no build step, no backend. Vercel serves this at the root URL automatically.

## Deploy

Auto-deploys to Vercel on every push to `main`. See `DEPLOYMENT.md` in the parent Finance Optimization project for the full deploy guide.

## Update the rates

All configurable values live in the `SETTINGS` block near the top of `index.html`. Edit, commit, push — Vercel deploys in ~30 seconds.

- **Domestic burdens** (W-2 no-benefits, W-2 with benefits, C2C)
- **RTX rebate** (added to base burden for RTX placements)
- **Federal holiday burden** (added to base burden for federal placements)
- **Nearshore country rates** (social %, EOR fee, VAT, aguinaldo)
- **Nearshore C2C add-on** (added to domestic C2C burden for contractor placements abroad)
- **Commission tiers** for AM and Recruiter roles
- **Base salaries** for AM and Recruiter

## Tabs

1. **Domestic Spread** — Non-RTX and RTX scenarios × W-2 NB / W-2 B / C2C matrix, plus sensitivity analysis.
2. **Federal Placement** — Base burden + 5% federal holiday burden baked in, plus a PTO break-even pay calculator (2 or 4 weeks).
3. **Nearshore Spread** — EOR (employee via Employer of Record) across 16 countries, plus a C2C (contractor) alternative column at flat 13% burden.
4. **Weekly Commission** — Tier breakdown for AM and Recruiter roles with annual comp projection.

Any calculated spread cell across the first three tabs can be clicked to send that value into the Commission tab.

## Visual convention

- **Green-tinted cells with ✎ EDIT marker** = your inputs (editable)
- **White cells** = calculated results (read-only)

## Support

Owned by Taylor Hosmer (`thosmer@innovien.com`).
