# Session Handoff — College Baseball Valuations B2B SaaS

> **Date:** 2026-02-16
> **Purpose:** Continue work in a new Claude Code window. This file captures everything done in the previous session so the new session can pick up where we left off.

---

## What Was Done This Session

### 1. Financial Model Built (`financial-model.md`)

Complete 36-month financial model for a college baseball player valuations B2B SaaS ("the PFF of college baseball"). Includes:

- **All assumptions** — ACV $12K, 87% gross margin, 2%/3%/4% churn scenarios, $1K/mo budget, zero hires
- **TAM/SAM/SOM** — $3.6M SAM (300 D1 programs x $12K), realistic SOM 95-115 programs
- **Customer acquisition model** — 3 channels: content/organic (60-70%), paid ads (10-15%), outbound (20-25%)
- **36-month revenue projection** — Month-by-month Y1, quarterly Y2-3. Ends at ~54 customers, $653K ARR (base case)
- **Full P&L** — Revenue, COGS, gross profit, OpEx, net income, cumulative cash. Cash-positive Month 7
- **Unit economics** — LTV $43,500, CAC ~$1,600, LTV:CAC 27x, payback 1.8 months
- **Churn scenarios** — Business works at 2%, 3%, and 4% monthly churn
- **Sensitivity analysis** — Customer acquisition rate and pricing are highest-leverage variables

### 2. CDO 20-Agent Analysis (`cdo-20-agent-analysis.md` + `.pdf`)

20 independent expert perspectives across 5 agent groups (no group saw another's work). Perspectives:

**Group 1 — Financial:** CFO, VC/Investor, Pricing Strategist, Exit/M&A Advisor
**Group 2 — Buyer:** College Baseball Coach, Athletic Director, Industry Insider, Market Sizing Skeptic
**Group 3 — GTM:** B2B Sales Expert, Content Marketing Strategist, Paid Ads Specialist, Growth Hacker
**Group 4 — Product:** Data Scientist, Product Strategist, Competitive Intel, StatsBomb Analyst
**Group 5 — Risk:** Churn Analyst, Risk Analyst, Legal/Compliance, Bootstrapped SaaS Founder

**Overall Verdict:** CONDITIONAL GO (0.65 confidence). 16 conditional go, 2 go, 2 no-go (on VC funding and paid ads specifically).

### Top 10 Conditions from the Analysis

1. **Secure data license for Baseball Savant** — existential risk, flagged by 4 independent groups
2. **Model churn at 3-3.5%** — not 2% (coaching turnover)
3. **Implement tiered pricing** — $6K Scout / $15K Pro / $25K Elite
4. **Build scouting report generator** (workflow tool), not a dashboard
5. **Pursue conference-level deals** — sell to SEC, not 14 programs individually
6. **Plan first hire at $300K ARR** — solo ceiling at 35-45 customers
7. **Redirect paid ads to ABCA convention** and in-person events
8. **Pre-sell before building** — validate with LOIs from 5-10 coaches
9. **18-24 month competitive window** — before Hudl/Teamworks enter
10. **Don't anchor to StatsBomb comparison** — borrow data-moat tactic, use PFF brand strategy

---

## Files in the Repo

| File | What It Is | Status |
|------|------------|--------|
| `financial-model.md` | 36-month financial model | BUILT this session |
| `cdo-20-agent-analysis.md` | 20-agent CDO analysis | BUILT this session |
| `cdo-20-agent-analysis.pdf` | PDF version of above | BUILT this session |
| `pressure-test-notes.md` | Phase roadmap and open questions | FROM BEFORE — the master plan |
| `sports-analytics-evaluation.md` | Full business evaluation with market data | FROM BEFORE — key reference |
| `3yr_launch_customer_acquisition_report.md` | Original template (now superseded by financial-model.md) | FROM BEFORE — replaced |
| `session-handoff.md` | This file | BUILT this session |

Other files in repo (CFC streetwear brand — separate project, not active):
- `CFC-MASTER-ORCHESTRATOR.md`, `AGENT-01-OPSEC.md`, `AGENT-02-SOURCING.md`, `AGENT-03-KICKSTARTER.md`
- `CFC-LEVIATHAN-ITERATION-1.md`, `CFC-STRESS-TEST-ITERATION-2.md` + `.pdf`

---

## Phase Status (from pressure-test-notes.md)

| Phase | Status | What's Left |
|-------|--------|-------------|
| Phase 1: Fix the Foundation | **COMPLETE** | Financial model built. Churn scenarios run. TAM/SAM/SOM added. 20-agent analysis complete. |
| Phase 2: Design the Product | **NOT STARTED** | Define composite model, mock up player profile, decide data product vs. workflow tool (answered: workflow tool / scouting report generator), map buyer journey |
| Phase 3: Build the Free Tool | **NOT STARTED** | Data ingestion pipeline, composite valuation model, public website with rankings, content distribution setup |
| Phase 4: Validate With Buyers | **NOT STARTED** | Cold outreach to 10 coaches, collect feedback, iterate |

---

## Top 5 Action Items (Next Session)

1. **Read Baseball Savant ToS** — Check if commercial use of Statcast data requires a license. This is the #1 blocker.
2. **Mock up the scouting report** — One page: player name, composite score, key stats, competition-adjusted projections, comparable players. This is the MVP product.
3. **Design tiered pricing page** — Scout ($6K) / Pro ($15K) / Elite ($25K) with feature breakdown.
4. **Map the buyer journey** — Who finds you → who evaluates → who approves → who signs. Include seasonal timing windows.
5. **Build a pre-sell pitch deck** — 5-10 slides for showing to coaches before building anything.

---

## Key Decision Made

**Data product vs. workflow tool?** DECIDED: **Workflow tool that produces a data product.** Specifically, a scouting report generator that produces one-page PDF reports coaches can pull up during recruiting calls. Not a dashboard. Not charts. Answers.

---

## Memory File

Auto-memory is stored at `/home/john/.claude/projects/-home-john-cfc/memory/MEMORY.md` and will persist across sessions automatically.

---

## How to Continue

Open a new Claude Code window and say:

```
Read session-handoff.md for full context on what we've done. Then let's start Phase 2: Design the Product. First task: mock up the scouting report (the MVP).
```

---

*Session handoff created: 2026-02-16*
