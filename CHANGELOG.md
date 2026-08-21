# Changelog

## v3 — Aug 21, 2026

**Status:** complete (Equity Research section added)

- New "Equity Research" section added between Experience and Deals, with nav link "Research"
- 5 equity research one-pagers added (style exercise, J.P. Morgan format, explicit disclosure that it's unaffiliated / not investment advice):
  - AXON (Axon Enterprise) — Neutral, PT $670 (Dec-27), 20 Aug close $614.26
  - CADY (Cadillac Mines) — Neutral, PT C$8.30, 20 Aug close C$8.30
  - EEFT (Euronet Worldwide) — Overweight, PT $92.00, 20 Aug close $69.38
  - NU (Nu Holdings) — Overweight, PT $17.00, 20 Aug close $14.21
  - SOFI (SoFi Technologies) — Neutral, PT $19.50, 20 Aug close $17.92
- Files stored as `downloads/AXON_Equity_Research.pdf`, `CADY_Equity_Research.pdf`, `EEFT_Equity_Research.pdf`, `NU_Equity_Research.pdf`, `SOFI_Equity_Research.pdf`
- New CSS: `.card.research`, `.rc-head` / `.rc-ticker` / `.rc-metrics` / `.rc-foot` / `.rc-date`, `.badge.ow` (green, Overweight), `.badge.neutral` (gray)
- Alternating section background preserved: about (plain) - experience (alt) - research (plain) - deals (alt) - projects (plain) - library (alt) - achievements (plain) - skills (alt)

### Site philosophy (per Akul, Aug 21 2026)

This site is meant to show **all** of Akul's finance work, comprehensively — not a curated top-N. Once any category (Equity Research, Projects & Models, Model Library) gets too long, Akul will say when it's time to narrow it down to his top 3 per category. Until then, keep adding everything. Section-lede text in all three of those sections says this explicitly ("this section holds everything... once it grows I'll narrow to top 3").

## v2 — Aug 18, 2026

- Headshot added to hero (right side), LinkedIn added: https://www.linkedin.com/in/akul-veauli-6b7370219/
- "Analyst" removed from job titles (plain "Intern"); "BBA with Distinction" → "BBA"
- All em dashes removed sitewide
- Phone number removed (email + LinkedIn only)
- Interests kept (poker/chess/bodybuilding)
- Model Library download section added, two groups: "Built by Hand" and "Generated Entirely by Code"
- Resume download button added (IB Resume version)
- Timbercreek/CI work described only, labeled "Employer Confidential" — never posted as a downloadable file

## Deploy

GitHub Pages, repo `akul-veauli.github.io`, site contents at repo root → https://akul-veauli.github.io

## Next steps

- Push project repos to github.com/akul-veauli (strip `.env` / venv before pushing)
- Update SFR model to replace v1 when ready
- Add more code-generated workbooks after validation
- Add more equity research reports over time — keep adding to `.card.research`, no cap yet
- When any category gets long, narrow to top 3 per category
