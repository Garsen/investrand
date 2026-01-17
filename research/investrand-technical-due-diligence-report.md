# InvestRand Technical Due Diligence Report

**Prepared for:** Ezra Rasethe, CEO, InvestRand
**Prepared by:** Ampersand Insights
**Date:** 17 January 2026

---

## Executive Summary

This report presents findings from an independent technical due diligence review of InvestRand's platform and Develutions' proposed code migration.

**Key Findings:**

1. **The platform rebuild does not address InvestRand's core business needs.** Develutions is modernising infrastructure while business-critical functions remain incomplete or out of scope.

2. **Progress is concentrated in infrastructure, not business functionality.** Financial calculations (the core value proposition) are at 35%. CRM integration (how deals close) is at 0%. These figures come from Develutions' own progress report.

3. **The full code migration approach carries significant risk** with unclear justification for why incremental modernisation would not suffice.

4. **Regulatory questions require attention** before further technology investment. The 5% sourcing fee structure may require PPRA registration and potentially FSP licensing.

**Recommendation:** Before proceeding with any development path, clarify the business requirements, verify Develutions' claimed progress, and confirm regulatory compliance status.

---

## 1. Scope & Approach

### 1.1 What We Were Asked To Do

Ezra Rasethe engaged this review to answer three questions:

1. Is Develutions' recommendation for a full code migration technically sound and necessary?
2. Is the pricing reasonable relative to scope?
3. Can we create a standardised brief to compare development houses fairly?

*Source: Ezra Rasethe email to Chand Tjingaete, 8 December 2025*

### 1.2 How We Conducted This Review

| Activity | Method | Date |
|----------|--------|------|
| Document analysis | Reviewed Requirements Specification (80 pages), Business Rules Specification (50 pages), email correspondence | January 2026 |
| Platform testing | Browser-based testing of investrand.co.za as authenticated investor | 17 January 2026 |
| Business model research | Web research on InvestRand, competitors, regulatory framework | 17 January 2026 |
| Progress assessment | Analysis of Develutions' self-reported status | Based on 27 December 2025 email |

### 1.3 Limitations

- **No access to Develutions' code.** We cannot verify their claimed progress; we can only analyse their self-reported status.
- **No admin portal access.** Many bug fixes claimed by Develutions require admin credentials to verify.
- **Regulatory status unverified.** PPRA and FSCA registration status requires direct verification with regulators or legal counsel.

---

## 2. Understanding InvestRand's Business Model

### 2.1 What InvestRand Is (And Is Not)

**InvestRand is a property sourcing marketplace, not a fractional investment platform.**

This is a critical distinction that affects both the technology requirements and regulatory analysis.

| Aspect | Fractional Platform (e.g., EasyProperties) | InvestRand (Actual Model) |
|--------|-------------------------------------------|---------------------------|
| Ownership | Fractional shares in SPV | Full property ownership |
| Minimum investment | As low as R1 | Full property deposit/bond |
| Revenue model | Management fees on pooled funds | 5% sourcing fee per transaction |
| Regulatory framework | FSP license, CISCA registration | Potentially PPRA, possibly FAIS |

**Evidence:**

From InvestRand's own website (investrand.co.za):
> "With investRand, you get full ownership of your property—no fractional investments, no hidden costs."

From Disrupt Africa article, 26 March 2024:
> InvestRand charges a 5% sourcing fee (minimum R30,000) per transaction.

*Sources: investrand.co.za; Disrupt Africa, "How InvestRand is helping young South Africans get clever with property investments", 26 March 2024*

### 2.2 How the Business Works

Based on public information and platform analysis, InvestRand operates as follows:

```
SOURCING → LISTING → APPROVAL → DISCOVERY → INTEREST → DEAL → REVENUE
   │          │          │          │           │        │        │
   ▼          ▼          ▼          ▼           ▼        ▼        ▼
 Agent     Platform   Admin      Investor    Express   Close   Collect
 finds     displays   reviews    browses     interest  sale    5% fee
 property  listing    quality    options     (HOW?)    (HOW?)  (HOW?)
```

**The platform currently supports steps 1-4. Steps 5-7 are either incomplete or not in scope.**

### 2.3 Stated Business Metrics

From Disrupt Africa (March 2024):
- 1,000+ users
- 60% repeat customers
- R1M+ revenue in first year
- Profitable since inception
- Bootstrapped (no external funding)
- Median customer age: 33 years
- ~50% first-time property investors

*Source: Disrupt Africa, 26 March 2024*

---

## 3. Current Platform Assessment

### 3.1 Platform Testing Findings

We tested the live platform (investrand.co.za) on 17 January 2026.

**What Works:**

| Feature | Status | Observation |
|---------|--------|-------------|
| Property listing display | ✓ Working | 9+ properties visible with images, prices, status |
| Investor dashboard | ✓ Working | Welcome message, navigation, summary cards |
| Portfolio view | ✓ Working | Shows owned properties (4 in test account) |
| Service providers marketplace | ✓ Working | 3 providers listed with contact details |
| User profile management | ✓ Partial | Can edit name, email, phone |

**What Does Not Work or Is Missing:**

| Feature | Status | Observation |
|---------|--------|-------------|
| Password reset in profile | ✗ Missing | No option visible in Settings > Profile |
| Express Interest functionality | ✗ Future | Listed as "future" in specifications |
| Property filtering | ✗ Missing | No filter controls on Properties page |
| Financial breakdown access | Gated | Requires accepting "Proposal to Service" |

### 3.2 Bug Verification

Ezra's original bug list (November 2025) contained 11 items. We could verify only one directly:

| Bug | Description | Verification Status |
|-----|-------------|---------------------|
| #2 | Password reset unavailable internally | **CONFIRMED** — not visible in profile settings |
| #1, #3-6 | Admin functions | Cannot verify — requires admin access |
| #7-8 | Calculation errors (ROI, bond) | Cannot verify — requires active investment |
| #9-11 | Email, CMS, validation | Cannot verify — requires backend access |

**Conclusion:** Most of Develutions' claimed bug fixes cannot be independently verified without admin credentials or code access.

---

## 4. Develutions Progress Assessment

### 4.1 Claimed Overall Progress

Develutions reports **55-60% overall project progress**.

*Source: Mokhina Maitin (Develutions) email to Ezra Rasethe, 27 December 2025, Subject: "Project Status"*

### 4.2 Detailed Progress Breakdown

The following table is reproduced directly from Develutions' progress report:

| Phase | Category | Status | Progress |
|-------|----------|--------|----------|
| 1.5 | Frontend Modernisation | ADVANCED | 80% |
| 1.6 | Backend Modernisation | ADVANCED | 75% |
| 2.5 | Property Display | IN PROGRESS | 85% |
| 2.2 | User Management | IN PROGRESS | 60% |
| 2.3 | Approval Workflow | IN PROGRESS | 55% |
| 1.3 | Database & Architecture | IN PROGRESS | 50% |
| 1.1 | Security Hardening | PARTIAL | 40% |
| **2.1** | **Financial Calculations** | **SCAFFOLDED** | **35%** |
| 3.2 | System Documentation | IN PROGRESS | 40% |
| 3.1 | Monitoring Implementation | PARTIAL | 25% |
| **2.4** | **CRM Integrations** | **NOT STARTED** | **0%** |

*Source: Develutions Project Status email, 27 December 2025*

### 4.3 Analysis: Where Progress Is Concentrated

**High progress (60-85%):** Frontend, backend, property display, user management — *infrastructure*

**Low progress (0-35%):** Financial calculations, CRM integrations — *business-critical functions*

The 55-60% overall figure is achieved through strong infrastructure progress while the functions that directly support InvestRand's business model and revenue generation remain incomplete.

### 4.4 Specific Concerns

**Financial Calculations (35%, "SCAFFOLDED")**

This is InvestRand's core value proposition — helping investors understand ROI, bond repayments, and rental yields. "SCAFFOLDED" means the structure exists but the calculation logic is not implemented.

Ezra's original bug list included:
- Bug #7: "ROI formula on the platform not matching our financial model"
- Bug #8: "Bond repayment not recalculating consistently"

These bugs are in the 35%-complete component.

*Source: Ezra Rasethe email, 18 November 2025; Develutions status report, 27 December 2025*

**CRM Integrations (0%, "NOT STARTED")**

Ezra's original bug list included:
- Bug #6: "Re-integrate inquiries so contact details sync correctly with ActiveCampaign/Notion"

This is how leads are managed and deals are closed. It remains at 0%.

*Source: Ezra Rasethe email, 18 November 2025; Develutions status report, 27 December 2025*

---

## 5. Technology-Business Alignment

### 5.1 The Core Question

Does Develutions' work enable InvestRand to scale toward its stated goal of R500M in property transactions?

### 5.2 Gap Analysis

| Business Need | Required For | Platform Status | Develutions Progress |
|---------------|--------------|-----------------|---------------------|
| Property listing | Attract investors | Working | 85% |
| Financial projections | Investor decision-making | Bugs reported | 35% |
| Lead capture | Convert interest to deals | "Future" feature | Not in scope |
| CRM integration | Manage deal pipeline | Broken | 0% |
| Deal facilitation | Close transactions | Not in platform | Not in scope |
| Fee collection | Generate revenue | Not in platform | Not in scope |

### 5.3 What Is Being Built vs What Is Needed

**What Develutions is building:**
- Modern React 18 frontend (80%)
- Spring Boot 3.4 backend (75%)
- UI component library (complete)
- API layer (complete)
- Authentication system (complete)

**What InvestRand needs to scale:**
- Accurate financial calculations (35%)
- Working CRM integration (0%)
- Lead capture and conversion (not in scope)
- Deal pipeline management (not in scope)
- Revenue collection mechanism (not in scope)

### 5.4 Observation

The rebuild focuses on modernising the technology container while the business functionality that would enable growth remains incomplete or explicitly out of scope.

---

## 6. Migration Approach Assessment

### 6.1 Current vs Proposed Stack

| Layer | Current | Proposed |
|-------|---------|----------|
| Frontend | Vue.js 2.x | React 18 + TypeScript |
| Backend | Django 4.2, Python | Spring Boot 3.4, Java 21 |
| Database | MySQL | MySQL (unchanged) |
| Infrastructure | AWS Lambda (Zappa) | Not specified |

### 6.2 Stated Rationale

Develutions' assessment documents cite:
- Vue 2 end-of-life (December 2023)
- Security concerns with legacy stack
- Performance constraints

*Source: Develutions Technical Assessment, November 2025*

### 6.3 Alternative Approaches Not Explored

| Approach | Description | Risk Level |
|----------|-------------|------------|
| Vue 2 → Vue 3 migration | Upgrade frontend using official migration tools | Lower |
| Incremental modernisation | Fix bugs, upgrade dependencies in existing stack | Lower |
| Hybrid approach | New features in modern stack, gradual replacement | Medium |
| Full migration | Complete rebuild in new stack (current approach) | Higher |

### 6.4 Migration Risk Factors

| Risk | Severity | Notes |
|------|----------|-------|
| Complete system rebuild | High | All business logic must be reimplemented |
| Business logic recreation | High | 3,800+ lines of calculation rules |
| Testing coverage reset | High | All test cases must be rewritten |
| Knowledge transfer | High | New codebase, new team learning curve |
| Data migration | Medium | MySQL → MySQL should be straightforward |
| Integration recreation | Medium | ActiveCampaign, Telegram, S3 need new implementations |

### 6.5 Questions for Develutions

1. Why is full migration necessary rather than Vue 2 → Vue 3 with bug fixes?
2. What specific technical issues in the current stack cannot be addressed incrementally?
3. What is the data migration plan and rollback strategy?
4. How will 3,800+ lines of business logic be verified in the new system?
5. When is the realistic production-ready date given current progress?

---

## 7. Regulatory Considerations

### 7.1 Why This Matters

Before investing further in technology, InvestRand should confirm its regulatory compliance. The business model has characteristics that may trigger registration requirements.

### 7.2 Property Practitioners Regulatory Authority (PPRA)

**The question:** Is the 5% sourcing fee commission on property sales?

| Factor | Observation |
|--------|-------------|
| Fee structure | 5% of transaction value (minimum R30,000) |
| Activity | Connecting buyers with properties |
| Legal framework | Property Practitioners Act 22 of 2019 |
| Requirement | Fidelity Fund Certificate (FFC) for earning commission |

**To verify:**
- Is InvestRand registered with PPRA?
- Is Ezra Rasethe (noted as former estate agent) currently registered?
- Are the sourcing agents on the platform PPRA-registered?

*Source: Property Practitioners Act 22 of 2019; PPRA registration requirements*

### 7.3 Financial Sector Conduct Authority (FSCA)

**The question:** Is InvestRand providing financial advice?

| Factor | Observation |
|--------|-------------|
| Platform activity | Calculates ROI, bond repayments, rental yields |
| Presentation | Helps investors make financial decisions |
| Connections | Links to financing options |
| Comparator | EasyProperties operates under FSP License 22588 |

**To verify:**
- Does presenting financial projections constitute financial advice under FAIS?
- Is FSP licensing required?

*Source: Financial Advisory and Intermediary Services Act (FAIS); FSCA licensing requirements*

### 7.4 What Is Not Applicable

**CISCA (Collective Investment Schemes Control Act):** Not applicable. InvestRand does not pool investor funds — each investor receives full property ownership.

### 7.5 Recommendation

Consult with a compliance attorney to verify regulatory status before further technology investment. Regulatory non-compliance could invalidate the business model regardless of technology quality.

---

## 8. Recommendations

### 8.1 Immediate Actions

| Priority | Action | Rationale |
|----------|--------|-----------|
| 1 | Verify Develutions' progress | Request code access or demonstration of completed work |
| 2 | Clarify regulatory status | Consult compliance attorney on PPRA/FSCA requirements |
| 3 | Define the investor journey | Document end-to-end process from discovery to completed investment |
| 4 | Clarify revenue collection | How is the 5% fee actually tracked and collected today? |

### 8.2 Questions for Ezra

Before evaluating any technology path:

1. How do investors currently invest? What is the actual process?
2. How do you currently collect the 5% sourcing fees?
3. What specifically prevents you from scaling today — technology or business process?
4. What is your PPRA registration status?

### 8.3 Questions for Develutions

1. How will this rebuild enable InvestRand to scale to R500M in transactions?
2. Where in the architecture is the investment transaction flow?
3. Why is financial calculations at 35% when this is the core value proposition?
4. Why is CRM integration at 0% when this is how deals are managed?
5. Why full migration versus Vue 2 → Vue 3 incremental approach?
6. What is the detailed data migration and rollback strategy?
7. What is the realistic timeline to production-ready?

### 8.4 Evaluating the Path Forward

| Option | Description | Consideration |
|--------|-------------|---------------|
| Continue with Develutions | Complete the migration | Verify progress first; clarify business functionality scope |
| Pause and reassess | Stop development, evaluate alternatives | Lower risk; may delay timeline |
| Change direction | Different vendor or approach | Requires clear requirements definition |

---

## 9. Summary

**The core issue is not technical — it is alignment between technology investment and business needs.**

Develutions is building infrastructure. InvestRand needs business functionality that enables growth.

Before any further investment:
1. Verify what has actually been built
2. Confirm regulatory compliance
3. Define what technology must deliver for the business to scale
4. Evaluate whether the current approach addresses those needs

---

## Appendix A: Document Sources

| Document | Source | Date |
|----------|--------|------|
| Initial engagement email | Ezra Rasethe to Chand Tjingaete | 8 December 2025 |
| Original bug list and scope | Ezra Rasethe to Develutions | 18 November 2025 |
| Technical assessment delivery | Develutions to Ezra Rasethe | 21 November 2025 |
| Project status report | Develutions to Ezra Rasethe | 27 December 2025 |
| Requirements Specification | Develutions | November 2025 |
| Business Rules Specification | Develutions | November 2025 |
| Platform testing | Ampersand Insights | 17 January 2026 |
| Business model research | investrand.co.za, Disrupt Africa | January 2026 |

## Appendix B: Platform Testing Screenshots

*Available upon request — captured during 17 January 2026 testing session*

## Appendix C: Regulatory Reference

| Regulator | Legislation | Relevance |
|-----------|-------------|-----------|
| PPRA | Property Practitioners Act 22 of 2019 | Commission on property transactions |
| FSCA | Financial Advisory and Intermediary Services Act | Financial advice and projections |
| FIC | Financial Intelligence Centre Act | FICA compliance for transactions > R25,000 |
| Information Regulator | Protection of Personal Information Act | Data handling (POPIA) |

---

*This report is provided for due diligence purposes. Regulatory compliance should be verified with appropriate legal counsel.*
