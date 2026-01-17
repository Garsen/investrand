# InvestRand Platform Gap Analysis Report

**Date:** 17 January 2026
**Prepared for:** Ezra Rasethe (InvestRand)
**Purpose:** Independent assessment of platform status vs contracted specifications

---

## Executive Summary

This report compares the **contracted/specified features** (from Develutions' reverse-engineered documentation) against **observed platform behaviour** from browser automation testing. The analysis also evaluates Develutions' recommendation for a full code migration.

### Key Findings

1. **The existing platform appears functional** for core investor workflows (viewing properties, dashboard access)
2. **Empty states exist** in Portfolio and Agreements pages (no user-facing content)
3. **All properties show "Sold Out"** - no active investment opportunities visible
4. **Critical admin functions untested** - require admin credentials
5. **The full code migration recommendation is questionable** - existing stack (Vue 2/Django) is not inherently problematic

---

## 1. Platform Inventory - Observed vs Specified

### 1.1 Public Pages

| Feature | Specification (REQ-PLM-011) | Observed | Status |
|---------|----------------------------|----------|--------|
| Property Discovery | Search/filter published listings | Properties page with 4 listings visible | ⚠️ PARTIAL |
| Property Filtering | Location, type, price range, rental | **NOT observed** - no filter controls visible | ❌ GAP |
| Listing Details | Photos, description, address, investment metrics | All components present | ✅ OK |
| Unauthenticated Access | Browse listings read-only | Confirmed | ✅ OK |

### 1.2 Investor Dashboard (Authenticated)

| Feature | Specification | Observed | Status |
|---------|---------------|----------|--------|
| Dashboard Home | Welcome message, summary cards | Present | ✅ OK |
| Portfolio Page (REQ-PFM-001) | All investments/interests | **EMPTY** - no content | ⚠️ UNTESTED |
| Agreements Page (REQ-PFM-002) | Contract execution history | **EMPTY** - no content | ⚠️ UNTESTED |
| Profile Management (REQ-UAM-003) | Edit contact details | Present (first name, last name, email, phone) | ✅ OK |
| Password Change | Reset password internally | **NOT visible** in profile settings | ❌ GAP |

### 1.3 Property Listing Features

| Feature | Specification | Observed | Status |
|---------|---------------|----------|--------|
| Property Cards | Name, location, price, status | Present | ✅ OK |
| Status Badge | "Sold Out" indicator | All 4 properties show "Sold Out" | ⚠️ CONCERN |
| Investment Metrics | Min investment, expected return, period | Present (R1,000 / 12% / 36 months) | ✅ OK |
| Photo Gallery | Hero image, gallery | Hero image present | ✅ OK |
| Documents Tab | Leases, reports, offers | Tab visible | ⚠️ UNTESTED |

### 1.4 Missing/Untested Features

The following **Must Have** features from the specification could not be observed or tested:

| Requirement | Feature | Reason |
|-------------|---------|--------|
| REQ-PLM-001 | Create Property Listing | Requires Sourcing Agent role |
| REQ-PLM-005 | Listing Approval Workflow | Requires Admin access |
| REQ-ADM-001 | Admin Listing Management | Requires Admin credentials |
| REQ-ADM-003 | User Account Management | Requires Admin credentials |
| REQ-INV-001-010 | Investment Calculations | No active investments to observe |
| REQ-NOT-001-006 | Notification System | Backend functionality |

---

## 2. Bug List Analysis

### 2.1 Ezra's Original Bug List (November 2025)

| # | Issue | Category | Can Verify? | Observed? |
|---|-------|----------|-------------|-----------|
| 1 | Permission to add/remove users internally | Admin | No - needs admin | Unknown |
| 2 | Ability to reset users' passwords internally | Admin | No - needs admin | Unknown |
| 3 | Listing approval feedback notifications | Admin | No - needs admin | Unknown |
| 4 | Create "Sales Manager" role | Admin | No - needs admin | Unknown |
| 5 | Listing agents change statuses post-live | Agent | No - needs agent role | Unknown |
| 6 | Inquiry sync with ActiveCampaign/Notion | Integration | No - backend | Unknown |
| 7 | ROI formula not matching financial model | Calculation | Partial - no active investment | ⚠️ |
| 8 | Bond repayment not recalculating | Calculation | Partial - no active investment | ⚠️ |
| 9 | Users not receiving password reset emails | Email | No - backend | Unknown |
| 10 | Display full property identifiers | UI | Not visible on investor portal | Unknown |
| 11 | Listing agents view assigned addresses | Agent | No - needs agent role | Unknown |

### 2.2 Additional Reported Bugs (December 2025)

From progress notes, these additional bugs were reported:

| # | Issue | Develutions' Claim | Verifiable? |
|---|-------|-------------------|-------------|
| 1 | Tax Certificate Download | Fixed ✓ | No |
| 2 | Password Reset Internal | Fixed ✓ | No - not visible in UI |
| 3 | Property Deletion | Fixed ✓ | No - needs admin |
| 4 | Property Adding | Fixed ✓ | No - needs agent |
| 5 | Transaction Editing | Fixed ✓ | No - needs admin |
| 6 | Investor Deletion | Fixed ✓ | No - needs admin |
| 7 | OTP Error | Needs clarification | No |
| 8 | Interest Calculation | In progress | No |
| 9 | CMS Updates | Fixed ✓ | No |
| 10 | Password Reset Emails | Fixed ✓ | Not visible |
| 11 | Tax Reg Field | Fixed ✓ | No |

**Observation:** Most bug fixes claimed by Develutions cannot be independently verified through the investor portal alone.

---

## 3. Code Migration Assessment

### 3.1 Current Stack
- **Frontend:** Vue.js 2.x
- **Backend:** Django 4.2.15, Python 3.9/3.12
- **API:** Django REST Framework + GraphQL (Graphene-Django)
- **Database:** MySQL (production), SQLite (dev)
- **Infrastructure:** AWS Lambda (Zappa), S3, af-south-1 region

### 3.2 Proposed Stack (Develutions)
- **Frontend:** React 18 + TypeScript + Vite
- **Backend:** Spring Boot 3.4.1 + Java 21
- **Database:** Unchanged

### 3.3 Migration Necessity Analysis

| Argument For Migration | Counter-Argument |
|------------------------|------------------|
| Vue 2 is end-of-life (Dec 2023) | Vue 2 → Vue 3 migration is well-documented and less risky |
| Django is "legacy" | Django 4.2 is current LTS, supported until April 2026 |
| Security concerns | Can be addressed with patches, not full rewrite |
| Performance issues | Can be optimized without changing framework |

### 3.4 Migration Risk Assessment

| Risk | Severity | Notes |
|------|----------|-------|
| Complete system rebuild | HIGH | 6-12 months minimum for feature parity |
| Business logic recreation | HIGH | All calculation rules must be reimplemented |
| Data migration | MEDIUM | MySQL → MySQL should be straightforward |
| Testing coverage reset | HIGH | All test cases must be rewritten |
| Knowledge transfer | HIGH | New team unfamiliar with business logic |
| Integration recreation | MEDIUM | ActiveCampaign, Telegram, S3 all need new implementations |

### 3.5 Alternative Approaches

1. **Vue 2 → Vue 3 Migration**
   - Estimated effort: 2-4 weeks for frontend
   - Uses official migration tools
   - Preserves existing business logic

2. **Incremental Modernization**
   - Fix bugs in existing codebase
   - Upgrade dependencies (Django 4.2 → 5.x when ready)
   - Add new features to existing stack

3. **Hybrid Approach**
   - New features in modern stack
   - Gradual replacement of legacy components
   - Maintain existing functionality during transition

---

## 4. Recommendations

### 4.1 Immediate Actions

1. **Obtain Admin Credentials** - Critical for verifying bug fixes and testing admin functionality
2. **Test Claimed Bug Fixes** - Verify each "Fixed ✓" item with actual testing
3. **Document Active Listings** - Currently all show "Sold Out", need to understand if this is data issue or bug

### 4.2 Technical Due Diligence Questions

Ask Develutions to clarify:

1. **Why full migration vs incremental?** - What specific technical issues require complete rebuild?
2. **Business logic preservation** - How will 3,800+ lines of calculation logic be migrated without errors?
3. **Data migration plan** - Detailed approach for preserving existing user/listing data
4. **Rollback strategy** - What happens if the new system fails?
5. **Timeline realism** - 55-60% progress after 1 month is aggressive; when is production-ready?

### 4.3 Suggested Comparison Criteria for Other Vendors

For the standardised brief to compare development houses:

| Criteria | Weight |
|----------|--------|
| Approach to existing bugs (fix vs rebuild) | 25% |
| Timeline to production-ready state | 20% |
| Preservation of existing business logic | 20% |
| Cost relative to scope | 15% |
| Ongoing support model | 10% |
| South African presence/timezone | 10% |

---

## 5. Summary of Gaps

### Critical Gaps (Must Address)
1. ❌ Password reset not visible in user settings
2. ❌ Property filtering not implemented on Properties page
3. ⚠️ Portfolio page empty (unclear if data issue or bug)
4. ⚠️ Agreements page empty (unclear if data issue or bug)

### Untestable Without Admin Access
- User management
- Property creation/deletion
- Approval workflow
- Transaction editing
- All admin dashboard functions

### Requires Further Investigation
- Calculation accuracy (ROI, bond repayment)
- Email delivery (password reset, notifications)
- CRM integration (ActiveCampaign sync)
- All Develutions claimed bug fixes

---

## Appendix: Document Sources

1. **Requirements Specification** - 80 pages, reverse-engineered from codebase
2. **Business Rules Specification** - 50 pages, calculation and workflow rules
3. **Email Thread** - Ezra's original scope, Develutions status updates
4. **Browser Automation** - Live platform testing via investrand.co.za

---

*Report generated as part of independent technical due diligence review.*
