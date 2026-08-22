# Changelog

## v4 — Aug 22, 2026

**Status:** complete (redesign + 10 new equity research entries)

- Full visual redesign: dark/black theme (`--black`, `--charcoal` tokens) replacing the navy palette; hero header now uses a Toronto (CN Tower) skyline photo (`assets/cn-tower.jpg`) with a dark gradient overlay instead of a solid navy gradient
- Meta description updated to lead with "Real estate private equity, valuation, and financial modelling portfolio"
- Equity Research section restructured from static `.card.research` cards into an expandable accordion (`.acc-co-*` classes), grouped by ticker/exchange with an inline Neutral/Overweight badge and report date in the summary row
- 10 new equity research one-pagers added, bringing the section to 15 total:
  - AMZN (Amazon.com) — 12 Mar 2026
  - PG (Procter & Gamble) — 21 Apr 2026
  - COST (Costco Wholesale) — 5 Feb 2026
  - 2222 / ARAMCO (Saudi Arabian Oil Co., Tadawul) — 26 May 2026
  - OSCR (Oscar Health) — 28 Aug 2025
  - UNH (UnitedHealth Group) — 22 Jul 2025
  - ENBDREIT (ENBD REIT, Nasdaq Dubai) — 30 Jul 2026
  - QBTS (D-Wave Quantum) — 9 Jun 2025
  - NEE (NextEra Energy) — 17 Jun 2026
  - WBD (Warner Bros. Discovery) — 14 Nov 2023
- Files stored as `downloads/AMZN_Equity_Research.pdf`, `PG_Equity_Research.pdf`, `COST_Equity_Research.pdf`, `ARAMCO_Equity_Research.pdf`, `OSCR_Equity_Research.pdf`, `UNH_Equity_Research.pdf`, `ENBDREIT_Equity_Research.pdf`, `QBTS_Equity_Research.pdf`, `NEE_Equity_Research.pdf`, `WBD_Equity_Research.pdf`

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
