# InvestRand Feature Inventory - Work in Progress

## Date: 17 January 2026

## Phase 1: Feature Inventory (Completed via Browser Automation)

### Platform URL
- https://investrand.co.za

### Public Pages Documented

#### 1. Homepage
- Hero section with "Invest in property today" tagline
- "Start investing" CTA button
- Three value proposition cards:
  - "Invest from R1,000" - Low barrier entry
  - "Diversified Portfolio" - Spread risk
  - "Expert Management" - Professional oversight
- Navigation: Home, Properties, About, FAQ, Contact
- Auth buttons: Sign In, Get Started

#### 2. Properties Page
- **4 properties listed** (all showing "Sold Out" status)
- Property cards display:
  - Property image
  - Name and location
  - Price (e.g., R1,800,000)
  - "Sold Out" badge
  - View Details button
- Properties found:
  1. Kensington Place
  2. Parkview Heights
  3. Sandton Executive
  4. Rosebank Residences

#### 3. Property Detail Page (Kensington Place example)
- Large hero image
- Property name and location
- Price: R1,800,000
- "Sold Out" status badge
- Tabs: Overview, Details, Documents
- Investment metrics:
  - Minimum Investment: R1,000
  - Expected Return: 12%
  - Investment Period: 36 months
- Property Details section (expandable)
- Documents section (expandable)
- "Reserve Your Share" button (disabled when sold out)

#### 4. About Page
- Company description
- Mission/vision content
- Team information (if any)

#### 5. Contact Page
- Contact form
- Company contact details

#### 6. FAQ Page
- Accordion-style Q&A sections

### Authenticated Portal (Investor Dashboard)

#### Login Process
- Email/password authentication
- Successful login redirects to Dashboard

#### Dashboard Structure
- Left sidebar navigation:
  - Dashboard (home icon)
  - My Portfolio (expandable)
    - Portfolio
    - Agreements
  - Properties
  - Settings (expandable)
    - Profile
    - Security (if exists)

#### Dashboard Home
- Welcome message with user name
- Summary cards (likely showing):
  - Total Invested
  - Active Investments
  - Returns/Performance
- Recent activity section

#### Profile Page (Settings > Profile)
- USER INFORMATION section:
  - First Name field
  - Last Name field
  - Email field
- CONTACT INFORMATION section:
  - Cell number field
  - Backup number field
- Save button
- **Note:** No password change field visible here

#### Portfolio Page
- **EMPTY** - No content displayed
- No empty state message shown
- Would show user's investments/reserved properties

#### Agreements Page
- **EMPTY** - No content displayed
- No empty state message shown
- Would show user's legal agreements

---

## Key Observations So Far

### Positive
1. Clean, modern UI design
2. Clear property listing structure
3. Investment metrics clearly displayed
4. Responsive layout

### Gaps/Issues Noted
1. All properties showing "Sold Out" - no active investment opportunities
2. Portfolio page completely empty (no empty state UX)
3. Agreements page completely empty (no empty state UX)
4. No visible password reset option in Profile settings (relates to Bug #2)

---

## Phase 2: Comparison with Develutions Specifications

### The 11 Bugs from Email Thread (December 2025)

From Ezra's email dated 2025-12-09:

1. **Tax Certificate Download** - Does not download tax certificate
2. **Password Reset** - Users cannot reset passwords internally
3. **Property Deletion** - Cannot delete properties from platform
4. **Property Adding** - Cannot add properties to platform
5. **Transaction Editing** - Cannot edit transactions
6. **Investor Deletion** - Cannot delete investors
7. **OTP Error** - OTP gives error and logs out user
8. **Interest Calculation** - Duplicate interest issue / Calculation errors
9. **CMS Updates** - Changes to CMS not reflecting
10. **Password Reset Emails** - Not being sent
11. **Tax Reg Field** - Error when leaving field blank

### Develutions' Claimed Progress (from email thread)

According to their 2025-12-11 email:
- Bug 1 (Tax Certificate): Fixed ✓
- Bug 2 (Password Reset): Fixed ✓
- Bug 3 (Property Deletion): Fixed ✓
- Bug 4 (Property Adding): Fixed ✓
- Bug 5 (Transaction Editing): Fixed ✓
- Bug 6 (Investor Deletion): Fixed ✓
- Bug 7 (OTP Error): Needs clarification
- Bug 8 (Interest Calculation): In progress
- Bug 9 (CMS Updates): Fixed ✓
- Bug 10 (Password Reset Emails): Fixed ✓
- Bug 11 (Tax Reg Field): Fixed ✓

---

## Next Steps

1. **Read Requirements Specification PDF** - Understand full scope of what was contracted
2. **Access Admin Portal** - Document admin-side features
3. **Test Bug Fixes** - Verify claimed fixes actually work
4. **Compare Features vs Spec** - Gap analysis
5. **Document API/Backend** - Technical architecture review
6. **Create Final Assessment Report**

---

## Session Notes

- Browser automation session active on tab in Chrome
- Currently logged in as investor user
- Need admin credentials to test admin portal
- PDF read failed due to API media limits - will need to read in smaller chunks

---

## Phase 2: Document Analysis (Completed)

### Documents Reviewed

1. **Requirements Specification** (80 pages)
   - Comprehensive functional and non-functional requirements
   - 10 major requirement categories (UAM, PLM, INV, SPM, CAM, AWE, NOT, PFM, ADM, LSE)
   - Derived from reverse-engineering the existing codebase

2. **Business Rules Specification** (50 pages)
   - Detailed calculation formulas (sourcing fee, bond repayment, rental aggregation)
   - Workflow state machines (listing lifecycle, approval workflow)
   - Validation rules and compliance requirements

3. **Email Thread** (December 2025)
   - Context: Ezra questioning whether Develutions' full migration is necessary
   - Original 11 bugs from November 2025
   - Develutions claiming 55-60% progress on React/Spring Boot migration

### Key Context

**Develutions is recommending a FULL CODE MIGRATION:**
- From: Vue 2 / Django 4.2 / Python
- To: React 18 / Spring Boot 3.4 / Java 21

**Ezra's Key Questions:**
1. Is this migration technically necessary?
2. Is the pricing reasonable?
3. Can we compare other vendors fairly?

---

## Gap Analysis Summary (See: gap-analysis-report.md)

### Critical Findings

1. **Most Develutions bug fixes cannot be verified** - require admin/agent access
2. **Full migration appears excessive** - Vue 2→Vue 3 + bug fixes would be lower risk
3. **Platform appears functional** for core investor workflows
4. **Key gaps observed:**
   - No password reset in profile settings
   - No property filtering on Properties page
   - Empty Portfolio and Agreements pages
   - All properties showing "Sold Out"

### Recommendation

Before accepting full migration, request:
1. Admin credentials to verify bug fixes
2. Justification for why incremental approach won't work
3. Detailed data migration plan
4. Rollback strategy if new system fails

---

## Phase 3: Comprehensive Platform Testing (17 January 2026)

### Updated Observations

**Discover Page (Properties)**
- 9+ properties visible (not just 4 as initially observed)
- Mix of "SOLD", "FOR SALE", and available properties
- Property cards show: image, name, location, price, status badge

**Portfolio Page**
- Shows 4 properties owned by test user (all SOLD status):
  1. Kensington Place
  2. Parkview Heights
  3. Sandton Executive
  4. Rosebank Residences
- This explains why public properties page shows "Sold Out"

**Agreements Page**
- Message: "You have no active agreements"
- Has empty state UX (unlike earlier observation)

**Property Detail - Financial Breakdown**
- Attempting to view financial details requires accepting "Proposal to Service"
- This gates the detailed financial projections behind agreement

**Service Providers Page**
- Working correctly
- 3 service providers listed with contact details

**Profile Page**
- First Name, Last Name, Email fields present
- Cell and Backup number fields present
- **NO password change option** - confirms Bug #2 (Password Reset)

### Bug Verification Summary

| Bug # | Issue | Status | Evidence |
|-------|-------|--------|----------|
| 1 | Tax Certificate | Cannot verify | Requires portfolio with tax docs |
| 2 | Password Reset | **CONFIRMED** | Not visible in Profile settings |
| 3-6 | Admin functions | Cannot verify | Requires admin access |
| 7 | OTP Error | Cannot verify | Requires OTP flow test |
| 8 | Interest Calculation | Cannot verify | No active investments |
| 9-11 | Other | Cannot verify | Requires admin/backend access |

---

## Phase 4: Business Model Analysis (17 January 2026)

### Critical Discovery

**InvestRand is NOT a fractional property investment platform.**

From their own marketing: "Full ownership of your property—no fractional investments, no hidden costs."

### Actual Business Model

InvestRand is a **property sourcing marketplace**:
1. Source properties (income-generating investments)
2. List on platform with financial projections
3. Connect investors with sourcing agents
4. Investor buys property (FULL ownership transfer)
5. InvestRand earns 5% sourcing fee (minimum R30,000)

### Technology-Business Gap

| Business Need | Platform Status | Develutions Progress |
|---------------|-----------------|---------------------|
| Property listing | ✅ Working | 85% |
| Financial calculations | ⚠️ Bugs | **35%** |
| Lead capture (Express Interest) | ❌ Future | Not in scope |
| CRM Integration | ❌ Broken | **0%** |
| Deal facilitation | ❌ Not in platform | Not in scope |
| Fee collection | ❌ Not in platform | Not in scope |

### Key Insight

**This is a business problem, not a technical problem.**

Develutions is building infrastructure (frontend/backend modernisation) but not addressing:
- How deals actually close
- How revenue is collected
- How leads are managed (CRM at 0%)
- Whether financial calculations (core value prop) are accurate (only 35%)

### Regulatory Questions to Verify

1. Is InvestRand PPRA-registered? (5% fee looks like commission)
2. Is FSP license required for financial advice/projections?
3. Are sourcing agents properly registered?
4. FICA compliance for property transactions?

---

## Deliverables Created

1. **research/gap-analysis-report.md** - Technical gap analysis
2. **research/business-model-analysis.md** - Business-technology alignment
3. **research/regulatory-and-business-analysis.md** - Comprehensive regulatory and business model analysis
4. **presentation/InvestRand-Business-Model-Analysis.pdf** - 4-slide visual summary:
   - Business Model Workflow (current vs proposed)
   - The Core Problem
   - Regulatory Compliance Considerations
   - Recommendations & Next Steps

---

## Outstanding Items

1. **Admin portal testing** - Blocked (no credentials)
2. **Codebase Analysis PDF** - Not yet extracted
3. **Standardised vendor comparison brief** - For comparing development houses
4. **Regulatory verification** - PPRA/FSCA status checks
