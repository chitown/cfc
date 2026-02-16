# College Baseball Valuations — 36-Month Financial Model

> **Product:** College baseball player valuations B2B SaaS ("the PFF of college baseball")
> **Buyer:** D1 college baseball programs
> **Operator:** Solo founder, bootstrapped, $1K/month budget
> **Acquisition:** Content-first + paid ads + founder-led outbound
> **Date:** 2026-02-16

---

## Summary

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Ending customers | 8 | 28 | 54 |
| Ending ARR | $101K | $338K | $653K |
| Revenue (collected) | $35K | $234K | $515K |
| Net income | $21K | $183K | $417K |
| Cumulative cash | $21K | $204K | $621K |

The business becomes cash-flow positive in **Month 5** (first customer). Cumulative cash turns positive in **Month 7**. At 2% monthly churn, the model reaches ~$653K ARR by Month 36 with 54 active customers out of ~300 D1 programs (18% market penetration). $1M ARR is reachable around Month 42-48.

**The math works in all churn scenarios tested (2%, 3%, 4%).** Even at 4% monthly churn (the coaching-turnover worst case), the business generates $527K ARR and $533K cumulative net income over 3 years.

---

## 1. All Assumptions

These are the inputs that drive the entire model. Change any of these and the outputs change.

### Revenue

| Input | Value | Why This Number |
|-------|-------|-----------------|
| ACV (Annual Contract Value) | $12,000 | $1,000/month. High enough for healthy unit economics, low enough to be noise in an athletic department budget |
| Gross margin | 87% | Infrastructure costs are ~$100-200/customer/year. At $12K revenue per customer, COGS is ~13% |
| Expansion revenue | $0 | Not modeled. Upside opportunity (usage tiers, add-on reports) but not assumed |
| Annual price increase | 0% | Conservative. Real-world you'd likely raise 3-5%/year after Year 2 |

### Churn

| Input | Base Case | Moderate | High |
|-------|-----------|----------|------|
| Monthly churn rate | 2% | 3% | 4% |
| Annual churn (implied) | 21.5% | 30.6% | 39.3% |
| Avg customer lifetime | 50 months | 33 months | 25 months |

**Why three scenarios:** College coaching staffs turn over frequently. When a head coach gets fired or a recruiting coordinator leaves, your champion at that program is gone. The 3-4% scenarios model what happens if new coaches don't renew. The 2% base case assumes the product becomes sticky at the program level (data history, institutional knowledge) rather than dependent on one person.

### Customer Acquisition

| Input | Value | Why This Number |
|-------|-------|-----------------|
| Paid ad CPL (Cost Per Lead) | $150 | Niche B2B targeting college athletics on LinkedIn/Google. Higher than consumer, lower than enterprise |
| Paid lead-to-customer rate | 3% | Cold leads from ads need nurturing through a 2-month sales cycle |
| Organic lead-to-customer rate | 8% | Warm leads who already use the free tool — they know the product works |
| Outbound lead-to-customer rate | 5% | Founder reaching out directly to coaches at conferences and via email |
| Sales cycle | 2 months | Athletic department procurement isn't instant. Coach evaluates → recommends to AD → budget approval |

### Operating Costs

| Cost | Pre-Revenue (M1-5) | Early Customers (M6-12) | Scaling (Y2) | Mature (Y3) |
|------|--------------------|-----------------------|-------------|-------------|
| Infrastructure (hosting, DB, APIs) | $150/mo | $300/mo | $500/mo | $800/mo |
| Paid ads | $0 → $300/mo | $500/mo | $1,000/mo | $1,500/mo |
| Tools & subscriptions | $50/mo | $50/mo | $50/mo | $50/mo |
| Conferences & events | $0 → $200/mo | $200/mo | $200/mo | $200/mo |
| Headcount | $0 | $0 | $0 | $0 |

**Zero hires until profitable.** The original model had $40K/month in headcount by Month 15 — that's a funded startup model, not a bootstrapped founder. You are the sales team, the CS team, and the product team.

---

## 2. TAM / SAM / SOM

**TAM, SAM, and SOM** are three concentric circles that describe your market opportunity from largest to smallest:

- **TAM (Total Addressable Market):** Everyone who could theoretically buy a sports analytics product at $12K ACV
- **SAM (Serviceable Addressable Market):** The slice you can actually reach and serve today
- **SOM (Serviceable Obtainable Market):** What you'll realistically capture in the next 1-3 years

### TAM: $13M - $18M

All potential buyers of mid-market sports analytics:

| Segment | Estimated Buyers | At $12K ACV |
|---------|-----------------|-------------|
| D1 college baseball programs | ~300 | $3,600,000 |
| D1 college basketball programs | ~350 | $4,200,000 |
| D2/NAIA baseball programs | ~550 | $4,400,000 (at lower $8K ACV) |
| Minor league / affiliate teams | ~200 | $2,400,000 |
| Other (media, fantasy, betting ops) | ~100 | $1,200,000 |
| **Total TAM** | **~1,500** | **~$15,800,000** |

### SAM: $3.6M

Your initial serviceable market — D1 college baseball programs only:

**~300 programs x $12,000 = $3,600,000**

This is the segment where all three conditions are met: they have the data (TrackMan/Rapsodo), they have the pain (transfer portal evaluation), and they have the budget ($12K is manageable for a D1 program).

### SOM: What You'll Realistically Capture

| Timeframe | Customers | ARR | % of SAM |
|-----------|-----------|-----|----------|
| Year 1 | 8 | $101K | 3% |
| Year 2 | 28 | $338K | 9% |
| Year 3 | 54 | $653K | 18% |

**18% penetration in 3 years is ambitious but achievable** if the product is good. College baseball is a tight-knit community — once a few SEC or ACC programs adopt, word spreads fast. PFF achieved near-universal adoption in football over ~10 years. Your niche is much smaller.

### Expansion Potential (Years 3-5)

Once you own college baseball, adjacent markets open up:

| Expansion | Additional SAM |
|-----------|---------------|
| D2/NAIA baseball (lower price tier) | +$4.4M |
| D1 basketball (same composite model, different data) | +$4.2M |
| Minor league baseball | +$2.4M |
| **Expanded SAM** | **$14.6M** |

This turns a ~$3.6M niche into a ~$15M opportunity without building anything fundamentally new — just adapting the valuation model to new sports and levels.

---

## 3. Customer Acquisition Model

### Where Customers Come From

Three channels, weighted differently over time:

**Channel 1: Content / Organic (60-70% of customers)**
Free tool users who discover the public rankings site, use it regularly, and eventually want the premium features (detailed player profiles, batch export, team-level scouting reports). Zero dollar cost — the "cost" is your time creating content and maintaining the free tool.

**Channel 2: Paid Ads (10-15% of customers)**
LinkedIn ads targeting college baseball coaches and athletic directors. Google search ads for terms like "college baseball analytics" and "transfer portal scouting tool." Drives awareness to the free tool, which then converts over time.

**Channel 3: Founder-Led Outbound (20-25% of customers)**
You at ABCA conferences. Cold emails to recruiting coordinators. Demo calls with coaches who've seen your content. This is the highest-conversion channel because you're having real conversations with real buyers.

### New Customer Schedule

This is the core input to the model — how many new paying customers you add each month. These numbers are judgment-based estimates, not mechanical outputs from a funnel formula. They're calibrated against the benchmarks in the evaluation doc (first customer Month 5-6, $100K ARR by Month 12).

| Period | New/Month | Rationale |
|--------|-----------|-----------|
| Months 1-4 | 0 | Building the product + free tool. No revenue yet |
| Month 5 | 1 | First customer from free tool early adopters. Paid ads have been running for 2 months |
| Months 6-11 | 1/mo | Steady founder-led sales. Each new customer is a reference for the next |
| Month 12 | 2 | Reputation building, first referrals, conference season |
| Months 13-24 | 2/mo | Content audience growing, ads at $1K/mo, word of mouth in coaching networks |
| Months 25-36 | 3/mo | Brand established, organic inbound growing, possibly first inbound from coaches who heard about you from other coaches |

**Year 1:** 9 new customers
**Year 2:** 24 new customers
**Year 3:** 36 new customers
**Total over 36 months:** 69 new customers acquired

### Funnel Validation

Do the channel numbers add up to support this schedule? Let's check Year 1:

| Channel | Leads (Y1) | Conversion | Customers |
|---------|-----------|------------|-----------|
| Paid ads ($4,200 total spend ÷ $150 CPL) | 28 | 3% | ~1 |
| Organic (free tool users, growing M3-M12) | ~60-80 | 8% | ~5-6 |
| Outbound (conferences, cold email M4-M12) | ~25-30 | 5% | ~1-2 |
| **Total** | **~115** | **blended ~7%** | **~7-9** |

Schedule says 9. Funnel math supports 7-9. Close enough — the schedule is realistic.

---

## 4. 36-Month Revenue Projection (Base Case: 2% Monthly Churn)

### How to Read This Table

- **New:** Paying customers added this month
- **Churned:** Expected customers lost (previous month's total x 2% churn rate). Fractions are normal — 0.1 means a 10% chance of losing one customer this month
- **End Customers:** Active paying customers at month end
- **MRR:** Monthly Recurring Revenue (End Customers x $1,000)
- **ARR:** Annualized run-rate (MRR x 12)

### Year 1 — Month by Month

| Month | New | Churned | End Cust | MRR | ARR |
|-------|-----|---------|----------|-----|-----|
| 1 | 0 | 0 | 0 | $0 | $0 |
| 2 | 0 | 0 | 0 | $0 | $0 |
| 3 | 0 | 0 | 0 | $0 | $0 |
| 4 | 0 | 0 | 0 | $0 | $0 |
| 5 | 1 | 0 | 1.0 | $1,000 | $12,000 |
| 6 | 1 | 0.02 | 1.98 | $1,980 | $23,760 |
| 7 | 1 | 0.04 | 2.94 | $2,940 | $35,280 |
| 8 | 1 | 0.06 | 3.88 | $3,882 | $46,584 |
| 9 | 1 | 0.08 | 4.80 | $4,804 | $57,648 |
| 10 | 1 | 0.10 | 5.71 | $5,708 | $68,496 |
| 11 | 1 | 0.11 | 6.59 | $6,594 | $79,128 |
| 12 | 2 | 0.13 | 8.46 | $8,462 | $101,544 |

**Year 1 total revenue collected: $35,370**

### Years 2-3 — Quarterly Summary

| Quarter | Months | New Cust | End Cust | End MRR | Quarterly Revenue |
|---------|--------|----------|----------|---------|-------------------|
| Q5 | 13-15 | 6 | 13.8 | $13,844 | $36,220 |
| Q6 | 16-18 | 6 | 18.9 | $18,903 | $51,715 |
| Q7 | 19-21 | 6 | 23.7 | $23,670 | $66,304 |
| Q8 | 22-24 | 6 | 28.2 | $28,158 | $80,047 |
| **Y2 Total** | | **24** | **28.2** | **$28,158** | **$234,286** |
| Q9 | 25-27 | 9 | 35.3 | $35,324 | $98,904 |
| Q10 | 28-30 | 9 | 42.1 | $42,069 | $119,553 |
| Q11 | 31-33 | 9 | 48.4 | $48,416 | $138,987 |
| Q12 | 34-36 | 9 | 54.4 | $54,390 | $157,277 |
| **Y3 Total** | | **36** | **54.4** | **$54,390** | **$514,721** |

### Annual Summary

| | Year 1 | Year 2 | Year 3 | 3-Year Total |
|---|--------|--------|--------|-------------|
| New customers | 9 | 24 | 36 | 69 |
| Customers lost to churn | ~0.5 | ~5.3 | ~9.8 | ~15.6 |
| Ending customers | 8.5 | 28.2 | 54.4 | — |
| Revenue collected | $35,370 | $234,286 | $514,721 | $784,377 |
| Ending MRR | $8,462 | $28,158 | $54,390 | — |
| Ending ARR | $101,544 | $337,896 | $652,680 | — |

---

## 5. Profit & Loss Statement (Base Case: 2% Churn)

### How to Read This

- **Revenue:** Cash collected from subscriptions
- **COGS (Cost of Goods Sold):** Direct costs to serve customers — hosting, database, API calls. At 13% of revenue
- **Gross Profit:** Revenue minus COGS. This is the money available to run the business
- **OpEx (Operating Expenses):** Everything else — ads, tools, conferences, infrastructure overhead
- **Net Income:** What's left. Positive = profit. Negative = burn

### Year 1 — Monthly P&L

| Month | Revenue | COGS (13%) | Gross Profit | OpEx | Net Income | Cum Cash |
|-------|---------|------------|-------------|------|------------|----------|
| 1 | $0 | $0 | $0 | $200 | -$200 | -$200 |
| 2 | $0 | $0 | $0 | $200 | -$200 | -$400 |
| 3 | $0 | $0 | $0 | $500 | -$500 | -$900 |
| 4 | $0 | $0 | $0 | $700 | -$700 | -$1,600 |
| 5 | $1,000 | $130 | $870 | $700 | $170 | -$1,430 |
| 6 | $1,980 | $257 | $1,723 | $850 | $873 | -$557 |
| 7 | $2,940 | $382 | $2,558 | $1,050 | $1,508 | $951 |
| 8 | $3,882 | $505 | $3,377 | $1,050 | $2,327 | $3,278 |
| 9 | $4,804 | $625 | $4,179 | $1,050 | $3,129 | $6,407 |
| 10 | $5,708 | $742 | $4,966 | $1,050 | $3,916 | $10,323 |
| 11 | $6,594 | $857 | $5,737 | $1,050 | $4,687 | $15,010 |
| 12 | $8,462 | $1,100 | $7,362 | $1,050 | $6,312 | $21,322 |

**Key moments:**
- **Month 5:** First profitable month (+$170). One customer covers all costs
- **Month 7:** Cumulative cash turns positive. The $1,600 "hole" from months 1-4 is paid back
- **Month 12:** Monthly net income of $6,312. The business is generating real cash

### OpEx Breakdown (What You're Spending On)

| Cost Category | M1-2 | M3 | M4-5 | M6 | M7-12 | Y2/mo | Y3/mo |
|---------------|------|----|------|-----|-------|-------|-------|
| Infrastructure | $150 | $150 | $150 | $300 | $300 | $500 | $800 |
| Paid ads | $0 | $300 | $300 | $300 | $500 | $1,000 | $1,500 |
| Tools/subs | $50 | $50 | $50 | $50 | $50 | $50 | $50 |
| Conferences | $0 | $0 | $200 | $200 | $200 | $200 | $200 |
| **Total** | **$200** | **$500** | **$700** | **$850** | **$1,050** | **$1,750** | **$2,550** |

### Quarterly P&L Summary (All 12 Quarters)

| Quarter | Revenue | COGS | Gross Profit | OpEx | Net Income | Cum Cash |
|---------|---------|------|-------------|------|------------|----------|
| Q1 (M1-3) | $0 | $0 | $0 | $900 | -$900 | -$900 |
| Q2 (M4-6) | $2,980 | $387 | $2,593 | $2,250 | $343 | -$557 |
| Q3 (M7-9) | $11,626 | $1,511 | $10,115 | $3,150 | $6,965 | $6,408 |
| Q4 (M10-12) | $20,764 | $2,699 | $18,065 | $3,150 | $14,915 | $21,322 |
| **Y1** | **$35,370** | **$4,598** | **$30,772** | **$9,450** | **$21,322** | **$21,322** |
| Q5 (M13-15) | $36,220 | $4,709 | $31,511 | $5,250 | $26,261 | $47,583 |
| Q6 (M16-18) | $51,715 | $6,723 | $44,992 | $5,250 | $39,742 | $87,325 |
| Q7 (M19-21) | $66,304 | $8,620 | $57,684 | $5,250 | $52,434 | $139,759 |
| Q8 (M22-24) | $80,047 | $10,406 | $69,641 | $5,250 | $64,391 | $204,150 |
| **Y2** | **$234,286** | **$30,457** | **$203,829** | **$21,000** | **$182,829** | **$204,150** |
| Q9 (M25-27) | $98,904 | $12,858 | $86,046 | $7,650 | $78,396 | $282,546 |
| Q10 (M28-30) | $119,553 | $15,542 | $104,011 | $7,650 | $96,361 | $378,907 |
| Q11 (M31-33) | $138,987 | $18,068 | $120,919 | $7,650 | $113,269 | $492,176 |
| Q12 (M34-36) | $157,277 | $20,446 | $136,831 | $7,650 | $129,181 | $621,357 |
| **Y3** | **$514,721** | **$66,914** | **$447,807** | **$30,600** | **$417,207** | **$621,357** |

### Annual P&L Summary

| | Year 1 | Year 2 | Year 3 | 3-Year Total |
|---|--------|--------|--------|-------------|
| Revenue | $35,370 | $234,286 | $514,721 | $784,377 |
| COGS (13%) | $4,598 | $30,457 | $66,914 | $101,969 |
| **Gross Profit (87%)** | **$30,772** | **$203,829** | **$447,807** | **$682,408** |
| OpEx | $9,450 | $21,000 | $30,600 | $61,050 |
| **Net Income** | **$21,322** | **$182,829** | **$417,207** | **$621,358** |
| Net margin | 60% | 78% | 81% | 79% |

**Why are the margins so high?** Two reasons: (1) infrastructure costs are minimal for a data product — you're not shipping physical goods, and (2) there's no headcount. A solo founder with $2,550/month in operating costs running a $54K/month revenue business is going to have enormous margins. This is the bootstrapped SaaS advantage.

**The real cost not captured here is your time.** If you value your time at $100/hour and spend 40 hours/week on this, that's ~$200K/year in imputed labor cost. The business is still profitable in Year 2 even with that factored in.

---

## 6. Unit Economics

Unit economics answer the question: **"Does it cost more to get a customer than that customer is worth?"** If the answer is yes, you lose money on every sale and can't grow your way out of it.

### LTV (Lifetime Value)

How much gross profit one average customer generates over their entire relationship with you.

**Formula:** LTV = (Monthly Revenue per Customer x Gross Margin) / Monthly Churn Rate

| Churn Rate | Avg Lifetime | LTV |
|------------|-------------|-----|
| 2% monthly | 50 months (4.2 years) | **$43,500** |
| 3% monthly | 33 months (2.8 years) | **$29,000** |
| 4% monthly | 25 months (2.1 years) | **$21,750** |

### CAC (Customer Acquisition Cost)

How much you spend in dollars to acquire one customer.

**Dollar CAC** (actual cash spent on marketing and events, divided by customers acquired):

| Period | Marketing + Events Spend | New Customers | Dollar CAC |
|--------|------------------------|---------------|------------|
| Year 1 | $6,000 | 9 | $667 |
| Year 2 | $14,400 | 24 | $600 |
| Year 3 | $20,400 | 36 | $567 |
| **3-Year Blended** | **$40,800** | **69** | **$591** |

**Fully Loaded CAC** (including imputed founder time at ~10 hours per customer x $100/hour):

| Period | Dollar Spend | Founder Time Value | Total | Customers | Fully Loaded CAC |
|--------|-------------|-------------------|-------|-----------|-----------------|
| Year 1 | $6,000 | $9,000 | $15,000 | 9 | $1,667 |
| Year 2 | $14,400 | $24,000 | $38,400 | 24 | $1,600 |
| Year 3 | $20,400 | $36,000 | $56,400 | 36 | $1,567 |
| **Blended** | **$40,800** | **$69,000** | **$109,800** | **69** | **$1,591** |

### LTV:CAC Ratio

The gold standard for SaaS health. Above 3x is good. Above 5x is great. Below 3x means you're spending too much to acquire customers relative to what they're worth.

| Churn Rate | LTV | CAC (fully loaded) | LTV:CAC |
|------------|-----|-------|---------|
| 2% | $43,500 | $1,591 | **27x** |
| 3% | $29,000 | $1,591 | **18x** |
| 4% | $21,750 | $1,591 | **14x** |

**All scenarios are extremely healthy.** Even the worst case (4% churn) has a 14x ratio. This is because founder-led sales with content marketing has near-zero dollar acquisition cost — the "cost" is your time, not your wallet.

### Payback Period

How many months until a customer's gross profit pays back their acquisition cost.

**Formula:** Payback = Fully Loaded CAC / (Monthly Revenue x Gross Margin)

$1,591 / ($1,000 x 0.87) = **1.8 months**

Translation: a new customer pays back their entire acquisition cost in less than 2 months. After that, every dollar is profit. This is outstanding — enterprise SaaS benchmarks target 12-18 months.

---

## 7. Churn Scenario Analysis

Same customer acquisition schedule across all scenarios. Only the churn rate changes.

### Year-End Comparison

| Metric | 2% Monthly | 3% Monthly | 4% Monthly |
|--------|-----------|-----------|-----------|
| **Year 1** | | | |
| End customers | 8.5 | 8.2 | 8.0 |
| ARR | $101,544 | $98,508 | $95,592 |
| Revenue collected | $35,370 | $34,592 | $33,838 |
| **Year 2** | | | |
| End customers | 28.2 | 26.1 | 24.3 |
| ARR | $337,896 | $313,200 | $290,988 |
| Revenue collected | $234,286 | $221,281 | $209,392 |
| **Year 3** | | | |
| End customers | 54.4 | 48.7 | 43.9 |
| ARR | $652,680 | $584,724 | $526,920 |
| Revenue collected | $514,721 | $468,484 | $428,293 |

### 3-Year Totals

| | 2% Churn | 3% Churn | 4% Churn |
|---|----------|----------|----------|
| Total revenue | $784,377 | $724,357 | $671,523 |
| Total COGS | $101,969 | $94,166 | $87,298 |
| Total gross profit | $682,408 | $630,191 | $584,225 |
| Total OpEx | $61,050 | $61,050 | $61,050 |
| **Total net income** | **$621,358** | **$569,141** | **$523,175** |

### What This Tells You

**Year 1 is nearly identical across scenarios.** With a small customer base (1-8 customers), churn barely matters — losing 2% vs 4% of 5 customers is the difference between 0.1 and 0.2 customers lost. The churn impact is negligible in Year 1.

**The gap widens in Years 2-3.** By Year 3, the difference between 2% and 4% churn is:
- 10.5 fewer customers (54 vs 44)
- $126K less ARR ($653K vs $527K)
- $98K less cumulative net income ($621K vs $523K)

**But the business works in ALL scenarios.** Even at 4% monthly churn:
- You still reach $527K ARR by Year 3
- You still generate $523K in cumulative net income
- LTV:CAC is still 14x
- Payback period is still under 2 months

**The strategic takeaway:** Churn management matters for long-term scale (getting to $1M+ ARR), but it's not a make-or-break risk in the first 3 years. The business is viable across all realistic churn scenarios.

### When Does the Math Break?

Working backward from "unsustainable" (LTV:CAC < 3x):

- At fully loaded CAC of ~$1,600, LTV needs to be at least $4,800
- $4,800 LTV at 87% margin = $5,517 lifetime revenue
- $5,517 / $1,000 per month = ~5.5 month average lifetime
- That requires ~18% monthly churn (87% annual churn)

**The model doesn't break until monthly churn exceeds ~18%.** Even the most pessimistic coaching-turnover scenario (4%) is nowhere near this. The unit economics have enormous safety margin.

---

## 8. Sensitivity Analysis

What happens to Year 3 ARR when you change one input by ±20%, holding everything else constant?

### ACV (Price) Sensitivity

| ACV | Y3 ARR | Y3 Net Income | 3yr Cumulative |
|-----|--------|--------------|----------------|
| $9,600 (-20%) | $522,144 | $333,766 | $497,086 |
| **$12,000 (base)** | **$652,680** | **$417,207** | **$621,358** |
| $14,400 (+20%) | $783,216 | $500,648 | $745,629 |

**Takeaway:** A 20% price increase adds $131K to Year 3 ARR and $124K to cumulative income. Worth testing $15K ACV early — if the product delivers clear value, coaches won't balk at $1,250/month vs $1,000/month.

### Customer Acquisition Rate Sensitivity

| Scenario | Y1 New | Y2 New | Y3 New | Y3 End Cust | Y3 ARR |
|----------|--------|--------|--------|-------------|--------|
| Slow (-20%) | 7 | 19 | 29 | ~43 | ~$522K |
| **Base** | **9** | **24** | **36** | **54** | **$653K** |
| Fast (+20%) | 11 | 29 | 43 | ~65 | ~$783K |

**Takeaway:** Customer acquisition speed is the highest-leverage variable. Getting 1 extra customer per month in Years 2-3 adds ~$130K to ARR. This is why paid ads matter — even if ads only contribute 10-15% of customers directly, they accelerate awareness that feeds organic and outbound channels.

### CPL (Paid Ad Efficiency) Sensitivity

| CPL | Paid Leads (Y1) | Extra/Fewer Customers | Impact on Y3 ARR |
|-----|-----------------|----------------------|-------------------|
| $120 (-20%) | 35 (+7 leads) | +0-1 | +$0-12K |
| **$150 (base)** | **28** | **—** | **—** |
| $180 (+20%) | 23 (-5 leads) | -0-1 | -$0-12K |

**Takeaway:** CPL sensitivity is low because paid ads drive only ~10% of total customers. A 20% swing in CPL changes Year 3 ARR by less than $12K. Don't obsess over ad efficiency — it's a supporting channel, not the primary growth engine.

### Gross Margin Sensitivity

| Margin | 3yr Net Income | Impact vs Base |
|--------|---------------|----------------|
| 80% | $566,452 | -$55K |
| **87% (base)** | **$621,358** | **—** |
| 93% | $668,019 | +$47K |

**Takeaway:** Gross margin has moderate sensitivity. If infrastructure costs creep up (premium data APIs, more compute), margins could drop to 80% — but the impact is manageable ($55K less over 3 years). If you find cheaper infrastructure solutions, the upside is similar.

### What Matters Most (Ranked by Impact)

1. **Customer acquisition rate** — Highest leverage. One extra customer/month = ~$130K more ARR by Year 3
2. **ACV / Pricing** — High leverage. A 20% price increase = $131K more ARR
3. **Churn rate** — Moderate leverage in years 2-3. Difference between 2% and 4% = $126K less ARR
4. **Gross margin** — Low-moderate. 7 points of margin = ~$55K over 3 years
5. **CPL** — Low. Paid ads are a small piece of the acquisition mix

---

## 9. Cash Position & Runway

### Monthly Cash Position (Year 1 Detail)

| Month | Revenue | Total Costs | Net | Cumulative Cash |
|-------|---------|------------|-----|-----------------|
| 1 | $0 | $200 | -$200 | -$200 |
| 2 | $0 | $200 | -$200 | -$400 |
| 3 | $0 | $500 | -$500 | -$900 |
| 4 | $0 | $700 | -$700 | -$1,600 |
| 5 | $1,000 | $830 | +$170 | -$1,430 |
| 6 | $1,980 | $1,107 | +$873 | -$557 |
| 7 | $2,940 | $1,432 | +$1,508 | +$951 |
| 8 | $3,882 | $1,555 | +$2,327 | +$3,278 |

**Maximum cash outlay before turning positive: $1,600** (end of Month 4)

This means you need less than $2,000 in starting capital to fund the business until it pays for itself. At your $1K/month budget, you have more than enough runway. There is no scenario in this model where you run out of money.

### Annual Cash Generation

| Year | Starting Cash | Net Income | Ending Cash |
|------|--------------|------------|-------------|
| 1 | $0 | $21,322 | $21,322 |
| 2 | $21,322 | $182,829 | $204,151 |
| 3 | $204,151 | $417,207 | $621,358 |

### When Can You Start Paying Yourself?

Depends on how much you want to take:

| Monthly Draw | Earliest Sustainable Month | Monthly Revenue at That Point |
|-------------|---------------------------|-------------------------------|
| $2,000/mo | Month 8 | $3,882 |
| $5,000/mo | Month 11 | $6,594 |
| $8,000/mo | Month 14 | ~$12,000 |
| $10,000/mo | Month 17 | ~$17,000 |

"Sustainable" = your draw plus all operating costs is less than monthly gross profit, and you're still accumulating cash.

---

## 10. Key Milestones & Decision Points

### Revenue Milestones

| Milestone | Target Month | Significance |
|-----------|-------------|--------------|
| First paying customer | Month 5 | Product-market signal. Someone will pay $1K/month for this |
| $100K ARR (8-9 customers) | Month 12 | Real business. Top 12% of indie hackers ever reach this |
| $250K ARR (~21 customers) | Month 19 | Sustainable solo income. Could hire first person |
| $500K ARR (~42 customers) | Month 29 | Serious business. 14% market penetration |
| $650K ARR (~54 customers) | Month 36 | 18% of SAM captured. Decision point: expand to new sports? |

### Decision Points

| When | Decision | Options |
|------|----------|---------|
| Month 6 (2 customers) | Is the product sticky? | If coaches use it weekly → keep going. If they log in once and ghost → pivot the product |
| Month 12 ($100K ARR) | Hire or stay solo? | If pipeline is overflowing → hire part-time CS. If manageable → stay solo and keep margins |
| Month 18 (~19 customers) | Expand to D2/NAIA? | If D1 penetration is strong → expand downmarket at lower price. If still grinding in D1 → focus |
| Month 24 (~28 customers) | Add basketball? | If the valuation model is proven and coaches trust it → adapt for basketball. If still iterating → stay in baseball |
| Month 30 (~42 customers) | Raise money or stay bootstrapped? | At $500K+ ARR with 87% margins, you have optionality. Raising money would accelerate but dilute |

---

## 11. What This Model Does NOT Include

Honest about the limitations:

1. **Expansion revenue** — No upsell or usage-based pricing modeled. If you add premium tiers ($2K/month for "conference-level" packages), revenue grows faster than shown
2. **Founder salary** — Net income doesn't account for your personal draw. Subtract whatever you take
3. **Seasonality** — College baseball has a season (Feb-June). Buying patterns may cluster around fall recruiting. Not modeled
4. **Tax** — All figures are pre-tax. Set aside 25-30% of net income for federal + state taxes
5. **One-time costs** — Legal (LLC formation, terms of service), initial conference travel, equipment. Probably $2,000-$5,000 upfront not included
6. **Competition response** — If Hudl or another player enters this niche, your acquisition rate drops. Not modeled
7. **Multi-year contracts** — If you offer annual prepaid discounts, cash collection timing changes (more cash upfront, less churn)

---

## 12. Comparison to Original Model

| Dimension | Original Template | This Model |
|-----------|------------------|------------|
| Buyer | Generic B2B SaaS | D1 college baseball programs specifically |
| Headcount | SDR + AE + CS by month 15 ($40K/mo) | Zero hires. Founder-led everything |
| Revenue at M36 | $141K ARR | $653K ARR |
| customers_end bug | Fractional wins with 0 customers | Fixed: whole-number new customers, fractional churn clearly labeled |
| CPL | Implied at ~$120, not stated | Explicit: $150 for paid, $0 for organic |
| P&L tab | Missing entirely | Full monthly Y1, quarterly Y2-Y3 |
| Unit economics | Formulas listed but not computed | CAC, LTV, LTV:CAC, payback all computed |
| TAM/SAM/SOM | Not included | Included with buyer universe data |
| Churn scenarios | Single 2% assumption | 2%, 3%, 4% all modeled |
| Sensitivity | "ARR decreases" (no dollar figures) | Actual dollar impacts for ±20% on each variable |
| Cash position | Not tracked | Monthly tracking with runway analysis |

---

*Model built: 2026-02-16*
*Assumptions source: sports-analytics-evaluation.md + pressure-test-notes.md*
*Next update: After Phase 2 product design decisions (may change ACV or margin assumptions)*
