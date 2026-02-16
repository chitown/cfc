# Sports Betting Affiliate + Strategy Platform — Project Package

_Packaged: 2026-02-16_

## What This Project Is

A **freemium sports betting strategy + odds intelligence platform** that helps users explore odds/lines, build and backtest betting strategies, and generate bet slips with deep links to regulated US sportsbooks. Primary monetization is affiliate CPA/RevShare deals with operators (FanDuel, DraftKings, BetMGM, Caesars, bet365, etc.), supplemented by premium subscriptions and ads.

**Key design constraint:** No auto-betting. US sportsbooks don't offer public wagering APIs and prohibit bots. The product generates actionable bet slips + deep links; the user confirms bets inside the sportsbook's own app.

---

## File Inventory

### Core Strategy & Blueprint

| File | What It Is |
|------|------------|
| `sports_betting_affiliate_ai_blueprint__1_.md` | **Master blueprint.** Covers affiliate program details (BetMGM, Caesars, bet365, FanDuel, DraftKings), state-by-state compliance, channel restrictions, product architecture, tech stack, 12-month roadmap, and go-to-market strategy. Start here. |
| `Next_Gen_Sports_Tracking_Data_Guide.md` | **Data sourcing guide.** Catalogs every significant source of advanced analytics data across 11 sports (NFL, NBA, MLB, NHL, soccer, tennis, golf, MMA, F1, cricket, horse racing). Covers free vs paid sources, APIs, open-source libraries, and which metrics are most predictive. Essential for the stats/backtest engine. |

### 3-Year Customer Acquisition Roadmap

| File | What It Is |
|------|------------|
| `3_year_acquisition_roadmap_package.md` | Executive summary of the full 3-year acquisition plan — deliverables list and next steps. |
| `3yr_launch_customer_acquisition_report.md` | Full 36-month roadmap with phase goals (Prove → Scale → Optimize), quarter-by-quarter execution plan, financial model blueprint with core formulas. Also available as `.txt` and `.pdf`. |
| `investor_slide_outline.md` | 10-slide investor/board deck outline template. Also `.txt` and `.pdf`. |
| `kpi_dashboard_one_pager.md` | KPI dashboard template — weekly, monthly, quarterly metrics. Also `.txt` and `.pdf`. |
| `model_structure_and_formulas.md` | Financial model structure — inputs, outputs, scenarios. Also `.txt` and `.pdf`. |

### Financial Model (Spreadsheet + CSVs)

| File | What It Is |
|------|------------|
| `3yr_launch_acquisition_financial_model_template.xlsx` | Excel financial model template with multiple tabs. |
| `assumptions.csv` | Model assumptions: ACV ($12K), 75% gross margin, 2% monthly churn, 2-month sales cycle lag, conversion rates (12% Lead→SQL, 35% SQL→Opp, 22% Opp→Win). **These are defaults — replace with actuals.** |
| `monthly_base.csv` | 36-month base scenario projections (spend, leads, SQLs, opps, wins, customers, MRR, ARR). |
| `monthly_optimistic.csv` | 36-month optimistic scenario. |
| `monthly_pessimistic.csv` | 36-month pessimistic scenario. |
| `cohort_customers_base.csv` | Year 1 monthly cohort: customers acquired per month (2→7 over 12 months). |
| `cohort_mrr_base.csv` | Year 1 monthly cohort: starting MRR per cohort ($200→$600 over 12 months). |
| `hiring_plan.csv` | Hiring plan: Founder (M1) → Marketing (M6) → SDR (M9) → AE (M10) → CS (M15). |
| `scenario_summary.csv` | Scenario labels and status (all marked "Template"). |
| `sensitivity.csv` | Sensitivity analysis: ±20% swings on ACV, win rate, and churn. |

---

## What's Been Done

1. **Market research** on affiliate programs — verified public details for BetMGM, Caesars, bet365, FanDuel, DraftKings.
2. **Compliance framework** — state-by-state legality snapshot, channel restriction matrix, universal rules (geo-fencing, age-gating, RG language).
3. **Product architecture** — 6 core services defined (data ingestion, feature store, strategy engine, recommendation service, affiliate routing, compliance layer).
4. **Tech stack recommendation** — Python/FastAPI backend, Postgres + TimescaleDB, Next.js frontend, etc.
5. **Data sourcing guide** — comprehensive catalog of free/paid data sources across 11 sports.
6. **Financial model** — template with 3 scenarios, cohort analysis, hiring plan, sensitivity analysis.
7. **GTM plan** — affiliate-first acquisition, SEO/content/newsletter/partnerships.

## What Still Needs To Be Done

1. **Fill the audit template with actual data** — the financial model uses placeholder defaults (ACV $12K, etc.). Replace with real pricing/conversion/churn numbers.
2. **Pick target launch states** — blueprint suggests starting with IL + NJ. Confirm and validate compliance requirements.
3. **Start affiliate applications** — BetMGM and Caesars have the most public/accessible programs. bet365 is also straightforward.
4. **Select odds/stats vendors** — The Odds API for MVP odds data; decide on stats providers (free open-source first, then paid).
5. **Build MVP** — Phase 1 in the roadmap (Weeks 3–8): odds display, line movement charts, strategy templates, bet slip generator + deep links.
6. **Insert chat transcripts** into the `3_year_acquisition_roadmap_package.md` appendix (placeholders are there).
7. **Design dashboards and event taxonomy** per the KPI one-pager.
8. **Validate all compliance details with gaming counsel** — the blueprint explicitly notes this is not legal advice.

---

## Key Technical Decisions to Make

| Decision | Options / Notes |
|----------|----------------|
| Backend framework | Python (FastAPI) recommended — aligns with ML/backtest tooling (pandas, numpy, numba) |
| Odds data provider | The Odds API (transparent pricing, good for MVP) vs. Genius Sports (enterprise, low-latency) |
| Stats data sources | Start with free: pybaseball (MLB), nflfastR (NFL), nba_api (NBA), FastF1 (F1). Graduate to Sportradar/Opta at scale. |
| Geo-compliance | GeoComply-like approach for location verification + IP fallback. Never IP-only for wagering context. |
| Auth | Passkeys + OAuth recommended |
| Hosting | Not yet decided — typical options: Vercel (frontend) + Railway/Render/AWS (backend) |

---

## How To Use This Package

1. Read `sports_betting_affiliate_ai_blueprint__1_.md` first — it's the master document.
2. Read `Next_Gen_Sports_Tracking_Data_Guide.md` for data sourcing decisions.
3. Review the financial model files (`assumptions.csv`, `monthly_*.csv`, etc.) to understand the default projections.
4. Follow the "What Still Needs To Be Done" list above to pick up where things left off.
