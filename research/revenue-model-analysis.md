# InvestRand Revenue Model Analysis

**Analysis Date:** 17 January 2026
**Source:** Disrupt Africa (March 2024) - Founder Interview

---

## Disclosed Data Points

| Metric | Value | Direct Quote |
|--------|-------|--------------|
| Commission Rate | 5% of property value | "charging five percent of the property value" |
| Minimum Fee | R30,000 per transaction | "or a minimum of ZAR30,000 (US$1,500) on each transaction" |
| Year 1 Revenue | R1M+ | "did over ZAR1 million in sales with no advertising" |
| Year 2 Revenue | ~R2M | "almost doubled that and became profitable" |
| Platform Users | ~1,000 | "acquired over 1,000 users" |
| Repeat Rate | 60% | "60 per cent of customers being repeat clients" |
| Profitability | Day 1 | "the company has been profitable since its inception" |

**Source URL:** https://disruptafrica.com/2024/03/26/how-investrand-is-helping-young-south-africans-get-clever-with-property-investments/

---

## Commission Structure Analysis

### How the Pricing Works

The model uses **whichever is higher**: 5% or R30k minimum.

| Property Value | 5% Commission | Actual Fee Charged | Why |
|----------------|---------------|-------------------|-----|
| R400,000 | R20,000 | **R30,000** | Minimum kicks in |
| R500,000 | R25,000 | **R30,000** | Minimum kicks in |
| R600,000 | R30,000 | **R30,000** | Breakeven point |
| R800,000 | R40,000 | **R40,000** | 5% applies |
| R1,000,000 | R50,000 | **R50,000** | 5% applies |
| R2,000,000 | R100,000 | **R100,000** | 5% applies |

### Key Threshold

**R600,000 is the breakeven point** where 5% equals the R30k minimum.

- Properties **below R600k**: Flat R30k fee (effectively higher than 5%)
- Properties **above R600k**: Straight 5% commission

This protects InvestRand's unit economics on smaller deals while remaining competitive on larger ones.

---

## Transaction Volume Estimates

### Maximum Transaction Count

```
Year 2 Revenue:     ~R2,000,000
Minimum Fee:        R30,000 per transaction
Maximum Deals:      R2,000,000 ÷ R30,000 = ~67 transactions
```

**67 is the ceiling** - if every deal was at the minimum fee.

### More Likely Scenario

If the average deal involves properties around R800k-R1M (common for investment properties in Gauteng/Western Cape), the average commission would be R40-50k.

```
At R40k average:    R2,000,000 ÷ R40,000 = 50 transactions
At R50k average:    R2,000,000 ÷ R50,000 = 40 transactions
```

**Likely range: 40-67 transactions in Year 2**

---

## User-to-Transaction Gap

### The Numbers

| Metric | Value |
|--------|-------|
| Registered Users | ~1,000 |
| Estimated Transactions | 40-67 |
| Conversion Rate | 4-7% |
| Revenue per User | ~R2,000 |

### What This Suggests

1. **Most users are in the funnel, not transacting**
   - 1,000 registered users
   - Only 40-67 have actually completed transactions
   - 93-96% of users haven't transacted yet

2. **Low average revenue per user**
   - R2M ÷ 1,000 users = R2,000 average
   - This is misleading because most users contribute R0
   - Active customers are worth much more

3. **The real unit economics are strong**
   - If 50 customers generated R2M, that's R40k per active customer
   - 60% repeat rate means loyal customers come back
   - The challenge is conversion, not retention

---

## Repeat Rate Analysis

### What 60% Repeat Rate Means

If 60% of customers are repeat clients:

| Scenario | First-Time Buyers | Repeat Buyers | Total Transactions |
|----------|------------------|---------------|-------------------|
| 50 deals | 20 customers (40%) | 30 deals from returning customers | 50 |
| 60 deals | 24 customers (40%) | 36 deals from returning customers | 60 |

### Implications

- **Small but loyal customer base**: Maybe 30-50 unique active customers
- **Strong product-market fit signal**: People who buy, buy again
- **Referral potential**: Satisfied repeat customers likely refer others
- **Founder relationship-driven?**: Are these Ezra's network connections?

---

## Growth Implications

### Current State (Year 2)

- ~R2M revenue
- ~40-67 transactions
- ~1,000 registered users
- ~4-7% conversion rate

### To Reach R10M Revenue

| Path | Required Change |
|------|-----------------|
| More transactions | 200-330 deals/year (5x current) |
| Higher value deals | Average deal size to R150-250k commission |
| Better conversion | 20-35% conversion rate (5x current) |
| More users | 5,000 users at current conversion |

### The Real Challenge

The business needs to either:

1. **Scale the funnel**: More registered users → more transactions
2. **Improve conversion**: Better nurturing of existing 1,000 users
3. **Move upmarket**: Focus on higher-value properties (R2M+)
4. **Systematise sales**: Reduce founder dependency in closing deals

---

## Questions This Raises for the Meeting

1. **"Are most of your deals coming through your personal network, or through the platform?"**
   - Tests whether the 60% repeat rate is relationship-driven or product-driven

2. **"What's your typical property value range?"**
   - Validates our commission estimates

3. **"What happens to the 93% of users who register but don't transact?"**
   - Understanding the funnel drop-off

4. **"Is the R30k minimum ever a barrier, or do most deals clear it easily?"**
   - Tests whether pricing is optimised

5. **"How many unique customers do you have vs. total transactions?"**
   - Direct validation of repeat rate mechanics

---

## Strategic Observations

### For Ampersand's Positioning

1. **The technology isn't losing deals** - conversion is the issue, likely sales/nurturing process

2. **CRM integration problems hurt here** - if you can't nurture 1,000 users effectively, you leak conversions

3. **This is a business scaling challenge** - not a Vue.js problem

4. **Quick win opportunity**: Improve conversion from 5% to 10% = double revenue without new users

### The R660k Proposal in Context

- Develutions proposal = R660k/year
- InvestRand revenue = ~R2M/year
- **Proposal = 33% of revenue**

For a business that needs to improve conversion and reduce founder dependency, a full-stack rewrite doesn't address the core problem. Better CRM workflows and operational systemisation would have higher ROI.

---

*Analysis completed: 17 January 2026*
