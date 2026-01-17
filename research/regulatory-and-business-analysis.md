# InvestRand: Regulatory, Compliance & Business Model Analysis

**Date:** 17 January 2026
**Purpose:** Comprehensive analysis of business model, regulatory requirements, and technology-business alignment

---

## 1. The Actual Business Model (Not What We Assumed)

### Critical Finding

**InvestRand is NOT a fractional property investment platform.**

From their own marketing:
> "With investRand, you get **full ownership** of your property—no fractional investments, no hidden costs."

This fundamentally changes the regulatory and technology analysis.

### What InvestRand Actually Does

InvestRand is a **property sourcing marketplace**:

1. **Source properties** - Find income-generating investment properties
2. **Present to investors** - List on platform with financial projections (ROI, rental yield, bond calculations)
3. **Connect with services** - Financing options, service providers, contractors
4. **Investor buys property** - Full ownership transfer (not fractional)
5. **InvestRand earns 5% sourcing fee** - Minimum R30,000 per transaction

### Target Market
- Median customer: 33 years old
- ~50% first-time property investors
- People with disposable income seeking property investment guidance

### Stated Traction (as of March 2024)
- 1,000+ users
- 60% repeat customers
- R1M+ revenue in first year
- Profitable since inception
- Bootstrapped (no external funding)

---

## 2. Business Model Workflow Comparison

### CURRENT STATE: How the Business Actually Works

```
┌─────────────────────────────────────────────────────────────────────┐
│                    INVESTRAND BUSINESS MODEL                        │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│  PROPERTY SOURCING                                                  │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐                      │
│  │ Sourcing │───▶│ Property │───▶│ Admin    │                      │
│  │ Agent    │    │ Listed   │    │ Approval │                      │
│  │ finds    │    │ on       │    │ (quality │                      │
│  │ property │    │ platform │    │ check)   │                      │
│  └──────────┘    └──────────┘    └──────────┘                      │
│                                       │                             │
│                                       ▼                             │
│  INVESTOR DISCOVERY           ┌──────────────┐                     │
│  ┌──────────┐                │ Property     │                      │
│  │ Investor │───────────────▶│ Published    │                      │
│  │ browses  │                │ with ROI/    │                      │
│  │ platform │                │ calculations │                      │
│  └──────────┘                └──────────────┘                      │
│       │                             │                               │
│       ▼                             ▼                               │
│  ┌──────────┐                ┌──────────────┐                      │
│  │ Express  │                │ Contact      │     ◀── WHERE IS     │
│  │ Interest │───────────────▶│ Sourcing     │         THIS IN THE  │
│  │ (FUTURE) │                │ Agent???     │         PLATFORM?    │
│  └──────────┘                └──────────────┘                      │
│                                     │                               │
│  ════════════════════════════════════════════════════════════════  │
│  ║           GAP: DEAL FACILITATION NOT IN PLATFORM              ║  │
│  ════════════════════════════════════════════════════════════════  │
│                                     │                               │
│                                     ▼                               │
│  OFFLINE PROCESS             ┌──────────────┐                      │
│  ┌──────────┐                │ Property     │                      │
│  │ Lawyers, │◀──────────────▶│ Transfer     │                      │
│  │ Finance, │                │ (Conveyancer)│                      │
│  │ etc.     │                └──────────────┘                      │
│  └──────────┘                       │                               │
│                                     ▼                               │
│  REVENUE                     ┌──────────────┐                      │
│  ┌──────────┐                │ Investor     │                      │
│  │ 5% Fee   │◀───────────────│ Owns         │                      │
│  │ Collected│                │ Property     │                      │
│  │ (HOW???) │                │ (FULL)       │                      │
│  └──────────┘                └──────────────┘                      │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

### THE TECHNOLOGY GAP

| Business Need | Platform Status | Gap |
|---------------|-----------------|-----|
| Property sourcing & listing | ✅ EXISTS | Working |
| Financial calculations (ROI, bond) | ⚠️ BUGS | ROI not matching financial model |
| Investor discovery | ✅ EXISTS | Working (all "Sold Out" currently) |
| Express Interest / Lead capture | ❌ FUTURE | Not implemented |
| CRM Integration (ActiveCampaign) | ❌ BROKEN | Contacts not syncing |
| Deal facilitation | ❌ NOT IN SCOPE | How does deal close? |
| Fee collection | ❌ NOT IN SCOPE | How is 5% collected? |
| Service provider marketplace | ✅ EXISTS | Present but untested |

### WHAT DEVELUTIONS IS BUILDING

```
┌─────────────────────────────────────────────────────────────────────┐
│              DEVELUTIONS REBUILD (React/Spring Boot)                │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│  PROGRESS BY CATEGORY:                                              │
│                                                                     │
│  Frontend (React 18)        ████████████████████░░░░ 80%           │
│  Backend (Spring Boot)      ███████████████████░░░░░ 75%           │
│  Property Display           █████████████████████░░░ 85%           │
│  User Management            ████████████████░░░░░░░░ 60%           │
│  Approval Workflow          ██████████████░░░░░░░░░░ 55%           │
│  Database/Architecture      █████████████░░░░░░░░░░░ 50%           │
│  Security                   ██████████░░░░░░░░░░░░░░ 40%           │
│                                                                     │
│  ┌─────────────────────────────────────────────────────────────┐   │
│  │  CRITICAL BUSINESS FUNCTIONS:                                │   │
│  │                                                              │   │
│  │  Financial Calculations  ████████░░░░░░░░░░░░░░░░ 35%       │   │
│  │  CRM Integrations        ░░░░░░░░░░░░░░░░░░░░░░░░ 0%        │   │
│  │  Deal Facilitation       NOT IN SCOPE                       │   │
│  │  Fee Collection          NOT IN SCOPE                       │   │
│  └─────────────────────────────────────────────────────────────┘   │
│                                                                     │
│  OBSERVATION: Building infrastructure, not business functionality  │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 3. Regulatory & Compliance Requirements

### 3.1 Property Practitioners Regulatory Authority (PPRA/EAAB)

**The Core Question:** Is the 5% "sourcing fee" actually commission on property sales?

**Legal Framework:**
- Property Practitioners Act 22 of 2019 (replaced Estate Agency Affairs Act)
- Section 34A: Cannot earn commission without Fidelity Fund Certificate (FFC)
- PPRA registration required for anyone facilitating property transactions

**InvestRand's Position:**
- Charging 5% (min R30,000) per transaction
- Connecting buyers with properties
- This looks like estate agency activity

**Potential Issue:**
- If InvestRand or sourcing agents are not PPRA-registered with valid FFCs, they may be operating illegally
- The "spotter's fee" exception is narrow and requires not "holding oneself out" as an agent

**Questions to Verify:**
1. Is InvestRand registered with PPRA?
2. Is Ezra Rasethe (former estate agent) still registered?
3. Are the "sourcing agents" on the platform PPRA-registered?

### 3.2 Financial Sector Conduct Authority (FSCA)

**The Core Question:** Is InvestRand providing financial advice?

**Legal Framework:**
- Financial Advisory and Intermediary Services Act (FAIS)
- FSP license required to provide financial advice or intermediary services
- Category I FSP for non-discretionary advice

**InvestRand's Position:**
- Platform calculates ROI, bond repayments, rental yields
- Presents this information to help investors make decisions
- Connects investors with financing options

**Potential Issue:**
- If the platform is advising on financial products (bonds, investments), may need FSP license
- If connecting to financing partners and earning referral fees, may need authorisation

**Comparison to Competitors:**
- EasyProperties operates under FSP License 22588 (through First World Trader)
- They are authorised to deal in financial products

### 3.3 Collective Investment Schemes Control Act (CISCA)

**NOT Applicable** - InvestRand does not pool investor funds. Each investor gets full property ownership.

### 3.4 Stokvel Model Consideration

**Potential Alternative Structure:**

Stokvels are exempt from:
- Banks Act
- FAIS
- National Credit Act

Could InvestRand structure property investment clubs as registered stokvels?

**Requirements:**
- Register with NASASA if holding > R100,000
- Have a constitution
- Pool funds in agreed common place
- Transparent financial records

**Benefit:** Regulatory simplification for group property investments

**Platforms already exploring this:** FracProp is piloting stokvel participation models

---

## 4. Competitive Landscape

### EasyProperties (Purple Group)
- **Model:** Fractional ownership through SPVs
- **License:** FSP 22588 (First World Trader)
- **Minimum:** No minimum investment
- **Structure:** Company per property, investors buy shares
- **Exit:** 5-7 year investment period or auction
- **Tax:** Company tax (28%) + dividends withholding (20%)

### Crowdprop
- **Model:** Property crowdfunding
- **Minimum:** R10,000
- **Fees:** 5% capital raise fee, 5% management fee
- **Types:** Residential, industrial, commercial, agricultural
- **Regulatory:** Unclear from research

### InvestRand (Current)
- **Model:** Property sourcing marketplace
- **Outcome:** Full property ownership
- **Fee:** 5% (min R30,000) per transaction
- **License:** Unknown - requires verification
- **Target:** First-time investors, median age 33

### Key Differentiator
InvestRand is NOT competing with EasyProperties/Crowdprop. They serve different needs:
- EasyProperties = Fractional for small investors (R1-R1000)
- InvestRand = Full ownership for investors with capital for deposits/bonds

---

## 5. The Business Problem (Restated)

### What InvestRand Needs Technology To Do

1. **Source & Present Properties**
   - Accurate financial projections (ROI, rental yield, bond calculations)
   - Quality photos and information
   - Admin approval workflow

2. **Capture & Convert Leads**
   - Express Interest functionality (CURRENTLY MISSING)
   - CRM integration for follow-up (CURRENTLY BROKEN)
   - Lead scoring and prioritisation

3. **Facilitate Deals**
   - Connect investor with sourcing agent (HOW?)
   - Track deal progress (NOT IN PLATFORM)
   - Coordinate with lawyers, financiers (NOT IN PLATFORM)

4. **Collect Revenue**
   - Track when deals close (HOW?)
   - Invoice 5% fee (HOW?)
   - Commission accounting (NOT IN PLATFORM)

5. **Post-Purchase Support**
   - Portfolio tracking for investors
   - Service provider marketplace
   - Ongoing property management referrals

### What the Current Platform Actually Does

1. ✅ Lists properties with financial calculations
2. ❌ Lead capture is "future"
3. ❌ Deal facilitation not in scope
4. ❌ Revenue collection not in platform
5. ⚠️ Portfolio tracking exists but empty

### What Develutions is Building

1. ✅ Better infrastructure for listing properties
2. ⚠️ Financial calculations only 35% done
3. ❌ CRM integration 0% done
4. ❌ Deal facilitation not in scope
5. ⚠️ Same gaps as current platform

---

## 6. Regulatory Compliance Checklist

### Must Verify

| Item | Requirement | How to Verify |
|------|-------------|---------------|
| PPRA Registration | If acting as estate agent | Check PPRA register |
| Fidelity Fund Certificate | If earning property commission | Check with PPRA |
| FSP License | If providing financial advice | Check FSCA FSP search |
| FICA Compliance | Anti-money laundering | Company policy review |
| POPIA Compliance | Data protection | Privacy policy review |

### Likely Required

Based on business model analysis:

1. **PPRA Registration** - The 5% sourcing fee on property transactions appears to be commission
2. **FSP License** - Financial advice/calculations on bonds and investments
3. **FICA Compliance** - Property transactions > R25,000 require FICA compliance

---

## 7. Recommendations

### For Ezra (InvestRand)

1. **Clarify Regulatory Position**
   - Verify PPRA registration status
   - Consult with compliance attorney on FSP requirements
   - Document "spotter's fee" vs "commission" distinction if relying on that

2. **Define Technology Requirements from Business Perspective**
   - How should deals actually close through the platform?
   - How should the 5% fee be tracked and collected?
   - What CRM integration is essential for lead management?

3. **Question Develutions on Business Functionality**
   - Financial calculations at 35% but claimed 55-60% overall progress?
   - CRM at 0% but this is how deals close?
   - Is the rebuild addressing the actual business gaps?

### For Due Diligence

1. **Regulatory Verification Required** - Cannot assess platform without knowing regulatory status
2. **Business Model Clarity Required** - How does a deal actually close today?
3. **Technology Assessment Requires Business Context** - Is Develutions building what the business needs?

---

## Sources

### Regulatory
- [FSCA Licensing](https://www.fsca.co.za/Regulated%20Entities/Pages/Licensing-and-Registration.aspx)
- [PPRA Registration](https://theppra.org.za/myffc/registration)
- [CISCA](https://www.saflii.org/za/legis/consol_act/cisca2002403/)
- [NASASA Stokvel Framework](https://www.nasasa.co.za/regulation/stokvel-regulatory-framework/)
- [Property Practitioners - Spotters Fees](https://propertyprofessional.co.za/2021/05/13/spotters-and-the-property-practitioners-act/)

### Competitors
- [EasyProperties](https://properties.easyequities.co.za/)
- [Crowdprop](https://crowdprop.co.za/)
- [SA PropTech Market 2025](https://jtbconsulting.co.za/blog/south-africa-proptech-fintech-market-2025/)

### InvestRand
- [Disrupt Africa - InvestRand Profile](https://disruptafrica.com/2024/03/26/how-investrand-is-helping-young-south-africans-get-clever-with-property-investments/)
- [InvestRand Website](https://www.investrand.co.za)

---

*This analysis is for due diligence purposes. Regulatory compliance should be verified with appropriate legal counsel.*
