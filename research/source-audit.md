# InvestRand Research - Source Audit

**Audit Date:** 17 January 2026
**Purpose:** Verify all claims with primary sources

---

## Revenue & Financial Data

| Claim | Value | Source | Verification |
|-------|-------|--------|--------------|
| Year 1 Revenue | R1M+ | Disrupt Africa (March 2024) | "In the first year, investRand did over ZAR1 million (US$52,000) in sales with no advertising" |
| Year 2 Revenue | ~R2M | Disrupt Africa (March 2024) | "in the second year, they almost doubled that and became profitable" |
| Profitable from Day 1 | Yes | Disrupt Africa (March 2024) | "the company has been profitable since its inception" |
| Commission Model | 5% (min R30k) | Disrupt Africa (March 2024) | "charging five percent of the property value, or a minimum of ZAR30,000 (US$1,500) on each transaction" |

**Source URL:** https://disruptafrica.com/2024/03/26/how-investrand-is-helping-young-south-africans-get-clever-with-property-investments/

---

## User Metrics

| Claim | Value | Source | Verification |
|-------|-------|--------|--------------|
| Total Users | ~1,000 | Disrupt Africa (March 2024) | "Since launching its marketplace in March 2023, investRand has acquired over 1,000 users" |
| Repeat Rate | 60% | Disrupt Africa (March 2024) | "with 60 per cent of customers being repeat clients" |
| Median Client Age | 33 | Disrupt Africa (March 2024) | "Their median client is a 33-year-old" |
| First-time Investors | ~50% | Disrupt Africa (March 2024) | "about half of them are first-time investors" |

---

## Founder Background

| Claim | Source | Verification |
|-------|--------|--------------|
| UCT Degree (Real Estate, 2022) | We Are Tech Africa | "degree in real estate development and investment from the University of Cape Town (obtained 2022)" |
| Founded InvestRand 2021 | Multiple sources | Consistent across We Are Tech Africa, Disrupt Africa, JT Communications |
| Founded Infinity Property Group 2017 | We Are Tech Africa | "Founded Infinity Property Group (2017)" |
| 6+ years real estate experience | Disrupt Africa | "working as a real estate agent for over half a decade" |
| Investec 2025 Award Nomination | LinkedIn/Search | "nominated for the Investec 2025 Early-Stage Entrepreneur of the Year Award" |
| SAIBPP100 Listing | IOL/Search | Listed in "South Africa's Top 100 black property practitioners" |
| President, 4thDimension Toastmasters | We Are Tech Africa | Direct statement in article |

**Source URLs:**
- https://www.wearetech.africa/en/fils-uk/tech-stars/ezra-rasethe-facilitates-real-estate-investing-in-south-africa
- https://jtcomms.co.za/emerging-black-innovator-and-entrepreneur-ezra-rasethe-democratizing-wealth-creation-in-south-africa-through-property-investment/

---

## Develutions Proposal Pricing

| Claim | Value | Source | Verification |
|-------|-------|--------|--------------|
| Monthly Retainer | R55,000 excl VAT | Develutions WBS PDF | Page 17: "Rate: R55 000 excluding vat" |
| Term | 12 months minimum | Develutions WBS PDF | Page 17: "Commitment: Minimum 12-month retainer agreement" |
| Annual Cost | R660,000 | Calculated | R55,000 × 12 = R660,000 |
| Hours per Month | 60 minimum | Develutions WBS PDF | Page 17: "Guaranteed Hours: Minimum 60 hours per month" |
| Hourly Alternative | R1,100/hour | Develutions WBS PDF | Page 18: "Rate: R1100/hour excluding vat" |

**Source:** InvestRand_Work_Breakdown_Structure_v1.0.pdf (provided by Ezra via email)

---

## Technical Stack (Verified)

| Claim | Source | Verification Method |
|-------|--------|---------------------|
| Vue.js 2.6.14 (EOL Dec 2023) | Ampersand Due Diligence | External analysis of platform.investrand.co.za |
| Django Backend | Develutions System Analysis | Internal code review |
| AWS Lambda (Zappa) | Develutions System Analysis | Internal infrastructure review |
| 15s Load Time | Ampersand Due Diligence | Lighthouse audit |
| 36% Performance Score | Ampersand Due Diligence | Lighthouse audit |
| 23MB Bundle Size | Develutions System Analysis | Page 6: "Total Bundle: 23 MB" |
| 197 Vue Components | Develutions System Analysis | Page 5: "197 components (44 base, 152 views)" |

**Sources:**
- Ampersand Due Diligence Report (12 January 2026) - External reconnaissance
- Develutions System Analysis v1.0 PDF - Internal code access

---

## Market Statistics

| Claim | Value | Source | Verification |
|-------|-------|--------|--------------|
| SA Residential Market 2025 | USD 21.97B | Research and Markets | Industry report |
| Market 2030 Projection | USD 36.13B | Research and Markets | Industry report |
| CAGR | 10.46% | Research and Markets | Industry report |
| Housing Shortage | 2.3M units | Multiple sources | Statista, The Africanvestor |
| House Price Growth (Apr 2025) | 3.7% | Ooba, Global Property Guide | National average |
| Repo Rate (May 2025) | 7.25% | Multiple sources | SARB announcement |
| CPI (Apr 2025) | 2.8% | Multiple sources | Stats SA |
| FATF Impact | 30-35% investor increase | RSM, JLL | Post-grey-list-removal |

**Source URLs:**
- https://www.researchandmarkets.com/reports/5529324/south-africa-residential-real-estate-market
- https://theafricanvestor.com/blogs/news/south-africa-real-estate-market
- https://www.ooba.co.za/resources/property-market-south-africa/

---

## Competitor Data

| Claim | Source | Verification |
|-------|--------|--------------|
| IGrow: 220,000+ investors | IGrow website, LocalMoney review | Stated on igrow.co.za |
| IGrow: Founded 2006 | IGrow website | Company about page |
| IGrow: Trustpilot complaints | Trustpilot | Direct review reading |
| EasyProperties: R300M+ portfolio | EasyProperties website | Stated on properties.easyequities.co.za |
| EasyProperties: R1 minimum | EasyProperties website | Platform feature |
| Crowdprop: R10,000 minimum | Crowdprop website | Platform feature |
| Stokvels: 11M members, R50B annually | JTB Consulting | SA PropTech Market 2025 report |

---

## Claims WITHOUT Primary Sources (To Verify)

| Claim | Current Source | Status |
|-------|----------------|--------|
| "45+ partner companies" | InvestRand website | **Self-reported - not independently verified** |
| "R2.5B+ opportunities" | InvestRand website | **Self-reported - not independently verified** |
| "230+ locations" | InvestRand website | **Self-reported - not independently verified** |
| "AI-powered" claims | InvestRand website | **Marketing claim - no technical evidence** |

---

## Revenue Context

### Key Calculation
- Revenue ~R2M/year (Year 2)
- Develutions proposal: R660k/year
- **Proposal = 33% of annual revenue**

This is the critical insight: Develutions is proposing to spend 33% of InvestRand's annual revenue on a technology migration.

### Revenue per User Calculation
- ~1,000 users
- ~R2M revenue
- = ~R2,000 average revenue per user

This suggests either:
1. Low transaction volume per user, OR
2. Many users haven't transacted yet, OR
3. Revenue concentrated in larger deals

At 5% commission with R30k minimum:
- R2M revenue ÷ R30k minimum = ~67 transactions maximum
- Or fewer transactions at higher values

---

## Summary: Source Confidence Levels

| Category | Confidence | Notes |
|----------|------------|-------|
| Revenue/Users | HIGH | Direct quotes from Disrupt Africa interview with founder |
| Founder Background | HIGH | Multiple independent sources |
| Develutions Pricing | HIGH | Primary source document |
| Technical Stack | HIGH | Independent verification (Ampersand DD) |
| Market Statistics | HIGH | Third-party research firms |
| Competitor Data | MEDIUM | Mix of company claims and reviews |
| InvestRand Platform Claims | LOW | Self-reported marketing, not verified |

---

*Audit completed: 17 January 2026*
