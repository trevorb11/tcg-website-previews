# Bronze Star Complete Lawn Care and Home Solutions — Full Website Audit & Redesign Plan

**Prepared:** June 19, 2026
**Client:** Robert C. Ford, Owner & CEO
**Business:** Bronze Star Complete Lawn Care and Home Solutions
**Location:** 126 Lee Rd 2083, Phenix City, AL 36870
**Phone:** (706) 464-5224 / (706) 358-9350
**Email:** fordlogistics34@gmail.com
**Certifications:** SDVOSB, VOSB, SAM.gov Registered

---

## Part 1: Current Site Audit

### Domains Under Review

| Domain | Status | Platform | Notes |
|--------|--------|----------|-------|
| bronzestarlawncare.com | Active (primary) | React SPA (likely Vite-built) | Single-page site, all anchor-linked sections |
| bronzestarlawncare34.com | Active (secondary) | React SPA (built with Lovable.dev AI tool) | Multi-page site with routing |
| bronzestarlawnservices.com | DNS dead | N/A | Domain has lapsed or DNS is not configured |

---

### Site 1: bronzestarlawncare.com (Primary)

#### 1. Design & UX

**Strengths:**
- Clean, modern single-page layout with a clear visual hierarchy
- Professional color palette (dark/military tones with green accents)
- Well-structured hero section with strong headline, subtext, and dual CTAs ("Get a Free Quote" / "Our Services")
- Stats bar in hero (Est. 2022, 14 Skilled Professionals, SDVOSB Veteran-Owned) adds immediate credibility
- Gallery section with 7 labeled project images
- Professional typography using Inter (body) and Playfair Display (headings)

**Weaknesses:**
- Single-page architecture means all content loads at once
- No separate service detail pages
- Navigation links are all anchor links (#home, #services, etc.) — not individually indexable by search engines
- Privacy Policy and Terms of Service links point to "#" (non-functional)

**Overall Design Score: 7/10**

#### 2. Content & Copy

**Strengths:**
- Strong, clear headline: "Complete Lawn Care & Home Solutions"
- Veteran/SDVOSB messaging is prominently placed in the hero badge
- About section includes a photo of Robert Ford with title and a well-written company narrative
- Testimonials section features 5 verified Angi reviews, all 5-star, with dates and attribution
- Contact section lists service area, phone numbers, email, and certifications
- Credentials listed: Category 3 Pesticide Sprayer (AL & GA), Level 1 TN Erosion Control

**Weaknesses:**
- Services are brief cards with no detailed pages
- No pricing guidance, even approximate ranges
- No mention of service area beyond "Phenix City, AL & Surrounding Areas"
- Reviews are from 2023 — over 3 years old
- "14 Skilled Professionals" stated but not elaborated
- No FAQ section
- Gmail email address undermines professionalism

**Content Score: 6.5/10**

#### 3. SEO

**Strengths:**
- Well-formed title tag: "Bronze Star Complete Lawn Care and Home Solutions | Phenix City, AL"
- Meta description present with key terms and location
- Proper heading hierarchy (H1: 1, H2: 5, H3: 8)
- All 8 images have alt text
- Viewport meta tag and lang="en" set correctly
- Custom favicon (SVG)

**Critical Weaknesses:**
- No JSON-LD / Schema markup — missing LocalBusiness, Service, Review structured data
- No Open Graph tags — social sharing shows generic previews
- No Twitter Card tags
- No canonical tag — risk of duplicate content with multiple domains
- No Google Analytics or any analytics platform
- Single-page architecture is hostile to SEO — Google cannot index individual service pages
- Only 1 external link (to Angi reviews page)

**SEO Score: 3/10** — Fundamentally broken for search engine visibility.

#### 4. Trust & Conversion

**Strengths:**
- SDVOSB certification mentioned multiple times
- 5 verified Angi reviews with 5-star ratings, names, and dates
- Well-designed contact form with service dropdown
- "Get a Free Quote" CTA repeated throughout
- Owner photo with name and title
- Link to Angi reviews page

**Weaknesses:**
- No Google Business Profile link
- No social media links anywhere
- Reviews are from 2023
- No before/after project photos
- No license numbers displayed
- No insurance mention
- Contact form has no backend confirmation
- Gmail email address

**Trust & Conversion Score: 5/10**

#### 5. Technical

- **Platform:** Custom React SPA, built with Vite
- Single JavaScript bundle, single CSS file
- No analytics whatsoever
- No server-side rendering — Google may struggle to index React-rendered content
- Form functionality questionable — no visible form action or backend endpoint
- 1 console error detected on page load

**Technical Score: 4/10**

---

### Site 2: bronzestarlawncare34.com (Secondary)

#### 1. Design & UX

**Strengths:**
- Multi-page architecture with proper routing (Home, About, Services, Gallery, Testimonials, Certifications, Contact)
- Phone number prominently displayed in header navigation
- Footer includes physical address and business hours (Mon-Fri 7:30 AM - 7:00 PM, Sat 8:00 AM - 5:00 PM)
- Dedicated Certifications page with detailed SDVOSB, VOSB, and SAM.gov explanations
- "Why Choose Bronze Star?" section with 7 value propositions

**Weaknesses:**
- Page titles are identical across all pages
- Services page lists 11 services but all "Request a Quote" buttons link to /contact — no individual service pages
- Built with Lovable.dev (AI website builder) — twitter:site meta tag says "@Lovable"
- No sticky/floating CTA button on mobile

**Design Score: 7.5/10**

#### 2. Content & Copy

**Critical Issue:**
- **Conflicting founding date:** This site says "17+ years experience" while the primary site says "Est. 2022." These cannot both be true. Major credibility red flag.

**Strengths:**
- More detailed service descriptions than the primary site
- Robert Ford's bio is more detailed
- Certifications page explains SDVOSB, VOSB, and SAM.gov
- Additional services: Stonework, Rock Beds & Flowerbeds, Electrical/Heating/Cooling

**Content Score: 6/10**

#### 3. SEO

- Open Graph tags present (improvement over primary site)
- Twitter Card tags present (but twitter:site points to @Lovable)
- Multi-page architecture allows individual pages to be indexed
- Still no JSON-LD / Schema markup
- No canonical tags
- Identical page titles across all pages
- No Google Analytics
- OG image URL appears broken

**SEO Score: 4/10**

#### 4. Cross-Site Branding Comparison

| Element | bronzestarlawncare.com | bronzestarlawncare34.com |
|---------|----------------------|------------------------|
| Business name in header | "BRONZE STAR COMPLETE LAWN CARE" | "BRONZE STAR COMPLETE LAWN CARE" |
| Full name in body | "...and Home Solutions" | "Bronze Star Lawn Care" |
| Founded/experience | "Est. 2022" | "17+ years experience" |
| Team size | "14 Skilled Professionals" | Not mentioned |
| Services count | 8 services | 11 services |
| Reviews | 5 Angi reviews displayed | Reviews page exists (not on homepage) |
| Address | Not shown | 126 Lee Rd 2083, Phenix City, AL 36870 |
| Business hours | Not shown | Mon-Fri 7:30-7:00, Sat 8:00-5:00 |

**Branding Consistency Score: 3/10** — naming and facts conflict between sites.

---

### Domain Strategy Assessment

**Current Problems:**
1. SEO authority diluted across 3 domains instead of 1
2. Customers may find different sites with conflicting information
3. Google Business Profile can only point to one website URL
4. Paying for 3 domain registrations and potentially multiple hosting plans
5. Trust erosion — savvy customers who find both sites will notice discrepancies

---

## Part 2: Recommended Redesign Plan

### 1. Domain Consolidation Strategy

**Primary domain:** `bronzestarlawncare.com`
- Shorter, cleaner, more memorable
- No confusing "34" suffix

**Actions:**
1. Build new unified site on bronzestarlawncare.com
2. 301 redirect bronzestarlawncare34.com to bronzestarlawncare.com
3. Renew bronzestarlawnservices.com and 301 redirect it (or let it expire)
4. Canonical tags on every page pointing to bronzestarlawncare.com
5. Update all directory listings to point to the primary domain

### 2. Recommended Site Architecture

```
bronzestarlawncare.com/
|-- / (Homepage)
|-- /about (About Us + Robert Ford bio)
|-- /services (Services overview)
|   |-- /services/lawn-care
|   |-- /services/landscaping
|   |-- /services/tree-services
|   |-- /services/pressure-washing
|   |-- /services/home-remodeling
|   |-- /services/roofing
|   |-- /services/painting
|   |-- /services/land-clearing
|   |-- /services/plumbing-gas
|   |-- /services/electrical-hvac
|-- /gallery (Project Gallery with before/after photos)
|-- /reviews (Testimonials + links to Angi, Google)
|-- /certifications (SDVOSB, VOSB, SAM.gov details)
|-- /service-areas
|   |-- /service-areas/phenix-city-al
|   |-- /service-areas/columbus-ga
|   |-- /service-areas/fort-moore
|   |-- /service-areas/auburn-opelika
|-- /contact (Contact form, map, hours, phone)
|-- /blog (Future content marketing)
|-- /privacy-policy
|-- /terms-of-service
```

### 3. Design Direction & Tone

**Visual Identity:**
- **Primary color:** Deep olive green or forest green (lawn care, growth, nature)
- **Secondary color:** Bronze/gold (#CD7F32) (Bronze Star, military honor)
- **Accent:** Cream/off-white backgrounds
- **Dark neutral:** Charcoal or deep slate for text

**Typography:**
- Keep Inter for body text
- Replace Playfair Display with Barlow or Oswald for headings (military-adjacent strength)
- 16px minimum body text

**Imagery:**
- Professional photos of actual Bronze Star work (not stock)
- Before/after project comparisons
- Robert Ford in professional attire or work gear
- Drone/aerial shots of completed landscape projects if possible

**Veteran-Owned Angle:**
- Subtle but consistent — badge in header, brief mention in hero, detailed on About page
- Use language like "military discipline," "mission-driven," "service before self" naturally
- Display SDVOSB badge prominently but not as primary branding

### 4. Content Strategy

**Immediate Priorities:**
1. **Resolve the founding date discrepancy** — If Robert has 17+ years of personal experience but founded Bronze Star in 2022, say exactly that: "Founded in 2022 by Robert C. Ford, a veteran with 17 years of experience in lawn care and property services."
2. **Standardize the business name** — Pick one and use it everywhere
3. **Write detailed service pages** — 400-800 words each
4. **Get a branded email** — info@bronzestarlawncare.com
5. **Gather fresh reviews** — The 2023 Angi reviews are good but dated
6. **Add FAQ sections**

### 5. SEO Strategy

**Technical SEO:**
- JSON-LD structured data on every page (LocalBusiness, Service, Review, FAQPage, BreadcrumbList)
- Canonical tags, XML sitemap, robots.txt
- Open Graph and Twitter Card meta tags
- Server-side rendering or static site generation (critical for Google indexing)
- Google Analytics 4 + Google Tag Manager + Search Console

**Local SEO (highest priority):**
1. **Claim and optimize Google Business Profile** — single most impactful action
2. **Build NAP-consistent citations** across all directories
3. **Service area pages** for Phenix City, Columbus GA, Fort Moore, surrounding areas
4. **Google Reviews campaign** — target 50+ reviews within 6 months

**Keyword Targets:**
- "lawn care Phenix City AL"
- "landscaping Columbus GA"
- "lawn service near Fort Moore"
- "veteran owned lawn care Alabama"
- "SDVOSB lawn care contractor"
- "[service] + [city]" combinations for all services and areas

### 6. Conversion Optimization

- Click-to-call buttons on every page
- Sticky mobile CTA (floating "Call Now" or "Get Quote")
- Short contact forms: Name + Phone + Service (email optional)
- Before/after gallery — most powerful conversion tool for service businesses
- Trust badge bar: SDVOSB seal, SAM.gov logo, Angi badge, Google rating, insurance/license badges
- Urgency messaging: "Same-week service available"

### 7. Social Media Presence Gaps

**No social media presence currently.** Recommended platforms (priority order):
1. **Facebook Business Page** — essential for local businesses in this market
2. **Instagram** — visual platform perfect for lawn care/landscaping
3. **Google Business Profile** posts — weekly updates
4. **Nextdoor** — hyperlocal, homeowners actively seek service providers here
5. **LinkedIn** — important for government contracting leads (SDVOSB)
6. **YouTube** (future) — project walkthroughs, how-to content

### 8. Technical Stack Recommendation

**Option A (Recommended): Next.js or Astro with static export**
- Server-side rendered or statically generated pages
- Excellent SEO, fast page loads
- Deploy to Vercel or Netlify

**Option B: WordPress with quality theme**
- Easier for client to self-manage
- Astra or GeneratePress theme
- SiteGround or Cloudways hosting

### 9. Priority Order

**Phase 1 — Immediate (Week 1-2):**
1. Claim Google Business Profile
2. Set up branded email
3. Resolve founding date discrepancy
4. Standardize business name across platforms
5. Install analytics on current sites temporarily

**Phase 2 — Short-term (Week 3-6): New Site Build**
6. Design and build unified website on bronzestarlawncare.com
7. Write all service page content with local SEO keywords
8. Implement full JSON-LD structured data
9. Create service area pages

**Phase 3 — Launch (Week 7-8):**
10. Launch new site
11. Set up 301 redirects from secondary domains
12. Update all directory listings

**Phase 4 — Growth (Month 3-6):**
13. Create Facebook and Instagram pages
14. Google Reviews collection campaign
15. Build local citations across 20+ directories
16. Start blog content (2 posts/month minimum)
17. Consider Google Local Service Ads

---

## Summary of Critical Findings

| Issue | Severity |
|-------|----------|
| No Google Business Profile linked/visible | Critical |
| No analytics on either site | Critical |
| No JSON-LD structured data | Critical |
| Conflicting founding date (2022 vs. 17 years) | Critical |
| 3-domain fragmentation with no redirects | High |
| SPA architecture on primary site (not indexable) | High |
| No social media presence | High |
| Gmail email address | Medium |
| Inconsistent business naming | Medium |
| Reviews are 3+ years old | Medium |

**Bottom line:** Bronze Star has a strong foundation — real reviews, real certifications, real expertise, and a compelling veteran-owned story. But the current web presence is fragmented, technically underbuilt, and nearly invisible to search engines. A unified, SEO-optimized, professionally branded website consolidated on a single domain would dramatically improve discoverability, credibility, and lead generation.
