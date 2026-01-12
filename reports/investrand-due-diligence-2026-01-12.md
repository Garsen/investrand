# Investrand Technical Due Diligence Report

**Date:** 12 January 2026
**Target:** https://platform.investrand.co.za/
**Type:** External reconnaissance (no internal access)
**Prepared for:** Presales consulting engagement

---

## Executive Summary

Investrand is a South African real estate investment platform helping users build wealth through property investments. The platform shows signs of being an early-stage product with significant technical debt and performance issues that present clear opportunities for improvement.

### Top 5 Findings

| # | Finding | Severity | Category |
|---|---------|----------|----------|
| 1 | **Critical performance issues** - 15s load time, 36% Lighthouse score | Critical | Performance |
| 2 | **Missing security headers** - No CSP, X-Frame-Options, or CORS config | High | Security |
| 3 | **Outdated frontend framework** - Vue 2.6 (EOL Dec 2023) | Medium | Tech Debt |
| 4 | **No DMARC email security** - Spoofing vulnerability | Medium | Security |
| 5 | **Accessibility gaps** - 70% score, 13 contrast issues | Medium | UX |

### Recommended Next Steps

1. **Immediate:** Security headers implementation (1-2 days)
2. **Quick win:** Performance optimisation - unused JS removal could save 3+ seconds
3. **Medium-term:** Vue 2 → Vue 3 migration planning
4. **Discovery:** Schedule technical architecture walkthrough with their team

---

## 1. Technology Stack

### Frontend
| Component | Version/Details | Status |
|-----------|-----------------|--------|
| Framework | Vue.js 2.6.14 | ⚠️ EOL Dec 2023 |
| State Management | Vuex 3.6.2 | Current for Vue 2 |
| Router | Vue Router 3.5.2 | Current for Vue 2 |
| UI Library | BootstrapVue | Active |
| Build Tool | Webpack | Inferred from chunk naming |
| Icons | Font Awesome 5.6.3 | Slightly outdated |
| Fonts | Open Sans (Google Fonts) | OK |

### Infrastructure
| Component | Provider | Notes |
|-----------|----------|-------|
| Hosting | Netlify | Good choice - CDN, CI/CD built-in |
| CDN/Proxy | Cloudflare | Enterprise-grade, good security |
| SSL Certificate | Google Trust Services | Valid, auto-renewing via Cloudflare |
| DNS | Cloudflare | 172.67.157.247, 104.21.58.78 |
| Marketing Site | Wix (separate) | www.investrand.co.za |

### Third-Party Services
| Service | Purpose | Provider |
|---------|---------|----------|
| Analytics | User behaviour tracking | Microsoft Clarity |
| Error Monitoring | Application errors | Sentry |
| Support | Customer tickets | Freshdesk |
| Maps | Location services | Google Maps API |
| Email | Business email | Microsoft 365 |

### Backend (Inferred)
- API endpoint pattern: `/api/v1/*`
- Environment hints in code: `dev-api-*`, `uat-api-*` (proper staging environment exists)
- Authentication: Custom implementation (api.user.logout() referenced)
- Cannot determine backend language/framework without access

---

## 2. Security Assessment

### 2.1 Transport Security ✅ Acceptable

| Check | Status | Details |
|-------|--------|---------|
| HTTPS | ✅ Pass | Enforced via HSTS |
| HSTS | ✅ Pass | max-age=31536000 (1 year) |
| SSL Certificate | ✅ Pass | Valid ECDSA P-256, expires April 2026 |
| HTTP/2 | ✅ Pass | Enabled |
| TLS Version | ✅ Pass | TLS 1.3 supported |

### 2.2 HTTP Security Headers ❌ Critical Gaps

| Header | Status | Risk |
|--------|--------|------|
| Content-Security-Policy | ❌ Missing | XSS attacks, code injection |
| X-Frame-Options | ❌ Missing | Clickjacking attacks |
| X-Content-Type-Options | ❌ Missing | MIME sniffing attacks |
| Referrer-Policy | ❌ Missing | Privacy leakage |
| Permissions-Policy | ❌ Missing | Feature abuse |
| X-XSS-Protection | ❌ Missing | Legacy XSS protection |

**Recommendation:** Implement all headers via Netlify `_headers` file or `netlify.toml`. This is a quick win (< 1 hour implementation).

### 2.3 Information Disclosure ⚠️ Moderate Risk

| Item | Status | Details |
|------|--------|---------|
| Server Version | ✅ Hidden | Cloudflare obscures backend |
| .git exposed | ✅ Not exposed | 404 response |
| .env exposed | ✅ Not exposed | 404 response |
| API docs exposed | ✅ Not exposed | No swagger/OpenAPI found |
| **Google Maps API Key** | ⚠️ Exposed | Key visible in HTML source (redacted from this report) |
| **Sentry DSN** | ⚠️ Exposed | Visible in source (low risk) |
| **Environment hints** | ⚠️ In source | dev-api/uat-api references visible |

**Google API Key Risk:** Key is exposed and appears unrestricted. Should be restricted to:
- Specific APIs (Maps JavaScript API, Places API only)
- Specific referrers (*.investrand.co.za)

### 2.4 Email Security ❌ Gap

| Record | Status | Details |
|--------|--------|---------|
| SPF | ✅ Present | `v=spf1 include:secureserver.net include:spf.protection.outlook.com ~all` |
| DKIM | ⚠️ Unknown | Requires DNS access to verify |
| **DMARC** | ❌ Missing | No `_dmarc.investrand.co.za` TXT record |

**Risk:** Without DMARC, attackers can spoof emails from @investrand.co.za. Critical for a financial services platform.

**Recommendation:** Implement DMARC policy:
```
_dmarc.investrand.co.za TXT "v=DMARC1; p=quarantine; rua=mailto:dmarc@investrand.co.za"
```

### 2.5 OWASP Alignment Summary

| OWASP Top 10 Category | External Assessment |
|-----------------------|---------------------|
| A01 Broken Access Control | Cannot assess externally |
| A02 Cryptographic Failures | ✅ TLS properly configured |
| A03 Injection | Cannot assess externally |
| A04 Insecure Design | ⚠️ Missing security headers suggest gaps |
| A05 Security Misconfiguration | ❌ Missing headers, exposed API key |
| A06 Vulnerable Components | ⚠️ Vue 2 EOL |
| A07 Auth Failures | Cannot assess externally |
| A08 Data Integrity Failures | Cannot assess externally |
| A09 Logging/Monitoring | ✅ Sentry implemented |
| A10 SSRF | Cannot assess externally |

---

## 3. Performance Analysis

### 3.1 Lighthouse Scores

| Category | Score | Rating |
|----------|-------|--------|
| **Performance** | 36% | 🔴 Critical |
| Accessibility | 70% | 🟠 Needs Work |
| Best Practices | 77% | 🟡 Acceptable |
| SEO | 83% | 🟢 OK |

### 3.2 Core Web Vitals

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| **First Contentful Paint** | 8.1s | < 1.8s | 🔴 4.5x over |
| **Largest Contentful Paint** | 15.1s | < 2.5s | 🔴 6x over |
| **Time to Interactive** | 15.1s | < 3.8s | 🔴 4x over |
| **Speed Index** | 9.5s | < 3.4s | 🔴 2.8x over |
| Total Blocking Time | 860ms | < 200ms | 🔴 4x over |
| Cumulative Layout Shift | 0.035 | < 0.1 | 🟢 Pass |

### 3.3 Performance Opportunities

| Opportunity | Potential Savings | Priority |
|-------------|-------------------|----------|
| **Reduce unused JavaScript** | 1,163 KiB / 3.1s | 🔴 Critical |
| Reduce unused CSS | 81 KiB / 280ms | 🟠 High |
| Render-blocking resources | TBD | 🟠 High |
| Image optimisation | TBD | 🟡 Medium |

**Root Cause Analysis:**
- SPA loading entire application on initial page load
- No code splitting by route (all chunks prefetched)
- Large vendor bundle (Vue + BootstrapVue + dependencies)
- Third-party scripts (Google Maps, Clarity, Sentry) add overhead

**Quick Wins:**
1. Implement route-based code splitting
2. Lazy-load Google Maps only on pages that need it
3. Tree-shake unused BootstrapVue components
4. Consider moving to Vue 3 + Vite for better tree-shaking

---

## 4. Accessibility Assessment

### Failed Audits

| Issue | Count | WCAG | Priority |
|-------|-------|------|----------|
| Insufficient colour contrast | 13 elements | 2.1 AA | High |
| Missing image alt text | 2 images | 2.1 A | High |
| Missing lang attribute on HTML | 1 | 2.1 A | High |
| user-scalable=no in viewport | 1 | 2.1 AA | High |
| Missing main landmark | 1 | 2.1 A | Medium |
| Links without discernible name | 1 | 2.1 A | Medium |

### Specific Issues

1. **Colour Contrast:** 13 elements fail WCAG 2.1 AA (4.5:1 ratio for normal text)
2. **Zoom Disabled:** `user-scalable=0, maximum-scale=1` prevents users from zooming
3. **No Language Declaration:** Screen readers cannot determine language

**Quick Fix:** Update viewport meta tag:
```html
<!-- Current (bad) -->
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=0">

<!-- Fixed -->
<meta name="viewport" content="width=device-width,initial-scale=1">
```

---

## 5. Product & UX Observations

### Platform Overview
- **Business:** Real estate investment platform for South African market
- **Value Prop:** "Build wealth through property investments"
- **Target Market:** Individual investors seeking passive income from property

### Observed Features (from source analysis)
- User authentication (login/logout)
- Dashboard
- Forms (likely property listings or investments)
- Tables (likely portfolio/transaction views)
- Google Maps integration (property locations)
- Support ticket integration (Freshdesk)

### UX Concerns
1. **15-second load time** - Users likely bounce before seeing content
2. **No meta description** - Poor search appearance
3. **Zoom disabled** - Accessibility barrier
4. **Mixed hosting** - Marketing (Wix) vs Platform (Netlify) may cause brand inconsistency

---

## 6. Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| **User abandonment due to slow load times** | High | High | Performance optimisation |
| **Security breach via missing headers** | Medium | High | Implement CSP, X-Frame-Options |
| **Email spoofing attacks** | Medium | High | Implement DMARC |
| **Vue 2 EOL - no security patches** | Medium | Medium | Plan Vue 3 migration |
| **Google API key abuse** | Low | Medium | Restrict API key |
| **Accessibility lawsuit** | Low | Medium | Fix WCAG violations |
| **Technical debt accumulation** | High | Medium | Establish coding standards |

---

## 7. Opportunities

### Quick Wins (1-3 days)
| Item | Effort | Impact | Value |
|------|--------|--------|-------|
| Add security headers | 1 hour | High | Immediate security improvement |
| Fix viewport meta tag | 10 mins | Medium | Accessibility compliance |
| Add HTML lang attribute | 10 mins | Medium | Accessibility compliance |
| Restrict Google API key | 30 mins | Medium | Security hardening |
| Add DMARC record | 1 hour | High | Email security |

### Medium-Term Improvements (1-4 weeks)
| Item | Effort | Impact |
|------|--------|--------|
| Performance optimisation (code splitting, lazy loading) | 1-2 weeks | Critical |
| Accessibility remediation (contrast, alt text) | 1 week | High |
| SEO meta tags and sitemap | 2-3 days | Medium |

### Strategic Initiatives (1-3 months)
| Item | Effort | Impact |
|------|--------|--------|
| Vue 2 → Vue 3 migration | 4-8 weeks | High |
| Design system/component library | 2-4 weeks | Medium |
| Backend architecture review (requires access) | TBD | TBD |

---

## 8. Discovery Questions for Their Team

### Technical Architecture
1. What backend technology stack are you using?
2. Where is the backend hosted? (AWS, Azure, GCP?)
3. What database(s) are in use?
4. Do you have CI/CD pipelines? What does deployment look like?
5. How do you handle authentication? Custom or third-party?

### Development Practices
6. What does your development team look like? (size, skills, structure)
7. Do you have automated testing? What's the coverage?
8. How do you manage technical debt?
9. What's your current sprint/release cadence?

### Business & Product
10. What are your key product metrics? (MAU, conversion, etc.)
11. What's on the product roadmap for the next 6 months?
12. What are the biggest pain points with the current platform?
13. Have you experienced any security incidents?

### Infrastructure & Operations
14. What's your monitoring and alerting setup?
15. How do you handle backups and disaster recovery?
16. What's your current hosting cost structure?
17. Do you have staging/UAT environments? (We see hints of this)

---

## 9. Appendices

### A. Raw Scan Data

All scan outputs are available in `/scans/`:
- `headers-main.txt` - HTTP response headers
- `lighthouse-report.json` - Full Lighthouse audit

### B. Tools Used
- curl (HTTP analysis)
- dig/nslookup (DNS analysis)
- openssl (SSL analysis)
- Lighthouse 12.x (Performance/Accessibility)
- Manual source code review

### C. Limitations

This assessment was conducted externally without access to:
- Source code repositories
- Backend systems or databases
- Internal documentation
- Team members for interviews

A complete technical due diligence would require internal access to assess:
- Code quality and test coverage
- Database schema and query performance
- API security (authentication, authorisation, input validation)
- Infrastructure configuration
- Deployment processes
- Security practices (secrets management, logging, etc.)

---

## 10. Summary

Investrand has a functional real estate investment platform with a modern frontend hosting stack (Netlify + Cloudflare). However, significant issues exist:

**Critical:**
- Performance is severely degraded (15s load time)
- Security headers are missing

**High Priority:**
- Vue 2 is end-of-life (no security patches)
- Email security (DMARC) is missing
- Accessibility issues need attention

**Positive Signs:**
- Error monitoring (Sentry) is in place
- HTTPS/HSTS properly configured
- Cloudflare provides DDoS protection
- Proper staging environments exist (dev/uat)

This represents a clear opportunity to add value. The platform needs both immediate remediation work and longer-term modernisation. The fact that the current team isn't addressing these issues suggests capacity or capability gaps that your engagement could fill.

---

*Report generated: 12 January 2026*
