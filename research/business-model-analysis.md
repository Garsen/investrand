# InvestRand Business Model Analysis

**Date:** 17 January 2026
**Purpose:** Assess whether the technical specification supports the business model

---

## The Fundamental Question

Does the specification that Develutions produced actually articulate and support InvestRand's business model?

**Answer: No.** The specification documents what code exists, not how it supports the business.

---

## What the Specification Describes

The specification describes a **property listing platform** with:
- Property discovery and search
- Financial calculators (ROI, bond repayment, rental yield)
- User registration with "Proposal to Service" (terms & conditions)
- Admin approval workflows for listings
- Sourcing agent listing creation

---

## What's Explicitly OUT OF SCOPE

> "Property transaction processing (escrow, payments)" - OUT OF SCOPE

This is critical. The platform doesn't process actual investment transactions.

---

## What's Listed as FUTURE

- "Express Interest" functionality - not fully implemented
- Investment agreements - only "Proposal to Service" exists (which is just T&Cs)

---

## The Business Model Disconnect

### Stated Business Goals
- "Facilitate R500M in property transactions annually by year 3"
- "25% of listings result in agreements"
- Revenue: 5% sourcing fee (minimum R30,000) per transaction

### The Gap
**How does an investor actually invest?**

If an investor sees a property on InvestRand and wants to invest:
1. What do they click?
2. How do they commit funds?
3. What agreement do they sign? (Investment agreement doesn't exist)
4. How does InvestRand collect the 5% sourcing fee?
5. How is the transaction processed? (Out of scope)

**The specification doesn't answer any of these questions.**

---

## What InvestRand Actually Appears To Be

Based on the specification, InvestRand is a **lead generation platform**, not an **investment transaction platform**:

- Investors browse listings
- Investors see financial projections
- Investors... contact someone? (Express Interest is "future")
- Deal closes... offline? Through lawyers? Email?
- Sourcing fee collected... somehow?

The platform is a marketing tool with financial calculators. The actual investment transaction happens elsewhere.

---

## What Develutions Is Building

Develutions is rebuilding the same structure in a new tech stack:

| Component | Progress | Business Criticality |
|-----------|----------|---------------------|
| Frontend/Backend modernisation | 75-80% | Infrastructure (no business value) |
| Financial Calculations | 35% | **CORE VALUE** - barely started |
| CRM Integrations | 0% | Lead management - not started |
| Investment transaction flow | Out of scope | **THE ACTUAL BUSINESS** |

They're rebuilding the container without ensuring the contents work, and without addressing the fundamental gap of how investments actually happen.

---

## Questions That Should Have Been Asked

Before any development work, these questions needed answers:

1. **What is the actual investor journey** from "I see this property" to "I own a share"?

2. **How does that journey generate revenue** for InvestRand?

3. **What technology is required** to support that journey?

4. **What's missing from the current platform** that prevents scaling?

5. **Is the current platform architecture fundamentally broken**, or does it just need bug fixes and the transaction flow built out?

6. **If transaction processing is "out of scope", how does the business actually work?** Is this a platform business or a services business with a website?

---

## The Real Issue

This is not a technical problem. This is a business problem.

**The failing within InvestRand:** Not articulating clearly how technology should support the business model and enable scale.

**The failing within Develutions:** Just came to build something. Didn't ask the fundamental questions: Why are we doing this? How does it support the business?

**The cost implication:** Develutions is charging significant money (relative to InvestRand's revenue) to rebuild infrastructure that doesn't address the core business need.

---

## Recommendations

### Before Any More Development

1. **Define the investor journey end-to-end** - from discovery to completed investment
2. **Clarify the revenue model** - when and how is the sourcing fee collected?
3. **Determine if transaction processing should be in scope** - this changes everything
4. **Assess whether a rebuild is necessary** or if the existing platform just needs:
   - Bug fixes
   - Vue 2 → Vue 3 upgrade
   - The investment transaction flow built out

### Questions for Develutions

1. How will your rebuild enable InvestRand to scale to R500M in transactions?
2. Where in your architecture is the investment transaction flow?
3. Why is financial calculations only 35% complete if that's the core value proposition?
4. Why is CRM integration 0% complete if lead management is how deals close?

### Questions for Ezra

1. How do investors currently invest? What's the process?
2. How do you currently collect sourcing fees?
3. What specifically prevents you from scaling today?
4. Is the problem the technology, or the business process?

---

*This analysis focuses on business-technology alignment, not technical assessment.*
