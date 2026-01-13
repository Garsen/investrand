# InvestRand Technical Due Diligence - Email Thread

## Context
Ezra Rasethe (InvestRand CEO) has engaged Chand Tjingaete to vet Develutions' technical assessment and provide guidance on their code migration recommendation.

---

## Email 1: Initial Request for Assistance
**From:** Ezra Rasethe <Ezra@investrand.co.za>
**To:** Chand Tjingaete <cftjingaete@gmail.com>
**Date:** Monday, 8 December 2025, 15:13
**Subject:** Fw: Next Steps: Phase 1 Technical Assessment, Roadmap Alignment & Required Access

Hello Chand,

Thank you for agreeing to assist me with vetting this development company.

Please find attached the report they shared with me.

The most important section is the investRand work breakdown—they are recommending a full code migration, which is a concern for me. I would greatly appreciate your guidance on whether this recommendation is technically sound and truly necessary.

I would also value your input on the pricing they've provided relative to the scope of work.

Additionally, I've identified five development houses I'd like to compare. To ensure a fair comparison, I need help putting together a standardised brief that I can send to all of them so we're comparing apples with apples. Please let me know if you are able to assist with this as well.

Thank you again for your support on this matter. I look forward to your guidance on the way forward.

Best Regards,
Ezra Rasethe

---

## Email 2: Develutions Technical Assessment Delivery
**From:** mokhina.maitin@develution.co.za
**To:** Ezra Rasethe
**Date:** Thursday, 21 November 2025, 08:30
**Subject:** Re: Next Steps: Phase 1 Technical Assessment, Roadmap Alignment & Required Access

Good morning, Ezra,

Please find attached the system and performance analysis, the work breakdown, and the accompanying technical documents. These include the code analysis, business rules, and business requirements derived from the existing code base. The work breakdown also outlines the costing for the two approaches we discussed.

Please see my company details below for the NDA:

- **Company Name:** Develutions (PTY) LTD
- **Registration Number:** 2016/419500/07
- **Address:** 325 Castellet Country Estate, Syringa Avenue, Broadacres, 2055
- **Email:** mokhina.maitin@develutions.co.za
- **Phone:** 079 634 1643

Please let me know if you need any further information.

Kind regards,
Mokhina Maitin

---

## Email 3: Ezra's Original Scope Request
**From:** Ezra Rasethe <Ezra@investrand.co.za>
**To:** mokhina.maitin@develutions.co.za
**CC:** Sales <sales@investrand.co.za>, Kim Hudson <KimH@investrand.co.za>
**Date:** Tuesday, 18 November 2025, 10:37
**Subject:** Next Steps: Phase 1 Technical Assessment, Roadmap Alignment & Required Access

Hello Mokhina,

Thank you again for the productive meeting today. I appreciate the clarity you brought to our discussion and your willingness to align the development roadmap with the immediate business needs.

As agreed, here is the consolidated way forward for Phase 1 and the next roadmap stages.

### 1. Phase 1 — Code Review & Technical Assessment

As discussed, Phase 1 is an assessment phase, not a development phase.

This includes a full review of:
- the platform source code
- AWS architecture and environment
- database structure
- current bug behaviour
- performance constraints
- any technical debt that may impact future development

The objective of Phase 1 is to provide:
- a clear technical diagnosis
- prioritised recommendations
- scoped work items for each future phase
- estimated timelines and cost ranges
- identification of any high-risk areas

Once we receive your recommendations, we will lock the scope for Phases 2–6 and proceed with development.

### 2. Bug List for Review (To Support Your Assessment)

Below is the consolidated list of bugs and functional issues we discussed. These will help you size the initial work and understand where the platform is currently creating friction:

1. Permission to add/remove users internally.
2. Ability to reset users' passwords internally.
3. Listing approval feedback notifications to multiple users.
4. Create a "Sales Manager" role with final-approval rights.
5. Listing agents to change listing statuses post-live (e.g., under offer, sold).
6. Re-integrate inquiries so contact details sync correctly with ActiveCampaign/Notion.
7. ROI formula on the platform not matching our financial model.
8. Bond repayment not recalculating consistently.
9. Users not receiving password reset emails.
10. Display full property identifiers (address, ERF/unit numbers) for SharePoint tracking.
11. Listing agents to view their own assigned property addresses on the platform.

You can include or exclude items from Phase 1 once you complete your assessment and confirm dependencies.

### 3. Roadmap Alignment (Updated Based on Meeting)

To confirm our shared understanding, the roadmap will follow this structure once Phase 1 is complete:

- **Phase 1** — Code Review & Technical Assessment
- **Phase 2** — Number Calculation Engine (MVP)
- **Phase 3** — Unified Upload System + Document Manager
- **Phase 4** — Workflow & Approvals Automation
- **Phase 5** — Internal Optimisation & Functional Enhancements
- **Phase 6** — Scraper Bot & Sourcing Automation

We will only proceed phase by phase, with no scope creep, and each phase must be stable before the next begins.

### 4. Access to Notion Boards

As requested, here are the Notion links for:

**A. User Feedback Kanban Board**
https://www.notion.so/93d87df9d03147ebb075a6066a135c29?v=be264f447a294318918d8e4bdf822a03&source=copy_link

**B. Release Train / Development Work Breakdown**
https://www.notion.so/1be9b7c1a3734f9a906d771d28bf7f49?v=85b13695861f4043a3385b8e74e65bf0&source=copy_link

You can use these for capturing notes, architectural decisions, task breakdowns, and development progress.

### 5. NDA for Access to All Systems

Although you already have access to AWS and the codebase, please sign the attached NDA so we can formalise access and proceed with the full technical assessment.

Kindly return the signed document at your earliest convenience.

### 6. Next Steps

1. Sign and return the NDA
2. Complete Phase 1 Technical Assessment
3. Share recommendations, risks, timelines, and cost estimates
4. Align on scope for Phases 2–6
5. Begin development after scope confirmation

Please let me know if you need anything else from my side (examples, edge cases, documentation, or clarification).

Thank you again for partnering with us on this. Resolving these constraints and improving the listing workflow is a critical enabler for our next stage of growth, and I appreciate your support and collaboration.

Successful Investing,
Ezra Rasethe

---

## Email 4: Project Status Update
**From:** Ezra Rasethe <Ezra@investrand.co.za>
**To:** Chand Tjingaete <cftjingaete@gmail.com>
**Date:** Saturday, 27 December 2025, 12:53
**Subject:** Fw: Project Status

Hi Brother Chand,

I hope you are well.

I wanted to give you up-to-date progress from the dev company.

Best Regards,
Ezra Rasethe

---

## Email 5: Develutions Project Status Report
**From:** mokhina.maitin@develution.co.za
**To:** Ezra Rasethe
**Date:** Saturday, 27 December 2025, 08:37
**Subject:** Project Status

### Executive Summary

The InvestRand Property Investment Platform modernization project has achieved substantial progress with the technology stack migration now well advanced. The new architecture replaces the legacy Vue 2/Django stack with a modern React 18/Spring Boot 3.4 stack, addressing critical security and performance concerns outlined in the Work Breakdown Structure.

**OVERALL PROJECT PROGRESS: 55-60%**

---

### Technology Stack Migration Status

#### Frontend Modernization (React 18 + TypeScript + Vite)
**Progress: 80% COMPLETE**

| Component | Status | Details |
|-----------|--------|---------|
| Project Setup | COMPLETE | Vite + TypeScript + Tailwind CSS |
| UI Component Library | COMPLETE | 18+ Radix UI components |
| State Management | COMPLETE | Zustand + TanStack Query |
| Authentication Pages | COMPLETE | Login, Register, Password Reset, Verify Email |
| Property Pages | COMPLETE | List, Detail, Create, Edit |
| Portfolio/Investment Pages | COMPLETE | Portfolio overview, Investment detail |
| User Management Pages | COMPLETE | Profile, Settings, Notifications |
| Service Provider Pages | COMPLETE | List and Detail views |
| Legal/Approval Pages | COMPLETE | Contracts, Approvals |
| Dashboard | COMPLETE | Main dashboard page |
| Public Pages | COMPLETE | Home, About, Contact, 404 |
| API Integration Layer | COMPLETE | 8 REST + GraphQL service modules |
| Testing Setup | COMPLETE | Vitest + Playwright configured |

#### Backend Modernization (Spring Boot 3.4.1 + Java 21)
**Progress: 75% COMPLETE**

| Component | Status | Details |
|-----------|--------|---------|
| Project Setup | COMPLETE | Spring Boot 3.4.1 + Java 21 |
| Domain Models | COMPLETE | All 8 modules (110 Java files) |
| Service Layer | COMPLETE | Business logic |
| REST Controllers | COMPLETE | All CRUD endpoints implemented |
| JWT Authentication | COMPLETE | Full auth flow + account lockout |
| API Documentation | COMPLETE | SpringDoc/OpenAPI |
| Database Migrations | COMPLETE | Flyway configured |
| AWS S3 Integration | COMPLETE | File storage ready |
| Rate Limiting | COMPLETE | Bucket4j implemented |
| GraphQL | COMPLETE | Netflix DGS framework |

---

### Key Achievements

- **Complete Authentication System:** JWT tokens, refresh mechanism, account lockout after 5 failed attempts, password reset functionality
- **Full API Layer:** All 8 domain services with complete CRUD operations implemented (Property, Investment, User, Approval, Contract, Notification, Rating, Service Provider)
- **Modern UI Framework:** React 18 with TypeScript, Tailwind CSS, 21 application pages ready
- **Production Infrastructure:** Docker, Flyway migrations, OpenAPI documentation, rate limiting

---

### WBS Progress Overview

| Phase | Category | Status | Progress |
|-------|----------|--------|----------|
| 1.5 | Frontend Modernization | ADVANCED | 80% |
| 1.6 | Backend Modernization | ADVANCED | 75% |
| 2.5 | Property Display | IN PROGRESS | 85% |
| 2.2 | User Management | IN PROGRESS | 60% |
| 2.3 | Approval Workflow | IN PROGRESS | 55% |
| 1.3 | Database & Architecture | IN PROGRESS | 50% |
| 1.1 | Security Hardening | PARTIAL | 40% |
| 2.1 | Financial Calculations | SCAFFOLDED | 35% |
| 3.2 | System Documentation | IN PROGRESS | 40% |
| 3.1 | Monitoring Implementation | PARTIAL | 25% |
| 2.4 | CRM Integrations | NOT STARTED | 0% |

---

### Priority Items

#### High Priority

| # | Item | Status | Notes |
|---|------|--------|-------|
| 1 | Frontend-Backend Integration Testing | IN PROGRESS | Core APIs ready, needs E2E testing |
| 2 | Email Service Configuration | PENDING | Spring Mail configured, needs SMTP setup |
| 3 | Financial Calculations (WBS 2.1) | PENDING | ROI/bond repayment logic needed |

#### Medium Priority

| # | Item | Status | Notes |
|---|------|--------|-------|
| 4 | Sales Manager Role (WBS 2.3.1) | SCAFFOLDED | Role system exists, needs permissions |
| 5 | Multi-User Notifications (WBS 2.3.2) | SCAFFOLDED | Notification domain ready |
| 6 | CRM Integrations (WBS 2.4) | NOT STARTED | ActiveCampaign, Notion sync |
| 7 | Data Migration Scripts | NOT STARTED | Legacy to new system |

#### Lower Priority

| # | Item | Status | Notes |
|---|------|--------|-------|
| 8 | Monitoring Dashboard (WBS 3.1) | PARTIAL | Actuator enabled, needs dashboard |
| 9 | Documentation (WBS 3.2) | IN PROGRESS | API docs exist, need guides |
| 10 | CI/CD Pipeline | PARTIAL | Docker ready, needs GitHub Actions |

---

### Risk Assessment

| Risk | Severity | Mitigation |
|------|----------|------------|
| Data migration from legacy | MEDIUM | Plan migration scripts early |
| Integration testing gaps | LOW | E2E test framework ready (Playwright) |
| External service dependencies | LOW | Abstraction layers in place |

---

## Key Questions from Ezra (Requiring Due Diligence Review)

1. **Is the full code migration technically sound and truly necessary?**
   - Legacy stack: Vue 2 / Django
   - New stack: React 18 / Spring Boot 3.4 / Java 21

2. **Is the pricing reasonable relative to the scope of work?**

3. **Can we create a standardised brief to compare 5 development houses fairly?**
