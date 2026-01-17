# InvestRand Company Profile

**Research Date:** 17 January 2026
**Prepared by:** Ampersand Insights

---

## Executive Summary

InvestRand is a South African proptech startup operating a three-sided marketplace connecting property investors, sellers, and service providers. Founded in 2021 by Ezra Rasethe, the platform launched its marketplace in March 2023 and has acquired ~1,000 users with a 60% repeat rate. The company is bootstrapped, profitable from inception, and generates approximately R2M annually through a 5% transaction fee model (minimum R30,000 per transaction).

**Key Insight:** While InvestRand positions itself as a technology platform, its current challenges are fundamentally business and operational rather than purely technical. The proposed R660k tech migration represents 33% of annual revenue—a disproportionate investment that addresses symptoms rather than root causes.

---

## Company Overview

| Attribute | Detail |
|-----------|--------|
| **Legal Name** | InvestRand |
| **Founded** | 2021 |
| **Marketplace Launch** | March 2023 |
| **Headquarters** | Johannesburg, South Africa |
| **Website** | www.investrand.co.za |
| **Platform** | platform.investrand.co.za |
| **Industry** | PropTech / Real Estate Investment |
| **Business Model** | Three-sided marketplace (B2C2B) |

### Mission Statement
"To empower ordinary South Africans to create long-term wealth through property."

### Value Proposition
InvestRand reduces the complexity of property investing, making it simple, accessible, and profitable. The platform connects investors with:
- Pre-vetted investment properties
- Reliable service providers
- Multiple financing options

---

## Founder Profile: Ezra Rasethe

### Background
- **Role:** Founder & CEO
- **Education:** Degree in Real Estate Development and Investment, University of Cape Town (2022)
- **Prior Experience:** Real estate agent for over half a decade before founding InvestRand
- **Other Ventures:** Founder & CEO of Infinity Property Group (2017) - encompasses proptech, affordable housing, and student housing divisions
- **Community:** President of 4thDimension Toastmasters club

### Recognition
- Nominated for **Investec 2025 Early-Stage Entrepreneur of the Year Award** (Consumer category via OPUS)
- Listed in **SAIBPP100** - South Africa's Top 100 black property practitioners driving transformation in the industry
- Featured in multiple publications: Disrupt Africa, IOL, We Are Tech Africa, Vutivi Business

### Origin Story
Ezra founded InvestRand after purchasing his first investment property and recognising the challenges ordinary South Africans face navigating the property market. His initial motivation came from helping friends and family find quality property investments.

### Notable Quote
> "If done right, real estate investing can be a great wealth hack for ordinary South Africans."

> "In the South African context, where we're transitioning from a legacy of apartheid that excluded black people from owning property and land, there's an urgent need for transformative solutions. InvestRand is committed to changing the way people think about land ownership and property investment."

---

## Business Model

### Revenue Model
- **Commission:** 5% of property value per transaction
- **Minimum Fee:** R30,000 (US$1,500) per transaction, whichever is higher
- **Current Revenue:** ~R2M annually (Year 2)
- **Profitability:** Profitable from day one (bootstrapped)

### Three-Sided Marketplace

| Stakeholder | Value Delivered |
|-------------|-----------------|
| **Investors** | Access to vetted properties, financing options, service providers, investment guidance |
| **Property Sellers** | Access to qualified, motivated buyers |
| **Service Providers** | Lead generation, platform presence |

### Target Market
- **Primary:** Young professionals (median age 33)
- **First-time investors:** ~50% of customer base
- **Geography:** South Africa (with expansion ambitions to Africa, Australia, USA)

### Claimed Platform Statistics
- 45+ partner companies
- R2.5B+ in opportunities
- 230+ locations

---

## Key Metrics

| Metric | Value | Notes |
|--------|-------|-------|
| **Users** | ~1,000 | Since March 2023 launch |
| **Repeat Rate** | 60% | Strong retention signal |
| **Year 1 Revenue** | ~R1M | No advertising spend |
| **Year 2 Revenue** | ~R2M | Nearly doubled YoY |
| **Team Size** | 2 core | Ezra (CEO) + Francois van der Merwe (CTO/Advisor) |

---

## Technology Stack (Current)

| Component | Technology | Status |
|-----------|------------|--------|
| **Frontend** | Vue 2.6 | End of Life (EOL) |
| **Backend** | Django | Functional |
| **Hosting** | Netlify, Cloudflare | Standard |
| **Website** | Wix (marketing site) | Separate from platform |

### Technical Issues Identified
1. **Performance:** 15-second page load times
2. **Security:** Missing security headers
3. **Integrations:** Broken CRM integrations
4. **Bugs:** 11 operational bugs documented by Develutions
5. **Accessibility:** Poor mobile experience

### Develutions' Proposal
- Full migration to React 18 / Spring Boot 3.4 / Java 21
- Cost: R660k/year (33% of current revenue)
- **Ampersand Assessment:** Over-engineered for SMB scale; most bugs are workflow/integration issues, not framework problems

---

## Competitive Landscape

### Direct Competitors

#### IGrow Wealth Investments
| Aspect | Detail |
|--------|--------|
| **Founded** | 2006 |
| **Model** | Vertically integrated property investment (buy-to-let focus) |
| **Users** | Claims 220,000+ investors assisted |
| **Approach** | End-to-end locked ecosystem (acquisition, financing, management, accounting) |
| **Pricing** | Multiple fees across services; R15,000 investor software upfront |
| **Reputation** | Mixed - strong advisory but complaints about communication, hidden fees, lock-in |
| **Key Difference** | Established, larger scale, but more expensive and restrictive |

#### PropInvest
- High-yield development focus
- Expert advisory with free consultations
- Traditional model

### Fractional Property Platforms

| Platform | Minimum Investment | Model |
|----------|-------------------|-------|
| **EasyProperties** | R1 | Fractionalised shares in property SPVs; R300M+ portfolio |
| **FracProp** | Variable | Community-first; stokvel integration; cross-border (Botswana) |
| **Crowdprop** | R10,000 | Crowdfunding; residential, commercial, industrial, agricultural |
| **Wealth Migrate** | Variable | International property crowdfunding |

### InvestRand's Positioning
InvestRand sits between:
- **Full-service lock-in models** (IGrow) - too expensive and restrictive
- **Fractional platforms** (EasyProperties) - don't offer full ownership
- **Traditional agents** - lack curation and investment guidance

**Unique Value:** Full property ownership with marketplace convenience and vetted options.

---

## Market Context: SA Real Estate 2025

### Market Size
- **Residential Market (2025):** USD 21.97 billion
- **Projected (2030):** USD 36.13 billion
- **CAGR:** 10.46%
- **Housing Shortage:** 2.3 million units

### Economic Indicators
- **House Price Growth:** 3.7% nationally (April 2025)
- **Repo Rate:** 7.25% (May 2025) - 4th consecutive cut
- **Prime Lending Rate:** Expected to drop to 10.50% by end-2025
- **CPI:** 2.8% (April 2025) - below SARB's 3-6% target

### Regional Performance
| Region | Expected Growth |
|--------|----------------|
| Western Cape | 5-8% |
| KwaZulu-Natal | 3-5% |
| Gauteng | 1-3% |

### Investment Yields
- **Residential:** 5-8% capex rates
- **Commercial:** 11% capex rates
- **Johannesburg:** 7-10% average yield
- **Sectional titles:** 10.62% vs 7.44% for full-title

### Buyer Demographics
- **Average buyer age:** 37 years
- **First-time buyer average age:** 36 years (up 3 years over decade)
- **Home loan usage:** 60% of buyers
- **76% of properties:** Valued below R1.2 million

### Key Trends
1. **Semigration:** Growing demand in coastal towns (Hermanus, Plettenberg Bay, Umhlanga)
2. **Sectional Title Preference:** Security, affordability, lifestyle driving shift from freehold
3. **Mixed-Use Developments:** Rising demand for combined residential/commercial/retail
4. **FATF Delisting Impact:** 30-35% increase in investor activity post-grey list removal

---

## Online Presence Assessment

### Website (investrand.co.za)
- Built on Wix platform
- Claims AI-powered features
- Performance issues (15s load time reported)
- Mobile experience problematic

### LinkedIn
- 702 followers (investRand company page)
- Active posting by Ezra Rasethe
- Testimonials featured

### Press Coverage
- **Disrupt Africa** (March 2024): Feature on helping young South Africans
- **IOL:** "Democratising wealth creation" profile
- **We Are Tech Africa:** Founder spotlight
- **Vutivi Business:** Platform profile

### Third-Party Reviews
- **No presence on HelloPeter or Trustpilot** (searched January 2026)
- Testimonials exist only on owned properties (LinkedIn, website)

---

## SWOT Analysis

### Strengths
- **Founder credibility:** Real estate education + 6+ years industry experience
- **Profitable from day one:** No dependency on external funding
- **Strong retention:** 60% repeat rate indicates product-market fit
- **Mission-driven:** Strong narrative around democratising wealth
- **Recognition:** Investec award nomination, SAIBPP100 listing

### Weaknesses
- **Technical debt:** Outdated Vue 2.6 frontend, performance issues
- **Small team:** Only 2 core members (CEO + CTO/Advisor)
- **Limited resources:** R660k proposal = 33% of revenue
- **No independent reviews:** Lack of third-party validation
- **CRM integration issues:** Operational friction

### Opportunities
- **Market timing:** Rate cuts, FATF delisting, housing shortage
- **Underserved segment:** Young professionals priced out of traditional market
- **Stokvel integration:** 11M members, R50B annually - untapped channel
- **Geographic expansion:** Model fits Africa, Australia, USA per founder
- **Fractional hybrid:** Could add fractional options to full-ownership model

### Threats
- **Well-funded competitors:** EasyProperties (R300M+ portfolio), IGrow (established since 2006)
- **Tech migration risk:** Major platform change could disrupt operations
- **Economic volatility:** Interest rate sensitivity, GDP growth at 1%
- **Regulatory environment:** FSCA, SARB, SARS compliance requirements
- **Founder dependency:** Business heavily reliant on Ezra's relationships

---

## Strategic Observations for Ampersand

### The Real Problem
Ezra is experiencing what appears to be a **business model scaling challenge**, not primarily a technology problem:

1. **Operational Overwhelm:** He explicitly wants people who "take work away, not give more work"
2. **Revenue Concentration:** R2M from ~1,000 users = ~R2,000 average per user; need volume or value increase
3. **Team Capacity:** 2-person team cannot scale without systemisation
4. **Integration Gaps:** CRM issues suggest workflow, not framework, problems

### Develutions Proposal Analysis
The R660k full-stack migration proposal appears to be:
- **Over-engineered:** SMB scale doesn't require enterprise Java architecture
- **Symptom-focused:** 11 bugs are mostly workflow issues, not Vue 2.6 limitations
- **Disproportionate:** 33% of revenue for uncertain benefit
- **Risk-laden:** Full migration disrupts operations during growth phase

### Opportunity for Ampersand
Ezra mentioned potentially having Chand become a "fractional owner of the product" - this signals:
1. He values partnership over vendor relationships
2. He's open to alternative engagement models
3. He needs strategic guidance, not just technical execution

### Recommended Approach
1. **Immediate wins:** Fix the 11 bugs with targeted interventions (not full rewrite)
2. **Stabilisation:** Address performance (15s load) with optimisation, not migration
3. **Business focus:** Help define what InvestRand needs to be at R10M revenue
4. **Phased modernisation:** If Vue 2.6 must go, incremental migration over 12-18 months
5. **Fractional CTO model:** Provide strategic technical leadership Ezra lacks

---

## Sources

- [Disrupt Africa - InvestRand Feature](https://disruptafrica.com/2024/03/26/how-investrand-is-helping-young-south-africans-get-clever-with-property-investments/)
- [We Are Tech Africa - Ezra Rasethe Profile](https://www.wearetech.africa/en/fils-uk/tech-stars/ezra-rasethe-facilitates-real-estate-investing-in-south-africa)
- [JT Communications - Ezra Rasethe Feature](https://jtcomms.co.za/emerging-black-innovator-and-entrepreneur-ezra-rasethe-democratizing-wealth-creation-in-south-africa-through-property-investment/)
- [The Africanvestor - SA Real Estate Stats](https://theafricanvestor.com/blogs/news/south-africa-real-estate-market)
- [Statista - SA Real Estate Market Forecast](https://www.statista.com/outlook/fmo/real-estate/south-africa)
- [Research and Markets - SA Residential Real Estate](https://www.researchandmarkets.com/reports/5529324/south-africa-residential-real-estate-market)
- [LocalMoney - IGrow Review](https://localmoney.co.za/igrow-wealth-investments-a-review-for-south-african-property-investors/)
- [Trustpilot - IGrow Reviews](https://www.trustpilot.com/review/igrow.co.za)
- [InvestRand Website](https://www.investrand.co.za)
- [InvestRand LinkedIn](https://za.linkedin.com/company/investrand32)
