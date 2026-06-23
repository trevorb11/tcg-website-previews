# J&M All-Pro Roofing & Construction — Website Audit & Redesign Plan

**Site:** https://allprorooftx.com/
**Business:** J&M All-Pro Roofing & Construction LLC DBA "Roof Repair Services"
**Owner:** Johnny Sanchez (former Marine, 100% disabled veteran)
**Location:** 126 Angel Hollow Ln, Rosenberg, TX 77469 (Fort Bend County)
**Phone:** (760) 978-3678
**Email:** johnny@allprorooftx.com
**Audit Date:** June 19, 2026

---

## PART 1: CURRENT SITE AUDIT

---

### 1. Design & UX

**Layout & Visual Quality**
- Homepage is a single long-scroll landing page with no traditional navigation menu. No `<nav>` element in the DOM. Only navigation is a logo linking to `/` and a "Free Estimate" button linking to `/contact#form`. Interior pages have breadcrumbs and footer quick links, but no persistent site-wide navigation bar.
- Strong visual hierarchy: hero with bold H1 ("Roof Leaking? Call Johnny. He Answers -- Guaranteed."), Google Guaranteed trust bar, cost-plus pricing breakdown, veteran/discounts section, reviews section, final CTA.
- Dark navy/blue color palette (#1e3a5f) with white text, green and gold accents. Professional for a roofing company.

**Imagery**
- Real crew photos (`team-1.jpeg` through `team-4.jpeg`) labeled "Real Crew. Real Roofs." -- strong authenticity signal.
- **Cartoon mascot image** used as a logo in the Google Guaranteed section -- undermines professionalism for a GAF Master Elite contractor.
- **Cartoon marine illustration** in the veteran section instead of an actual photo of Johnny Sanchez -- missed opportunity for authentic branding.
- Only 7 visible images on homepage -- fast loading but thin visually.

**Mobile Responsiveness**
- Viewport meta tag properly set.
- Built with Vite (module-based JS). No `<nav>` means no hamburger menu -- users can only find interior pages through footer links or breadcrumbs.

**Load Speed**
- DOM interactive in ~539ms, DOM complete in ~772ms -- extremely fast.
- Transfer size only 1,494 bytes for HTML. JS and CSS bundles are hashed and cache-friendly.
- Lazy loading implemented. No Google Analytics or third-party tracking scripts (performance benefit but major analytics gap).

---

### 2. Content & Copy

**Tone & Messaging**
- Aggressive, direct, anti-establishment: "No inflated margins funding $120K lifted trucks or fat commissions." Powerful differentiator.
- "Pure Cost-Plus Pricing" with itemized example ($6,380.29 materials + $3,500 labor + $250 dump + $250 crew lunch) is unique in the industry and builds enormous trust.
- "Se habla espanol" mentioned -- good for Houston market.
- "Low-income & budget-friendly -- everyone deserves a quality roof" is a strong emotional hook.

**CRITICAL: "Carlos" vs. "Johnny" Naming Inconsistency**
The single most damaging issue on the site:
- **Meta description** (what Google shows): "All-Pro Roofing by Carlos offers free estimates"
- **OG description** (what Facebook/LinkedIn show when shared): same "by Carlos" text
- **Twitter description**: same "by Carlos" text
- **FAQ schema markup** (4 instances): "All-Pro Roofing by Carlos specializes in...", "Call Carlos at (760) 978-3678"

Every Google result, social share, and rich snippet says "Carlos" while the actual page says "Call Johnny." Immediate confusion and trust erosion.

**Phone Number Inconsistency**
- All visible content uses: `+1 760-978-3678`
- JSON-LD schema telephone field uses: `+1 713-489-4265`
- The 760 area code (California) may raise suspicion for Texas customers.

**Review Count Inconsistencies**
Wildly different claims across the site:
- Homepage text: "1,500+ Five-Star Reviews"
- Contact page: "450+ Verified Google Reviews" and "10,000+ Clients Serviced"
- JSON-LD schema: 127 reviews with 4.9 rating
- Multiple pages: "1500+ Reviews"
- "25+ Years Experience" claimed but not substantiated

If Google's actual count is 127, claiming 1,500+ is deceptive and could trigger FTC scrutiny or Google penalties.

**About Page**
Generic and impersonal. Does not mention Johnny by name, does not tell his Marine story, no real photo. Reads like template copy. Completely wastes the most compelling brand asset.

**Blog**
Four posts from November-December 2025. Thin content (400-500 words each). No posts since -- blog appears abandoned.

**Testimonials**
Same five testimonials (Michael S., Sarah T., David R., Jennifer M., Robert K.) appear on every page. Generic first-name-last-initial format, relative timestamps ("2 months ago"), suspiciously polished language. Appear fabricated or placeholder.

---

### 3. SEO

**Title Tags**
- Homepage: "All-Pro Roofing & Repairs Rosenberg | Call (760) 978-3678 | Roof Repair Services" -- good.
- Interior pages have unique, keyword-rich titles.

**Meta Descriptions**
- Homepage references "Carlos" -- critically broken.
- Many interior pages share the same generic description -- not page-specific.

**Heading Structure**
- Clean hierarchy: 1 H1, 5 H2s, 4 H3s on homepage. No misuse detected.

**Schema/JSON-LD**
- Three schema blocks: LocalBusiness/RoofingContractor, WebSite, FAQPage.
- LocalBusiness schema is comprehensive (address, geo, hours, services, aggregate rating).
- Schema telephone uses wrong number (+17134894265).
- FAQPage references "Carlos" in all four answers -- poisoning rich snippets.
- SearchAction points to `/search?q=` which likely doesn't exist.

**Canonical Tags** -- Present and correct on homepage.

**Sitemap** -- 99 URLs at `/sitemap.xml`. All dates "2026-02-02" -- not dynamically updated.

**Robots.txt** -- Properly configured. 1-second crawl delay.

**Image Alt Text** -- All 7 images have alt text but it's generic and repetitive ("Roof Repair Services crew at work" on four images).

**SSR/SPA Issue** -- Initial HTML contains correct SSR content (good), but template artifacts from a different business ("Bronze Star Lawn Care") were detected in the HTML shell -- a Lovable.dev template that was not cleaned up.

**404 Issues** -- `/about-us/`, `/products-services-overview/`, `/roofing-sugar-land/` all return 404. Sitemap may contain broken URLs.

---

### 4. Trust & Conversion

**Reviews**
- Same 5 recycled testimonials on every page -- easily spotted as fake/placeholder.
- No embedded Google Reviews widget, no link to actual review profile (except one "Leave a review" link on contact page).

**Certifications**
- GAF Master Elite badge displayed in header -- good placement.
- "Top 2% of roofers nationwide" messaging on interior pages.
- GAF warranty options detailed on warranties page.
- BBB A+ mentioned in text but no badge or link provided.
- No Owens Corning certification displayed.

**Contact Page -- CRITICAL FAILURE**
- The contact page has **ZERO form elements** -- no form, no inputs, no textarea, nothing.
- The "Free Estimate" CTA links to `/contact#form` -- an anchor that does not exist.
- Users clicking "Free Estimate" expecting a form get nothing but a phone number.
- Email address `johnny@allprorooftx.com` does not appear anywhere on the website.

**Social Media Links**
- Footer has three social icon links that all point to `"#"` -- completely broken placeholders.
- Facebook URL exists in schema but is not linked in the UI.

---

### 5. Technical

**Framework**
- Vite + React SPA with SSR. Built with Lovable.dev (detected via template artifacts and Lovable analytics scripts).
- `~flock.js` (Lovable analytics), `__l5e/events.js` (event tracking), `__l5e/rrweb-record.js` (session recording).
- **No Google Analytics, Facebook Pixel, or Google Tag Manager.**
- **No CRM integration** (ServiceTitan, Jobber, HubSpot, etc.).
- **No live chat.**

**Accessibility Issues**
- No `<nav>` element -- screen readers cannot identify navigation.
- Only 2 `aria-label` attributes on entire homepage.
- No skip-to-content link.
- Decorative icons lack `role="presentation"` or `aria-hidden="true"`.

---

### 6. Branding

**Brand Identity Crisis**
Multiple names in play:
1. Legal: "J&M All-Pro Roofing & Construction LLC"
2. DBA: "Roof Repair Services"
3. Domain: "allprorooftx.com" (suggests "All-Pro Roofing TX")
4. Homepage header: "Roof Repair Services"
5. Meta tags: "All-Pro Roofing by Carlos"
6. Page titles: "All-Pro Roofing & Repairs Rosenberg"

"Roof Repair Services" is extremely generic -- impossible to rank for and zero brand memorability. "All-Pro Roofing" is stronger and matches the domain.

**Logo & Mascot**
- No professional logo -- just text "Roof Repair Services" in header.
- Cartoon mascot and cartoon marine undermine professional perception.

---

## PART 2: RECOMMENDED REDESIGN PLAN

---

### Recommended Site Architecture

```
Homepage (/)
+-- Services
|   +-- Roof Replacement (/roof-replacement)
|   +-- Roof Repair (/roof-repair) [NEW]
|   +-- Storm Damage Repair (/storm-damage)
|   +-- Insurance Claims (/insurance-claims)
|   +-- Tile Roof Repair (/tile-roof-repair)
+-- About Johnny (/about) [REWRITE]
+-- Our Process (/our-process) [NEW - cost-plus breakdown]
+-- Warranties (/warranties)
+-- Service Areas (/service-areas)
|   +-- City Pages (7 cities)
|   +-- Subdivision Pages (31 neighborhoods)
+-- Reviews (/reviews) [NEW - embedded real Google reviews]
+-- Gallery (/gallery) [NEW - before/after photos]
+-- Blog (/blog)
+-- Contact (/contact) [REBUILD with actual form]
+-- Financing (/financing) [NEW - if applicable]
```

---

### Design Direction

**Visual Identity**
- Commission professional logo for "All-Pro Roofing" -- retire generic "Roof Repair Services"
- Replace cartoon mascot with professional icon-based logo (roof silhouette, subtle military motif)
- Replace cartoon marine with actual photo of Johnny Sanchez
- Maintain navy blue (#1e3a5f) primary -- add warm amber/gold accent for CTAs
- Professional sans-serif font family (Inter, Outfit, or DM Sans)

**Photography**
- Professional photo shoot: Johnny with crew, before/after roofs, Johnny with service medals
- Project gallery showing recognizable Houston-area homes
- Every page should have real photography -- no stock, no cartoons

**Tone of Voice**
- Keep the direct, no-BS tone -- it's the biggest differentiator
- Keep "Pure Cost-Plus" as central messaging pillar
- Keep anti-corporate angle
- Add more of Johnny's personal voice -- short videos, "A message from Johnny" sections
- Maintain bilingual capability

---

### Content Strategy

**Keep (Working Well)**
- "Pure Cost-Plus Pricing" with itemized example -- brilliant and unique
- Military/first responder/teacher discount program
- "Johnny answers personally -- guaranteed" messaging
- "Se habla espanol"
- Phone-first conversion approach
- "Same-Day / Open Now" urgency signals

**Rewrite Completely**
- **About page** -- Needs Johnny's real story: where he served, when he came to Texas, why he started the company. Real photo. Most emotionally compelling page on the site.
- **All meta descriptions** -- Unique per page. Remove ALL "Carlos" references immediately.
- **All FAQ schema** -- Remove "Carlos," reference Johnny or use no names.
- **All testimonials** -- Embed real Google Reviews via widget (EmbedSocial, Elfsight) or get written permission from real customers with full names.

**Add New**
- Real Google Reviews integration
- Before/after gallery (15-20 projects)
- "Meet Johnny" video (60 seconds)
- Working contact form (name, phone, email, address, service type)
- Financing page
- Expanded blog (monthly posts)
- Emergency/24-hour section if applicable

---

### SEO Strategy

**Immediate Fixes (Week 1)**
1. Replace all "Carlos" with "Johnny" in meta descriptions, OG tags, Twitter cards, FAQ schema
2. Fix schema telephone to +17609783678
3. Install Google Analytics 4 and Search Console
4. Add working contact form
5. Reconcile review count claims to match reality (use actual Google count)

**On-Page SEO (Weeks 2-4)**
1. Add proper `<nav>` element with site-wide navigation
2. Diversify image alt text -- each image unique and descriptive
3. Add Service schema to service pages
4. Add BreadcrumbList schema to interior pages
5. Fix all 404 pages or remove from sitemap
6. Ensure city/subdivision pages have unique, locally-specific content

**Local SEO (Ongoing)**
1. Optimize Google Business Profile with correct NAP
2. Build citations: Yelp, BBB, Angi, HomeAdvisor, Houzz, Nextdoor
3. Review generation strategy -- follow up every completed job
4. Weekly Google Posts
5. Add to Apple Maps, Bing Places, Waze

**Content SEO (Monthly)**
1. Publish 2-4 blog posts targeting Houston-area roofing queries
2. Create comprehensive guides ("Complete Guide to Roof Replacement in Fort Bend County")
3. Target question-based queries for featured snippets

---

### Conversion Optimization

1. **Add a real contact form** -- even if Johnny prefers calls, many prefer forms
2. **Install analytics with conversion tracking** -- form submissions, phone clicks, "Free Estimate" clicks
3. **Add call tracking** (CallRail) -- attribute calls to pages/campaigns
4. **Embed real Google Reviews** -- replace fabricated testimonials
5. **Add sticky mobile CTA** -- fixed phone button at bottom of screen
6. **Fix "Free Estimate" link** -- add form or change CTA to "Call for Free Estimate"
7. **Add email** -- johnny@allprorooftx.com should be visible
8. **Fix/remove Recommended Contractors page** -- linking to competitors bleeds traffic
9. **Fix broken social media links** -- connect to real Facebook or remove

---

### Technical Stack Recommendation

**Immediate (Weeks 1-2): Fix Current Stack**
- Fix existing Lovable/Vite/React codebase
- Add GA4, GTM, Facebook Pixel
- Add form service (Formspree or Tally)
- Add review widget (Elfsight or Grade.us)

**Medium-term (Within 60 days): Migrate to Next.js**
- Next.js with static site generation for speed + SEO
- Sanity or Contentful for content management
- Deploy on Vercel
- Integrate CallRail, GA4, form backend
- Clean break from Lovable.dev template artifacts

---

### Priority Order

**CRITICAL -- Fix This Week**
1. Remove all "Carlos" references from meta/schema
2. Fix schema telephone number
3. Install Google Analytics 4 + Search Console
4. Add working contact form
5. Reconcile review count claims

**HIGH -- Within 30 Days**
6. Replace cartoons with real photography
7. Rewrite About page with Johnny's real story
8. Add site-wide `<nav>` navigation
9. Write unique meta descriptions for all pages
10. Fix broken social media footer links
11. Remove/nofollow Recommended Contractors page
12. Add email to contact page
13. Remove "Bronze Star" template artifacts

**MEDIUM -- Within 60 Days**
14. Install GTM, Facebook Pixel, CallRail
15. Embed real Google Reviews
16. Create project gallery with before/after photos
17. Record "Meet Johnny" video
18. Fix all 404s and update sitemap
19. Build proper ARIA accessibility
20. Consolidate brand name

---

### Competitive Advantages to Leverage

1. **Pure Cost-Plus Pricing Transparency** -- No other Houston roofer publishes itemized cost breakdowns. This is the single most powerful differentiator. Double down.

2. **100% Disabled Marine Veteran-Owned** -- Not a checkbox; it's an emotionally compelling story. Tell it with real photos and video.

3. **Personal Service** -- "Johnny answers personally -- guaranteed" is a promise no corporate company can make.

4. **Anti-Corporate Positioning** -- "$120K lifted truck" and "fat commissions" language resonates with burned homeowners.

5. **Budget-Friendly Inclusivity** -- "Everyone deserves a quality roof" is a message no competitor uses. Serving the underserved is both moral and strategic.

6. **Bilingual Service** -- Serves Fort Bend County's large Hispanic population. Most competitors are English-only.

7. **GAF Master Elite** -- Only 2% of roofers. Combined with cost-plus pricing, it answers "cheap = low quality."

---

**Bottom line:** The messaging foundation is already strong -- "Pure Cost-Plus" pricing transparency, veteran authenticity, and personal service are genuine differentiators. But the site is undermined by the "Carlos" problem, fabricated testimonials, inflated review counts, cartoon imagery, a non-functional contact form, zero analytics, and brand name confusion. Fix these technical and trust issues, and this site can dominate the Fort Bend County / southwest Houston roofing market.
