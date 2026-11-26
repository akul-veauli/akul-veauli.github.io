# Changelog

## v11: Nov 25, 2026

**Status:** complete (retrospective notes relabelled, their PDFs rebuilt, card, project and Model Library text checked against their files)

- The twelve notes previously dated 23 Aug 2024 and tagged Early Work (BN, CNQ, CP, CSU, ENB, EQB, HPS, JPM, KXS, LLY, MSFT, RY) are retrospective notes, written in August 2026 as of 23 August 2024 using only information public on that date. The site now tags them Retrospective (a grey pill, distinct from the amber Early Work tag) and dates them "As of 23 Aug 2024", and the lede and Methodology note say so. The Methodology note also says they apply a single forward multiple with no cross-checks and count dividends through the target date
- The twelve PDFs were rebuilt with real creation dates (the metadata is no longer backdated), a header and cover date reading "As of 23 August 2024 · retrospective, written August 2026", and a disclosure saying the estimates were made in August 2026 and that the notes were relabelled and rebuilt in November 2026 with no price, estimate or target changed. The cash-flow and peer cross-check rows and every "cross-checked against" claim were removed, since each target rests on one multiple; the EQB thesis now calls its 1.3x forward book "equivalent to" the EPS-based target rather than a second method. Source notes call the estimates "retrospective" instead of "contemporaneous", and the BN price source now says "see also the TMX Alpha daily record" instead of "daily-record cross-check". Bull and bear scenario values are unchanged but labelled illustrative (set 22% above and 32% below the target), and the probability-weighted value was removed. Subtitles and theses no longer use spaced hyphens as dashes, and every table fits within the page margins. Prices, targets, estimates, dividends and returns are unchanged
- CSU moved from Neutral to Overweight: its 15.1% expected total return clears its own "Overweight above 15%" scale, and its disclosure says the rating was revised in November 2026 to follow that scale. The PDF now defines FCFA2S at first use, and the card glosses it as free cash flow available to shareholders
- The UNH summary now gives the note's CMS figures (a 5.06% expected average Medicare Advantage revenue increase for 2026, up from 3.70% for 2025) instead of "the widest increase in years". The ENBDREIT summary now says the 8.1% yield is more than half of the expected +14.1% return, not effectively all of it
- Model Library: the dESCO model row now describes its exit-multiple valuation at 5.1x EBITDA (the workbook has no DCF), and the deck row no longer mentions a letter of intent, which none of its 25 slides contains. In the Hilton LBO, Returns!B68:B69 now say the revenue path applies a hindsight downturn (FY2009E -16%, FY2010E -6%) that is an assumption rather than Hilton's reported revenue, and that the 2010 restructuring is not modeled. Cover!B8 and Returns!B74, which called the model pre-crisis, now say it includes that hindsight revenue downturn and LIBOR path but not the 2010 restructuring; no other cell changed, and Excel's cached values are intact
- Projects: the LBO / Take-Private Modeller card no longer says every cell is a live formula. It now says the workbook is live formulas off an editable Inputs sheet, except the cash-sweep rows and sensitivity grids, which the Python engine writes as values, with outputs verified against the engine

## v10: Nov 25, 2026

**Status:** complete (credibility pass: note count, Return and Upside labels, Featured label, Early Work rule, unsupported claims, unfinished items, card and Model Library text checked against their files)

- Equity Research count: the stat band, About line and lede said 28 notes while the sector tiles summed to 29. They now say 29 research notes (28 initiation and update notes plus the PGAS stock pitch). A small inline script recomputes those numbers, the tile badges, the panel headers and the "N more" labels from the cards on the page (`data-count`); the static numbers stay as the no-JS fallback
- Card metrics now follow one rule, stated under the Equity Research lede: `Return` is price-target upside plus expected dividends, `Upside` is the price move alone. Relabelled `Upside` to `Return` on 11 cards whose figure includes dividends (CNQ, ENB, RY, JPM, BN, EQB, LLY, CP, HPS, MSFT, CSU) and `Return` to `Upside` on 3 cards that pay no dividend (WBD, OSCR, QBTS), each checked against its note PDF. No figures changed
- "Top Pick" renamed "Featured" in all 11 sector panels, since 8 of the 11 lead notes are rated Neutral or Underweight; the lede now says the label is not a rating. CSS class names unchanged
- Early Work rule in the lede reworded to match the tags: "Notes dated 2024 and the Spring 2025 stock pitch are tagged Early Work and left up on purpose so the progression is visible." The lede also says the rest of each sector is listed newest first, as the lists already were
- Hero stats: "$3B+ AUM Supported" (nothing in the repo supports it) replaced with "23 Models & Analyses Posted", counted from the Model Library rows on the page, and "8× First-Place Finance Competitions" relabelled "First-Place Competition Finishes", since 2 of the 8 listed wins are not finance competitions. The DCF engine's "412 built-in audit checks" bullet lost its number, which nothing in this repo supports; the version-stamp claim stays (`Pipeline Fingerprint` in `downloads/CELH_DCF_Code_Generated.xlsx`)
- Unfinished items: empty Real Estate and Waterfalls placeholders removed from the Model Library's Early Work list, Investment Memo Creator card removed (no sample output in the repo), the Live DCF Demo caveat moved out of the input hint into a reworded footnote under the result area, and the Model Library filter status no longer says earlier work is collapsed below for model types that have none
- Card text checked against the notes: the Cogeco summary now says the stock trades "near" its 52-week low (C$54.71 against a C$54.25 low), and the WBD summary gives the note's "two and a half to three and a half more years"
- Model Library descriptions checked against the workbooks: the Microsoft and Apple DCFs are five-year models (described as 10-year), the Apple DCF has no scenario toggles, the Microsoft three-statement model has no stress case, and the Hilton LBO does not model the 2010 restructuring, so those phrases were corrected or removed
- Equity Research: added a short Methodology note (price-target method, Return definition, rating scales, price dates, coverage) above the Disclosure, every statement taken from the notes themselves
- Equity Research is now linkable as `#equity-research` (same landing position as `#research`, which still works)

## v9 — Sep 10, 2026

**Status:** complete (stat fix, Verizon/Vodafone model correction, equity research refresh)

- Hero stat band: "Acquisition Modelled" `$550M` → `$500M+`, matching the Gold Producer Acquisition Analysis deal card's "~$500M+" entry figure
- `downloads/Verizon_Vodafone_MA_Analysis.xlsx` replaced with the corrected model: the "Deal Structure & Capital Impact" consideration bridge on the live site had a hard-coded total consideration of $131,274mm (~$1.3 Bn too high, and no longer a live formula) that didn't match its own "~$130.3 Bn" header. Restored to the version where TOTAL CONSIDERATION is a live `=SUM()` formula totalling $130,000mm, consistent with the header and the actual deal
- Equity research PDFs refreshed (`AMZN`, `ARAMCO`, `AXON`, `CADY`, `COST`, `EEFT`, `ENBDREIT`, `NEE`, `NU`, `OSCR`, `PG`, `QBTS`, `SOFI`, `UNH`, `WBD`) and new note added: `downloads/CGO_Equity_Research.pdf` (Cogeco Inc., Overweight, 10 Sep 2026)

## v8 — Aug 29, 2026

**Status:** complete (index rework, Model Library expansion, client name scrubbed)

- `index.html` reworked: section order is now About / Deal & Strategy Experience / Model Library / Equity Research / Projects / Achievements / Skills / Connect (Deal Experience and Model Library moved above Equity Research and Projects); ~450 lines added, ~236 removed
- **Git history rewritten** on this date to strip the former issuer name from every historical revision of `index.html`, then force-pushed. All commit hashes prior to this entry changed. Old unreachable commits may linger on GitHub by direct SHA for up to ~90 days; external caches (Wayback, Google) are outside our control
- Resume pulled from the site: hero "Download Resume" button and the Model Library "Resume" card both removed; `downloads/Akul_Veauli_Resume.pdf` deleted from the repo
- Model Library expanded with 17 hand-built workbooks: `3_Statement_Model_Microsoft`, `DCF_Model_Apple` / `_Microsoft` / `_Nvidia` / `_Alphabet`, `LBO_Model_Hilton_Blackstone_2007`, `LBO_Model_Twitter_X_2022`, `Merger_Model_Broadcom_VMware_2023` / `_Disney_Fox_2019` / `_Exxon_Pioneer_2023`, `Distribution_Waterfall_Model`, `Portfolio_Optimization_Model_NU_SPY_AGG`, `Precedent_Transactions`, `Trading_Comps_Football_Field`, `VC_Fund_Monte_Carlo_Portfolio_Construction`, `Toronto_Multifamily_Acquisition_Model`, `Texas_SFR_Investment_Model`
- `downloads/SFR_Model_v1.xlsx` removed, superseded by `downloads/Texas_SFR_Investment_Model.xlsx`

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

- Add more code-generated workbooks after validation
- Add more equity research reports over time. Keep adding to `.card.research`, no cap yet
- More models to be added to the Model Library (site now publicly says "through the end of August 2026")
- When any category gets long, narrow to top 3 per category
