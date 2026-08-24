# Changelog

## v7 — Aug 23, 2026

**Status:** complete (Equity Research expansion, GitHub repos published, Excel download wired up)

- Equity Research rebuilt: every sector panel now shows a "Top Pick" card followed by an "All Coverage · newest first" list of collapsed cards (sectors with only one report just show the Top Pick, no coverage list). Total is now 28 items (27 formal notes + the PGAS early stock pitch), up from 16.
- 12 new "early work" cards added (BN, CNQ, CP, CSU, ENB, EQB, HPS, JPM, KXS, LLY, MSFT, RY), all dated 23 Aug 2024, with an "Early Work" pill next to the rating badge
- WBD card fully replaced (was a placeholder/older draft) with the real 13 May 2025 note content
- The two RIT trading-algorithm projects ("Liability Trading Engine" and "Cross-Exchange Arbitrage Algorithm") are now published as separate public repos and linked from their project cards, replacing the `data-github-pending` placeholder buttons: `tender_vwap_trader.py` → [RIT-Tender-VWAP-Trader](https://github.com/akul-veauli/RIT-Tender-VWAP-Trader), `market_maker.py` → [Algo-Trader](https://github.com/akul-veauli/Algo-Trader)
- Live Valuation Demo now carries a "Beta" pill and disclaimer sentence, and the raw XBRL-tag-conflict `warnings[]` array is no longer rendered (internal debug noise, not user-facing)
- Live Valuation Demo: "Download the Excel model" button is wired up (`EXCEL_ENDPOINT` now points at `/api/excel?ticker=` on the `dcf-live-api` backend). Building that endpoint surfaced two backend bugs, both fixed: an `input()` prompt for unrecognised industries was crashing with `EOFError` on the server (no stdin) — this had been silently breaking `/api/valuation` too, not just the new endpoint — and the Excel writer assumed the AI-narrative dict was never `None`, which it always is on the web path (`run_ai=False`)
- Model Library's "Built by Hand" accordion no longer defaults to open on page load
- Style rule adopted: avoid em dashes in all site copy and documents

## v6 — Aug 23, 2026

**Status:** complete (Equity Research redesign + Experience section removed)

- "Professional Experience" section (Education / Work Experience / Leadership, `id="experience"`) removed entirely, along with its "Experience" nav link and the now-unused `.xp` / `.subhead` CSS
- Equity Research restructured from per-sector `<details class="acc-sector">` accordions into a clickable sector-tile grid (`.sector-grid` / `.sector-tile`, new `--gold` token): one tile per sector showing a report-count badge, click opens that sector's `.sector-panel` (only one open at a time), driven by a new small inline-script click handler
- PGAS (PT Perusahaan Gas Negara) moved from a bare download link in the Model Library's "DCF / Valuation" group into a full Utilities equity-research entry alongside NEE, with its own thesis/summary and base/bull/bear metrics — bringing Equity Research to 16 reports (count copy updated 15 → 16 accordingly)
- Hero stats: "15 Equity Research Reports" swapped for "$130B+ Transaction Value Analyzed"
- About-block closing line swapped from a subjective claim ("best automation-and-valuation analyst...") to a pointer at the evidence ("downloadable models, published research, and a live valuation engine you can run yourself")
- Live Valuation Demo: cold-start copy now sets expectations at up to 2 minutes (was "up to a minute"); added a live elapsed-time counter (`.demo-elapsed`) next to the status text while a request is in flight; status message now escalates through three stages (waking up → still waking up → almost there) instead of one fixed "still working" message at 4s
- Live Valuation Demo error handling now distinguishes quota/rate-limit errors (402/403/429 or detail text mentioning quota/budget/credit/rate limit/insufficient) from generic 5xx/unparseable responses, each with a tailored message, instead of a single generic error string
- `deals`, `models`, `achievements`, and `skills` sections toggled between plain/`alt` background to keep the alternating rhythm now that `experience` is gone

## v5 — Aug 23, 2026

**Status:** complete (Live Valuation Demo wired up to the real DCF API)

- The "Live Valuation Demo" card in the Projects section is no longer a disabled "Coming Soon" placeholder — it now calls the live DCF engine API (`web_api/` in the `dcf-live-api` repo, deployed on Render at `https://akul-dcf-api.onrender.com`)
- Enter a supported ticker and get back current price, DCF-implied price, upside/downside, WACC, terminal growth, and a BUY/HOLD/SELL rating, styled to match the card's dark theme
- Loading state shows a spinner immediately and, if the free-tier server is asleep, switches to a "waking up" message after ~4 seconds so a 30-50s cold start doesn't look broken
- Errors from the API (unsupported ticker, rate limit, daily cap, engine failure) are shown inline instead of failing silently
- No new dependencies: vanilla JS `fetch()` in an inline `<script>`, no build step
- Known issue carried over, not introduced here: some tickers (e.g. `JPM`) currently error out on the API side (`MetricNotFiledError`) — example tickers shown in the UI were chosen to avoid this until it's fixed

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

- Update SFR model to replace v1 when ready
- Add more code-generated workbooks after validation
- Add more equity research reports over time. Keep adding to `.card.research`, no cap yet
- More models to be added to the Model Library (site now publicly says "through the end of August 2026")
- When any category gets long, narrow to top 3 per category
