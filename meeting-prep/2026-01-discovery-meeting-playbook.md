# InvestRand Discovery Meeting - Playbook (Revised)

**Meeting with:** Ezra Rasethe (CEO, InvestRand)
**Objective:** Win the account by understanding operations and demonstrating we can help
**Approach:** Operational discovery - understand how the business actually runs

---

## The Business Reality (What We Know)

| Fact | Source |
|------|--------|
| **Model:** Property marketplace/brokerage | Press coverage |
| **Revenue:** 5% commission (min R30k) per transaction | Disrupt Africa |
| **Users:** 1,000+ since March 2023 | Disrupt Africa |
| **Repeat rate:** 60% | Disrupt Africa |
| **Revenue:** ~R2M Year 2 | Disrupt Africa |
| **Status:** Bootstrapped, profitable since day 1 | Disrupt Africa |
| **Team:** Ezra (CEO) + Francois (CTO/Advisor) | Press |

**The Mismatch:**
- Develutions quoting R660k/year (33% of revenue) for enterprise architecture
- InvestRand needs operational efficiency, not enterprise scale
- 11 bugs in Ezra's original list are mostly workflow/integration issues

---

## Meeting Structure (60 mins)

| Phase | Duration | Focus |
|-------|----------|-------|
| 1. Rapport | 5 mins | Acknowledge Chand, set collaborative tone |
| 2. Business Model | 15 mins | How does the marketplace actually work? |
| 3. Operations & Pain | 20 mins | Where does the system create friction? |
| 4. Technology Alignment | 15 mins | What should tech enable for growth? |
| 5. Next Steps | 5 mins | Propose focused discovery |

---

## Phase 1: Opening Frame

**Tone:** Helpful, curious, practical

**Opening:**
> "Ezra, thanks for making time. Chand speaks highly of what you're building. Before we talk technology, I'd love to understand how InvestRand actually works day-to-day - the operations, the workflows, where things work well and where they don't. That'll help us figure out where we can actually add value."

**Why:** Positions us as people who want to help the business, not sell technology.

---

## Phase 2: Business Model Questions (OSS/BSS Foundation)

These questions map how the business actually operates - the Operational Support Systems (how work gets done) and Business Support Systems (how you track, bill, report).

### Understanding the Marketplace

**Q1. The Transaction Flow**
"Walk me through what happens when an investor finds a property they want to buy - from first enquiry to transaction complete. Where does the platform help, and where do things go manual?"

**Listen for:**
- Where does automation stop?
- Manual handoffs (email, phone, WhatsApp?)
- CRM integration pain (ActiveCampaign/Notion)
- Where deals fall through the cracks

---

**Q2. The Listing Flow**
"When a seller or agent wants to list a property, what's that process? Who does what, and how does it get approved?"

**Listen for:**
- Approval workflow pain (mentioned in bug list)
- Role permissions issues (Sales Manager approval)
- Quality control process
- Time from listing to live

---

**Q3. The Three-Sided Marketplace**
"You've got investors, sellers, and service providers. How do you balance serving all three? Which one is hardest to manage?"

**Listen for:**
- Where the operational complexity lives
- Service provider integration
- Which side drives growth

---

### Understanding the Operations

**Q4. Lead Management**
"When an enquiry comes in, what happens to that lead? Where does it go, who follows up, how do you track it?"

**Listen for:**
- ActiveCampaign integration (we know it's broken)
- Notion sync issues
- Manual work required
- Leads falling through cracks

---

**Q5. Agent/Seller Management**
"How do you manage your relationships with listing agents? Do they have their own login, can they update their listings?"

**Listen for:**
- Agent portal needs
- Self-service gaps
- Permission issues (bug #5, #11)
- Communication friction

---

**Q6. Commission & Billing**
"When a transaction closes, how does the commission get calculated and collected? Is that all manual, or is there system support?"

**Listen for:**
- Payment infrastructure (or lack of)
- Manual invoicing pain
- Cash flow visibility
- Revenue leakage

---

## Phase 3: Operations & Pain Questions

### The Daily Friction

**Q7. The 3am Wake-Up Call**
"What's the thing that frustrates you most about the platform right now? If you could fix one thing tomorrow, what would make the biggest difference to your day?"

**Listen for:**
- His top priority (not what Develutions prioritised)
- Operational vs technical framing
- Urgency level

---

**Q8. Team Friction**
"Your team - what do they complain about? What slows them down?"

**Listen for:**
- Internal user pain (Kim, the CC'd colleague)
- Admin overhead
- Workarounds they've created

---

**Q9. Investor Friction**
"What feedback do investors give you? What do they wish the platform did better?"

**Listen for:**
- User-facing issues (15s load time?)
- Mobile experience
- Information they can't find
- Trust/credibility signals

---

### The Specific Pain Points (From His Bug List - Don't Reveal Source)

**Q10. User Management**
"How do you handle adding and removing users? What about password resets - is that something your team can do, or does it need tech support?"

**Listen for:**
- Validates bugs #1, #2, #9
- Admin capability gaps
- Support burden

---

**Q11. Notifications & Approvals**
"When a listing needs approval, how does that notification work? Does everyone who needs to know actually find out?"

**Listen for:**
- Validates bugs #3, #4
- Workflow gaps
- Communication breakdowns

---

**Q12. Financial Accuracy**
"The ROI calculations on the platform - how confident are you in those numbers? Do investors trust them?"

**Listen for:**
- Validates bugs #7, #8
- Credibility concern
- Core value prop issue

---

## Phase 4: Technology Alignment (What Should Tech Enable?)

### Growth Questions

**Q13. Scaling the Business**
"If the platform was working perfectly, what would that unlock for InvestRand? What would you do that you can't do now?"

**Listen for:**
- Growth constraints (tech vs sales vs market)
- Automation opportunities
- What matters for the next stage

---

**Q14. Mobile & Access**
"How do your users typically access the platform? Desktop, mobile, both?"

**Listen for:**
- Mobile gap (not discussed by Develutions)
- User context (on-the-go investors)
- Quick wins available

---

**Q15. Integration Needs**
"What other systems does InvestRand need to talk to? CRM, property feeds, anything else?"

**Listen for:**
- Integration landscape
- ActiveCampaign/Notion priority
- Future integration needs

---

### Technology Experience

**Q16. Current Development Situation**
"You've been working with a development team - how's that been going? What's working, what's not?"

**Listen for:**
- Develutions frustrations (without leading)
- Trust level
- What he wishes was different

---

**Q17. Technology Ownership**
"Long term, do you want to build internal tech capability, or always work with external partners? What makes sense for InvestRand?"

**Listen for:**
- Insource vs outsource preference
- Budget constraints implied
- Knowledge transfer importance

---

## Phase 5: Closing & Next Steps

### Summarise What You Heard

> "Let me make sure I've got this right: InvestRand is a marketplace connecting investors with properties - you take 5% on successful transactions. The platform handles listings, approvals, enquiries, and financial calculations. The main pain right now is [X, Y, Z he mentioned]. And you want the technology to [his words]. Did I miss anything?"

### Position Our Approach

> "Here's how we'd typically help: We'd do a focused discovery - maybe 2-3 days - where we understand the current system, map out what's actually causing friction, and give you a prioritised list of what to fix and in what order. No big upfront commitment, just clarity on what needs to happen. Would that be useful?"

### Propose Concrete Next Step

> "Would it help if we put together a short assessment - focused on the operational pain points you've mentioned? We can have something back to you in a week."

---

## OSS/BSS Framework for InvestRand

### Operational Support Systems (How Work Gets Done)

| System | Current State | Should Enable |
|--------|--------------|---------------|
| **Listing Management** | Manual approvals, status updates broken | Self-service for agents, automated workflows |
| **Lead Management** | ActiveCampaign sync broken | Enquiry → CRM → follow-up automated |
| **User Management** | Can't add/remove users, password reset broken | Self-service admin |
| **Notification System** | Multi-user notifications not working | Right people notified at right time |
| **Property Display** | Slow loading, missing identifiers | Fast, complete, trustworthy |

### Business Support Systems (How You Track & Bill)

| System | Current State | Should Enable |
|--------|--------------|---------------|
| **Financial Calculations** | ROI formula wrong, bond calc inconsistent | Accurate, trusted numbers |
| **Commission Tracking** | Manual? Unknown | Track pipeline, forecast revenue |
| **Reporting** | Unknown | Know what's working, what's not |
| **Billing/Invoicing** | Manual? | Streamlined collection |

---

## What We're Really Listening For

| Signal | What It Means |
|--------|---------------|
| "Leads fall through the cracks" | CRM integration priority |
| "I have to do it manually" | Automation opportunity |
| "Investors complain about..." | User-facing priority |
| "We can't add users ourselves" | Admin capability gap |
| "The numbers don't match" | Credibility/trust issue |
| "It's too slow" | Performance priority |
| "We want to do X but can't" | Growth constraint to solve |

---

## Landmines to Avoid

| Don't Say | Say Instead |
|-----------|-------------|
| "We saw your Lighthouse score is 36%" | "How do users find the platform speed?" |
| "The ActiveCampaign integration is broken" | "Walk me through what happens when an enquiry comes in" |
| "Develutions is recommending a full rewrite" | "What approach has been discussed for fixing these issues?" |
| "Your security headers are missing" | "Have you had any security concerns?" |
| "You're spending 33% of revenue on tech" | "How do you think about technology investment relative to growth?" |

---

## Power Phrases

These show we think about business operations, not just code:

- "Walk me through how that actually works day-to-day..."
- "Where does that process break down?"
- "What would that unlock for the business?"
- "Who else feels that pain?"
- "What's the workaround you use today?"
- "If that was fixed, what would change?"

---

## Capability Proof Points (If Asked)

Only deploy if he asks "What have you built?" or "Can you actually help?"

| Project | Relevance to InvestRand |
|---------|-------------------------|
| **AgentF ERP** | 173 tables, complex business logic, production deployment - we build real systems |
| **DCX Cloud** | 200+ organisations, multi-tenant billing - we understand marketplace dynamics |
| **OneFootball** | 100M users, configuration at scale - we can make things fast and reliable |

**Key message:** "We build systems that help businesses run better. We're not attached to any particular technology - we're attached to solving operational problems."

---

## Qualification (Internal Use)

### Green Lights (Pursue)
- ✅ Clear operational pain (not just "we want new tech")
- ✅ Budget awareness (knows R660k/year is a lot for current size)
- ✅ Pragmatic approach (fix what's broken vs rebuild everything)
- ✅ Decision maker (Ezra can decide, small company)
- ✅ Reasonable timeline

### Red Lights (Pause)
- ⚠️ Already committed to Develutions (12-month contract signed?)
- ⚠️ Wants enterprise architecture for SMB scale
- ⚠️ Budget not realistic for meaningful work
- ⚠️ No urgency (just exploring)

---

## Post-Meeting Actions

1. **Same day:** Thank-you message with 3 key things we heard
2. **Within 48 hours:** Short proposal for focused discovery
3. **Discovery scope:**
   - Current system review (see what Develutions built)
   - Operational workflow mapping
   - Prioritised fix list
   - Right-sized recommendations
   - Fixed price, 3-5 days

---

## One-Page Cheat Sheet (Print This)

**Open with:** "I'd love to understand how InvestRand actually works day-to-day"

**Must-ask questions:**
1. Walk me through a transaction from enquiry to close
2. What frustrates you most about the platform right now?
3. When an enquiry comes in, where does that lead go?
4. How confident are you in the ROI calculations?
5. If the platform worked perfectly, what would that unlock?

**Listen for:**
- Manual workarounds
- Integration breakdowns
- User complaints
- Growth constraints
- What he wishes was different about current dev team

**Close with:** Offer a focused discovery (3-5 days, fixed price, no lock-in)

**Avoid:** VC talk (cashflow, Series A), revealing our scans, badmouthing Develutions
