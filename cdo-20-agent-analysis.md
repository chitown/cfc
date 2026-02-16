# CDO 20-Agent Analysis — College Baseball Valuations B2B SaaS

> **Method:** 20 independent expert perspectives across 5 agent groups. No group saw another's work during analysis. This prevents groupthink — convergent findings across independent groups are high-signal.
> **Date:** 2026-02-16

---

## Final Verdict: CONDITIONAL GO

**Composite confidence: 0.65**

| Verdict | Count | Perspectives |
|---------|-------|-------------|
| GO | 2 | Athletic Director, Growth Hacker |
| CONDITIONAL GO | 16 | CFO, Pricing, Exit/M&A, Coach, Industry Insider, Market Skeptic, B2B Sales, Content Marketing, Data Scientist, Product Strategist, Competitive Intel, StatsBomb Analyst, Churn Analyst, Risk Analyst, Legal, Bootstrapped Founder |
| NO-GO | 2 | VC/Investor (as venture investment), Paid Ads Specialist (on ads specifically) |

**What "Conditional GO" means:** The business fundamentals are sound. The unit economics are strong. The market gap is real. But there are specific conditions that must be met — and several of them surfaced independently across multiple agent groups, which means they're real, not noise.

---

## The 10 Conditions (Ranked by How Many Independent Groups Flagged Them)

### 1. Secure a data license for Baseball Savant / Statcast (Flagged by 4 groups)

**Who flagged it:** Legal, Risk Analyst, Data Scientist, CFO

This is the single most important pre-condition. Baseball Savant is publicly accessible but "publicly accessible" does not mean "commercially licensable." MLB's Terms of Service almost certainly prohibit commercial scraping without authorization. If MLB sends a cease-and-desist, the product ceases to exist.

**What to do:** Read the actual Baseball Savant Terms of Service. Consult an IP attorney about whether composite scores derived from raw data qualify as transformative use. Ideally, seek a written data license from MLB. Even a low-cost license becomes a competitive moat — most competitors won't bother navigating the licensing process for a market this small.

**If you can't get a license:** The product must be architecturally designed to work without Statcast as the sole data source. Build a source-agnostic data pipeline from day one that can ingest TrackMan, Rapsodo, and manual entry.

---

### 2. Adjust the churn assumption to 3-3.5% monthly (Flagged by 3 groups)

**Who flagged it:** Churn Analyst, CFO, Bootstrapped Founder

The 2% monthly churn assumption is optimistic. College coaching staffs turn over at 15-25% annually. When a head coach leaves, the new staff doesn't inherit SaaS subscriptions with loyalty. The Churn Analyst estimates coaching turnover alone drives ~0.8-1.0% monthly churn before any other factors.

**Realistic churn:** 3-3.5% monthly. The business still works at this rate (already modeled in the financial model), but the Year 3 ARR drops from $653K to approximately $550-585K.

**How to improve churn:** Sell to the program, not the coach. Get the athletic department to own the contract. Build features that create institutional value (historical data archives, trend reports that compound over time). If the product becomes "how we do recruiting analysis here" rather than "that tool Coach Johnson liked," it survives coaching transitions.

---

### 3. Implement tiered pricing from day one (Flagged by 3 groups)

**Who flagged it:** Pricing Strategist, Bootstrapped Founder, Athletic Director

$12K flat pricing leaves significant money on the table and signals "budget tool" to premium buyers.

**Recommended tiers:**

| Tier | Price | What's Included | Target |
|------|-------|-----------------|--------|
| Scout | $6K/year | Composite scores, basic search, conference-level data | Budget-constrained programs, land-and-expand entry point |
| Pro | $15K/year | Full valuations, transfer portal intelligence, comparison tools, scouting reports | Serious programs (your core) |
| Elite | $25-30K/year | Everything + custom reports, API access, monthly analyst call, early access | SEC/ACC/Big 12 programs with large budgets |

**Why this matters:** A tiered model creates a conversation about "which tier" instead of "yes or no." It captures more willingness-to-pay from well-funded programs. And the anchor effect of a $25-30K Elite tier makes $15K Pro look reasonable. This could push average ACV from $12K to $16-18K, which is worth $120-180K in additional ARR at 54 customers.

---

### 4. Build a scouting report workflow tool, not a data dashboard (Flagged by 3 groups)

**Who flagged it:** Product Strategist, Coach, Data Scientist

This is the key product decision. Coaches don't want dashboards and charts. They want answers during a 72-hour transfer portal window when they're evaluating 40 names at 11pm.

**The MVP should be brutally narrow:** A scouting report generator. Coach enters a player name (or uploads a TrackMan CSV), the system pulls all available public stats, combines them with any uploaded data, and produces a one-page PDF scouting report with a composite score and comparable players. That's the product a coach pulls up on a recruiting call.

**Stickiness comes from three things:**
1. Historical data accumulation — the longer a program uses it, the more proprietary data lives in the system
2. Staff workflow habits — once assistants are trained on generating reports this way, inertia is powerful
3. Recruit tracking — becomes a lightweight CRM with data superpowers

**The coach said it plainly:** "I don't need something that tells me what I can already see. I need the 'so what' — projected performance in my conference, injury risk flags, and how this kid compares to players I already know."

---

### 5. Pursue conference-level deals as the primary growth accelerant (Flagged by 2 groups)

**Who flagged it:** Growth Hacker, Industry Insider

This is the single biggest strategic unlock that isn't in the current plan. Don't sell to 300 individual programs — sell to 10 conferences. The SEC, ACC, Big 12, Big Ten each have conference offices that can mandate or subsidize tools for member schools.

**Why this changes everything:** One SEC conference deal replaces 14 individual sales. If the SEC adopts, every non-SEC program needs it to keep up (competitive pressure). Conference offices care about competitive balance — if half their programs have a tool the other half lacks, they'll negotiate group access.

**How it works in practice:** Land 3-4 programs in the same conference through individual sales. Then approach the conference office with a group licensing proposal. Conferences have precedent for this (Catapult, Teamworks have conference-wide deals). This is the volume play that transforms a 300-program-at-a-time grind into a 14-programs-at-once motion.

---

### 6. Plan the first hire at $300K ARR / 30-35 customers (Flagged by 2 groups)

**Who flagged it:** Bootstrapped Founder, Risk Analyst

The solo founder model collapses between 35-45 customers. At that point, you're spending 60% of your time on support and account management, leaving 40% for everything else. Product development slows to a crawl. Content creation — your primary acquisition channel — drops off. New customer acquisition stalls.

**Plan for this transition at $300K ARR (roughly Month 18-20):**
- Part-time customer success / support person: ~$30-40K/year
- Part-time content creator: ~$30-40K/year
- Total new cost: $60-80K/year, easily covered at $300K+ ARR

The business can afford this. The founder needs to plan for it proactively, not wait until they're drowning.

---

### 7. Redirect paid ad budget to conferences and in-person events (Flagged by 2 groups)

**Who flagged it:** Paid Ads Specialist, Growth Hacker

The Paid Ads Specialist was the most definitive NO-GO in the entire analysis: "$150 CPL is unrealistic for this niche on most platforms."

- **LinkedIn:** Can't target "college baseball coach" with precision. Audience too broad. CPLs run $200-500 for niche B2B
- **Google Ads:** No meaningful search volume for "college baseball analytics software"
- **Facebook/Instagram:** Only useful for retargeting free tool users (Year 2+)

**Better use of that $300-500/month:**
- ABCA convention demo booth (~$2-3K, face time with 200+ coaches in one weekend)
- Regional coaching clinics
- Summer league partnerships (Cape Cod League coaches are often D1 assistants or future head coaches)
- Save paid ads budget for Year 2 retargeting once you have meaningful free tool traffic

---

### 8. Pre-sell before building (Flagged by 2 groups)

**Who flagged it:** Bootstrapped Founder, Market Sizing Skeptic

Don't build the product first. Go to 10 programs with mockups and a pitch deck. Get 3-5 letters of intent or prepaid annual contracts. Then build. This validates demand and funds development.

The Market Sizing Skeptic was blunt: the realistic addressable market may be 95-115 programs (not 300) once you subtract programs that can't afford it, don't believe in analytics, have built internal solutions, or will just have a grad student do it in Python.

Pre-selling answers the most important question before you invest months of building: will coaches actually pay for this?

---

### 9. The competitive window is 18-24 months (Flagged by 2 groups)

**Who flagged it:** Competitive Intelligence, StatsBomb Analyst

Hudl (344K team relationships, just acquired StatsBomb) and Teamworks Intelligence ($1B+ valuation, ML-based player evaluation) are the real threats. The realistic timeline before one of them enters college baseball analytics is 18-24 months.

In that window, you need to achieve two things:
1. Brand recognition as "the" college baseball valuation source
2. Enough data integration (coach uploads) to create switching costs

**The irony:** Your most likely successful exit (acquisition by Hudl or Teamworks) is also the source of your most likely competitive threat. If they decide to build rather than buy, the 300-program TAM is too small to sustain an independent fight.

---

### 10. Don't anchor to the StatsBomb comparison (Flagged by 1 group, but high confidence)

**Who flagged it:** StatsBomb Case Study Analyst (0.70 confidence)

The StatsBomb comparison is "seductive and mostly misleading." What breaks:
- StatsBomb had ~500+ global buyers across clubs, media, betting, federations. You have ~300 domestic programs
- StatsBomb created entirely new data (human event tagging). You're synthesizing existing data
- StatsBomb had 4 revenue streams. You have 1

**What to borrow:** The insight that data integration/synthesis is a stronger moat than algorithmic sophistication. Build the platform where fragmented private data gets synthesized into something greater than the sum of its parts.

**Better comparison:** PFF in its first 3 years (2006-2009) — small niche product that became the common language. PFF didn't win on model sophistication. It won on brand. If coaches start saying "he's a 74 on [your platform]," you own the market.

---

## The 20 Perspectives — Scorecard

| # | Role | Group | Verdict | Confidence |
|---|------|-------|---------|------------|
| 1 | CFO / Financial Analyst | Financial | CONDITIONAL GO | 0.72 |
| 2 | VC / Investor | Financial | NO-GO (VC) / GO (Bootstrap) | 0.85 |
| 3 | Pricing Strategist | Financial | CONDITIONAL GO | 0.68 |
| 4 | Exit / M&A Advisor | Financial | CONDITIONAL GO | 0.60 |
| 5 | College Baseball Head Coach | Buyer | CONDITIONAL GO | 0.60 |
| 6 | Athletic Director | Buyer | GO | 0.70 |
| 7 | College Athletics Industry Insider | Buyer | CONDITIONAL GO | 0.55 |
| 8 | Market Sizing Skeptic | Buyer | CONDITIONAL GO | 0.50 |
| 9 | B2B SaaS Sales Expert | GTM | CONDITIONAL GO | 0.65 |
| 10 | Content Marketing Strategist | GTM | CONDITIONAL GO | 0.60 |
| 11 | Paid Ads Specialist | GTM | NO-GO (on ads) | 0.75 |
| 12 | Growth Hacker | GTM | GO | 0.72 |
| 13 | Data Scientist / ML Engineer | Product | CONDITIONAL GO | 0.60 |
| 14 | Product Strategist | Product | CONDITIONAL GO | 0.70 |
| 15 | Competitive Intelligence Analyst | Product | CONDITIONAL GO | 0.55 |
| 16 | StatsBomb Case Study Analyst | Product | CONDITIONAL GO | 0.70 |
| 17 | Churn Analyst | Risk | CONDITIONAL GO | 0.72 |
| 18 | Risk Analyst | Risk | CONDITIONAL GO | 0.65 |
| 19 | Legal / Compliance | Risk | CONDITIONAL GO | 0.58 |
| 20 | Bootstrapped SaaS Founder | Risk | CONDITIONAL GO | 0.75 |

---

## Key Convergent Findings (Multiple Independent Groups Agreed)

These findings are high-signal because they emerged independently from groups that couldn't see each other's work:

| Finding | Groups That Independently Converged | Implication |
|---------|--------------------------------------|-------------|
| Data licensing is existential | Financial, Product, Risk | Must resolve BEFORE building |
| 2% churn is optimistic | Financial, Buyer, Risk | Re-model at 3-3.5% |
| Price higher / add tiers | Financial, Buyer, Risk | Could add $120-180K ARR |
| Build workflow tool, not dashboard | Buyer, Product, GTM | Changes the entire product roadmap |
| Conference deals are the unlock | Buyer, GTM | Not in current plan but could transform trajectory |
| Solo founder ceiling at 35-45 | Financial, Risk | Plan the hire, don't react to the crisis |
| Transfer portal is THE moment | Buyer, GTM, Product | All content and product decisions should center here |
| Paid ads won't work for this niche | GTM (high confidence) | Redirect budget to conferences and events |

---

## What Changes in the Financial Model

Based on the 20-agent analysis, the financial model should be updated:

| Parameter | Current Model | Recommended Update | Impact |
|-----------|--------------|-------------------|--------|
| Base churn | 2% monthly | 3.5% monthly | Y3 ARR drops ~$100K |
| ACV | $12,000 flat | $6K/$15K/$25K tiered, ~$16K blended | Y3 ARR increases ~$130K |
| Paid ads budget | $300-1,500/mo | $0 Y1, retargeting only Y2+ | Saves ~$4K Y1 |
| Conference/events | $200/mo | $500/mo (incl. ABCA booth) | Costs ~$3.6K more Y1 |
| First hire | Not modeled | $60-80K/yr starting Month 18-20 | Reduces net income Y2-3 |
| Realistic SAM | 300 programs | 95-115 programs Y1-3 | Changes penetration math |
| Sales cycle | 2 months | 3-4 months (fiscal year timing) | Shifts first customer to M6-7 |

**Net effect:** The optimistic case gets a haircut (~15-20% lower ARR) but the business still works. The revised model would show roughly $550K ARR at Month 36 with better risk-adjusted assumptions.

---

## Top 5 Action Items (In Priority Order)

1. **Read Baseball Savant Terms of Service and consult an IP attorney** — This is a potential showstopper. Do it this week.

2. **Pre-sell to 5-10 coaches with mockups** — Validate demand before investing months in building. Get letters of intent or prepaid contracts.

3. **Build the scouting report generator as the MVP** — Not a dashboard. A one-page PDF that a coach pulls up on a recruiting call.

4. **Implement tiered pricing** — Scout ($6K), Pro ($15K), Elite ($25K). Higher blended ACV with lower barrier to entry.

5. **Book a booth at the ABCA convention** — One weekend replaces 6 months of online outreach. This is the single highest-ROI event for this market.

---

## Divergent Findings (Where Perspectives Disagreed)

| Topic | Perspective A | Perspective B | Who's Right? |
|-------|--------------|---------------|-------------|
| Market size | Market Skeptic: 95-115 realistic buyers | AD: $12K is trivial for most D1 budgets | Both — the market IS smaller than 300, but the budget objection IS minimal for most programs |
| StatsBomb relevance | StatsBomb Analyst: Mostly misleading | Data Scientist: The data-moat insight transfers | The TACTIC transfers (build a unique dataset), the ECONOMICS don't (smaller market, single revenue stream) |
| Content vs. outbound in Y1 | Content Marketing: Content is king | B2B Sales: Y1 should be 50%+ outbound | B2B Sales is right for Y1 — content compounds over time but outbound gets you first customers faster |
| Exit potential | Exit/M&A: 3-6x ARR ($2-4M) | VC: Not venture-scale, don't even try | Both are right — this is a great bootstrap, not a venture play. $2-4M exit or $300-500K/yr lifestyle business. Both are excellent outcomes |

---

*CDO 20-Agent Analysis completed: 2026-02-16*
*5 independent agent groups, zero cross-contamination*
*Synthesis performed after all agents completed*
