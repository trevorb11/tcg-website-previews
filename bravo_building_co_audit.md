# Bravo Building Co., Inc. -- Website Audit & Redesign Plan

**Audit Date:** June 22, 2026
**Website:** https://bravobuildingco.com/
**Business:** Bravo Building Co., Inc. -- General Contractor, Founded 1982
**Owner/CEO:** Gregory (Greg) Di Loreto
**Location:** Clayton/Pittsburg, CA (P.O. Box 1130, Clayton, CA 94517)
**Phone:** (925) 432-1314
**License:** CSLB #716268 (General Engineering, General Building, Swimming Pool)
**Service Area:** CA, NV, OR, WA, ID, MT, AZ
**Platform:** WordPress + Elementor Pro, WP Rocket 3.20.2, Yoast SEO
**BuildZoom Score:** 126 (Top 1% of 336,931 CA contractors)
**BBB:** Listed, NOT accredited

---

## PART 1: COMPREHENSIVE SITE AUDIT

---

### 1. Site Architecture & Navigation

**Current Pages (8 total in sitemap):**
| Page | URL | Title Tag |
|------|-----|-----------|
| Homepage | `/` | Bravo Building Co. \| Leading California & Nevada Contractors |
| Company/About | `/company/` | About Us \| Reliable Commercial Building & Estate Builders |
| Commercial | `/commercial/` | Commercial Construction Services for Your Business Needs |
| Residential | `/residential/` | Residential Construction Services to Enhance Your Home |
| Blog | `/blog/` | Expert Commercial & Residential Construction Management Insights |
| Gallery | `/gallery/` | Construction Gallery \| Top California & Nevada General Contractors |
| Employment | `/employment/` | Careers \| Join Our General Construction Company |
| Contact | `/contact/` | Contact Us \| California & Nevada Top General Contractors |
| Get a Quote | `/get-a-quote/` | Bravo Building Co - Get a Quote for your Construction Project |

**Navigation Structure:**
- Split navigation with logo centered: Left side (Home, Company, Commercial, Residential) | Logo | Right side (Blog, Employment, Gallery, Contact)
- Top utility bar with email, phone, and "Get a Quote Now" CTA button
- Footer navigation mirrors main nav
- No dropdown menus or sub-pages

**Navigation Issues:**
- Only 8 static pages for a company serving 7 states -- extremely thin site architecture
- No service sub-pages (e.g., seismic retrofits, tenant improvements, structural steel)
- No location/service-area pages
- No project case study pages
- "Get a Quote" is in the header bar but is NOT in the main navigation -- it is a separate hidden page
- Two separate contact entry points: `/contact/` and `/get-a-quote/` with slightly different forms and different email addresses displayed

---

### 2. Homepage Audit

**Design & UX:**
- Hero slider with 5 slides, each linking to Get a Quote -- functional but generic
- Slider image filenames are raw camera names (e.g., "20240910_154600", "20230807_125126", "BBCcrew") -- unprofessional and bad for SEO
- No H1 tag on the homepage -- significant SEO gap; page jumps straight to H2
- "Our Achievements" counter section shows all zeros ("0" for Completed Projects, Professional Workers, Satisfied Customers) -- this is a **critical bug**. The Elementor counter widgets have no target values configured or the animation is broken, leaving the page displaying "0" across all metrics
- Duplicate "Our Achievements" H3 heading appears twice in the DOM (with inconsistent spacing)
- Image carousel in "Our Latest Projects" section has images with missing alt text
- Overall layout follows a standard Elementor template pattern -- competent but not distinctive
- The "Why Choose bravo Building co." heading has inconsistent capitalization -- lowercase "bravo" and "co." looks like an oversight

**Content & Copy:**
- Opening copy is generic and AI-sounding: "known for our expert craftsmanship, cutting-edge technology, and commitment to quality"
- Uses emoji checkmarks and bullet symbols throughout -- somewhat unprofessional for a high-end contractor
- Does not mention BuildZoom Top 1% ranking anywhere on the homepage
- Does not mention 40+ year history on the homepage (only says "decades" vaguely)
- Does not name Greg Di Loreto or any team members
- Does not mention CSLB license number
- "For over two decades" in the Residential section contradicts the 1982 founding date (should be "over four decades")
- Testimonials section references "G.D.L. Construction Development, Inc." (the prior company name) without explanation -- potentially confusing
- One testimonial references a 1999 date and dinner party -- charming but reads as oddly personal/dated for a professional site
- CTA buttons link to `/contact/` not `/get-a-quote/` despite the header button linking to `/get-a-quote/` -- inconsistent funnel

**SEO:**
- Title: "Bravo Building Co. | Leading California & Nevada Contractors" -- decent but does not mention "general contractor" which is a primary keyword
- Meta description: "We offer top-notch residential and commercial construction services in California and Nevada. Let's get your major project started!" -- generic, does not mention founding year, BuildZoom ranking, or specific services
- No H1 tag -- major SEO issue
- H2-H4 structure is present but hierarchy skips from H2 to H4 in places
- Schema markup: WebPage, ImageObject, BreadcrumbList, WebSite, Organization -- present but missing LocalBusiness schema, which is critical for local SEO
- OG tags present and properly configured
- Canonical tag present
- 2 images missing alt text out of 20 total
- 2 links with no accessible text
- No lazy loading on images (0 of 20 have loading="lazy")
- Sitemap properly configured via Yoast

**Trust & Conversion:**
- BuildZoom logo in footer links to BuildZoom profile -- good but buried and small
- "Member of ABC & AGC" mentioned in footer text only -- no logos, no links, no detail
- Charity/cause logos in footer carousel (Salute America's Heroes, Wounded Warrior Project, Freedom Alliance, Reconnect America, Turning Point USA) -- all link to "#" (broken links)
- No Google reviews widget or review count displayed
- No BBB badge or link
- No CSLB license number displayed
- Testimonials exist but are from the old company name (G.D.L.) and are dated (1990s-era references)
- No video content
- No case studies or project detail pages

---

### 3. Company/About Page Audit

**Content:**
- H1: "ABOUT BRAVO BUILDING CO. INC" -- present but ALL CAPS looks template-like
- Subtitle: "Family Run Business Building Excellence Since 1982" -- good, mentions founding year
- Says "Headquartered in Walnut Creek, CA" -- **factual inconsistency**. The Contact and Quote pages list the address as Clayton, CA 94517. Company records indicate Clayton/Pittsburg. This discrepancy could hurt local SEO and trust
- No team photos, no leadership bios, no mention of Greg Di Loreto by full name (only referenced indirectly in testimonials as "Greg")
- No company history timeline despite 40+ years of operation
- No mention of BuildZoom Top 1% ranking
- No project count, revenue figures, or concrete proof points
- Copy uses emoji icons (checkmarks, location pins) -- inconsistent with professional contractor branding
- Single image: "LafayetteHotel" -- only one photo on the entire About page
- "Our Mission" section reads as generic AI-generated content

**SEO:**
- Title: "About Us | Reliable Commercial Building & Estate Builders" -- does not include company name
- Meta description mentions only California and Nevada, despite serving 7 states

---

### 4. Commercial Services Page Audit

**Content:**
- H1: "Commercial Construction Solutions Built for Success" -- good keyword targeting
- Lists service categories well: Planning & Development, Design & Engineering, Project Execution
- Industries served list is solid: Retail, Corporate, Warehousing, R&D, Manufacturing, Seismic
- Only one image on the entire page ("a commercial building") -- needs more project photography
- No case studies, project examples, or before/after galleries
- No mention of specific completed projects or client names
- "Established in 1982" is mentioned -- good

**SEO:**
- Title: "Commercial Construction Services for Your Business Needs" -- generic, no company name, no location
- No specific location keywords for multi-state SEO

---

### 5. Residential Services Page Audit

**Content:**
- H1: "Residential Construction Services for Homes of Distinction" -- good
- H2 used as subtitle: "Exceptional Craftsmanship. Timeless Design. Unmatched Quality." -- reads as AI-generated tagline
- Three service cards with icon placeholders but the icons render as empty boxes
- 5-step process outlined but formatted as plain paragraphs with bullet characters, not a designed visual timeline
- "trusted name in custom home construction since 1982" -- good mention
- No project photos at all on this page -- significant gap for a luxury home builder
- No pricing ranges or project scope examples
- No client testimonials specific to residential

**SEO:**
- Title: "Residential Construction Services to Enhance Your Home" -- generic, no company name, no location
- "Serving CA, NV, OR, WA, ID, MT & AZ" mentioned in text -- good for indexing

---

### 6. Contact Page Audit

**Content:**
- H1: "Contact Bravo Building Co." -- good
- Form fields: Name, Phone (spinbutton type -- should be text/tel), Email, Message
- reCAPTCHA present -- good for spam prevention
- Address shown: P.O. Box 1130, Clayton, CA 94517
- No Google Map embed
- No office hours listed
- No response time expectation set
- Phone field uses `spinbutton` input type instead of `tel` -- poor UX, especially on mobile where it should trigger a phone number keypad

**Email Inconsistency (Critical):**
- Header bar across all pages: `OfficeMgr@BravoBuildingco.com`
- Contact page text: `Officemgr@bravobuildingco.com`
- Get a Quote page text: `bbc@bravobuildingco.com`
- Known business email (per brief): `info@bravobuildingco.com`
- This is four different email addresses displayed across the site -- extremely confusing and unprofessional

---

### 7. Get a Quote Page Audit

**Content:**
- More detailed form than Contact page: adds Business Name field and Project Type dropdown (Commercial/Residential)
- reCAPTCHA present
- Shows `bbc@bravobuildingco.com` as contact email (different from header)
- Essentially duplicates the Contact page with a slightly better form -- should be consolidated

---

### 8. Blog Audit

**Content:**
- 54 blog posts across 5 pages -- relatively active content marketing
- Blog title: "Expert Commercial & Residential Construction Management Insights"
- Topics cover a good range: commercial zoning, foundation cracks, drainage, leaking windows, safety assessments, tenant renovations, environmental hazards
- Content reads as SEO-focused but AI-generated -- long, verbose paragraphs with generic advice rather than project-specific expertise
- No author attribution on posts
- No publish dates visible in the feed
- No categories or tags visible for filtering
- No internal linking strategy evident from post titles
- Posts lack Bravo-specific case studies or project references
- Blog images use descriptive alt text -- adequate

**SEO Value:**
- Good topical coverage for construction keywords
- Posts are well-structured with proper URL slugs
- However, content lacks E-E-A-T signals (no author bios, no credentials, no first-person project experience)
- No schema markup for blog articles (BlogPosting or Article)

---

### 9. Gallery Page Audit

**Content:**
- Filterable gallery with "All", "Residential", "Commercial" categories -- good UX feature
- Approximately 80+ images -- substantial portfolio
- Many images lack alt text entirely (referenced by generic "Residential - 1" through "Residential - 39" numbering)
- No project descriptions, client names, locations, or context for any photos
- Images are raw uploads with camera filenames (e.g., "20220520_152950.jpg")
- No lightbox descriptions
- Sitemap shows 0 images indexed for the Gallery page -- images may not be crawlable

**Key Issue:** The gallery is a wasted SEO opportunity. Each major project should have its own page with before/after photos, project details, scope, budget range, and location -- creating dozens of indexable, keyword-rich pages.

---

### 10. Employment Page Audit

**Content:**
- Well-organized job listings for both office and field positions
- Benefits mentioned: Health, Medical, Dental, Vision, 401K
- No application form on the page -- directs to email only
- No company culture section, team photos, or employee testimonials
- No salary ranges (though common in construction)

---

### 11. Technical Audit

| Metric | Finding | Grade |
|--------|---------|-------|
| Platform | WordPress + Elementor Pro | Adequate |
| Caching | WP Rocket 3.20.2 | Good |
| SEO Plugin | Yoast SEO | Good |
| SSL/HTTPS | Fully secured, no mixed content | Good |
| Page Load (homepage) | ~647ms DOMContentLoaded, 312ms TTFB | Good |
| Total Resources | 73 on homepage | Moderate (could reduce) |
| JS Files | 28 | High -- could consolidate |
| CSS Files | 28 | High -- could consolidate |
| Lazy Loading | 0 of 20 images use lazy loading | Poor |
| Image Optimization | Camera-named files, no WebP | Poor |
| Mobile Responsive | Yes, detects mobile viewport, hamburger menu present | Good |
| Console Errors | 1 error on homepage load | Minor |
| Robots.txt | Properly configured via Yoast | Good |
| Sitemap | 4 sitemaps (posts, pages, categories, authors) | Good |
| Schema Markup | WebPage, Organization, BreadcrumbList -- missing LocalBusiness | Needs work |
| Social Media Links | None found on site | Missing |
| Google Map | Not present on Contact page | Missing |
| Google Reviews Widget | Not present | Missing |
| Accessibility | 2 images missing alt, 2 links without text, phone input as spinbutton | Needs work |

---

### 12. Branding Audit

**Logo:** Present, centered in navigation, links to homepage -- adequate but small/nondescript in screenshots
**Color Scheme:** Dark blue/navy primary, gold/amber accent -- professional for construction
**Typography:** Clean sans-serif -- adequate
**Imagery:** Mix of quality job-site photos and raw camera uploads -- inconsistent
**Voice/Tone:** Attempts premium/luxury positioning but undercut by AI-generated copy, emoji usage, and template-like formatting

**Key Branding Gaps:**
- No clear differentiator communicated -- "Excellence" and "Precision" are what every contractor says
- The 40+ year legacy is the strongest brand asset but is underutilized
- BuildZoom Top 1% ranking is an extraordinary differentiator that is essentially hidden in the footer
- No personal branding around Greg Di Loreto despite being a founder-led company
- Charity involvement (Wounded Warrior, Freedom Alliance) could be a strong brand differentiator but is relegated to broken footer links
- Footer says "General Contractors in Walnut Creek" (via BuildZoom link) while contact info says Clayton -- identity confusion

---

### 13. Competitive Analysis Summary

**What Bravo has that competitors likely lack:**
- 40+ years in business (since 1982) -- most competitors are 10-20 years old
- BuildZoom Top 1% ranking out of 336,931 contractors -- extraordinary credential
- Multi-state licensing across 7 states -- rare for a general contractor
- CSLB triple classification (General Engineering + General Building + Swimming Pool)
- Demonstrated both commercial and luxury residential capability
- Active blog with 54 posts (more than most competitors)

**What competitors likely have that Bravo lacks:**
- Team/leadership pages with bios and photos
- Detailed project case studies with scopes, timelines, and budgets
- Google Reviews integration (and active review solicitation)
- Social media presence and integration
- Video content (project walkthroughs, drone footage, team introductions)
- Location-specific landing pages
- Professional photography with proper naming and alt text
- Consistent branding and contact information

---

## PART 2: RECOMMENDED REDESIGN PLAN

---

### 1. Recommended Site Architecture

**Tier 1 -- Primary Navigation:**

```
Home
About
  |-- Our Story (history timeline, founding, evolution from GDL)
  |-- Leadership & Team (Greg Di Loreto bio, key team members)
  |-- Certifications & Awards (BuildZoom, CSLB, ABC, AGC, BBB)
  |-- Community Involvement (charity work, veterans support)
Services (mega menu)
  |-- Commercial Construction
  |     |-- Ground-Up Construction
  |     |-- Tenant Improvements
  |     |-- Seismic Retrofits
  |     |-- Structural Steel
  |     |-- Warehousing & Industrial
  |     |-- Retail & Office
  |  -- Residential Construction
  |     |-- Custom Estate Homes
  |     |-- Luxury Renovations
  |     |-- Pool Construction (leverage CSLB swimming pool license)
  |     |-- Architectural Collaboration
Projects (replaces Gallery)
  |-- Commercial Projects (filterable)
  |-- Residential Projects (filterable)
  |-- [Individual Case Study Pages]
Service Areas
  |-- California (primary, with city sub-pages)
  |-- Nevada
  |-- Oregon
  |-- Washington
  |-- Idaho
  |-- Montana
  |-- Arizona
Blog / Insights
Careers
Contact / Get a Quote (consolidated into one page)
```

**Total target pages: 40-60** (up from current 8)

---

### 2. Design Direction Improvements

**Header:**
- Consolidate to single "Get a Quote" CTA -- remove the split between Contact and Get a Quote
- Standardize one email address across the entire site
- Add phone number more prominently with click-to-call on mobile
- Add social media icons (once profiles are created)

**Homepage Redesign:**
- Add a proper H1 tag above the fold
- Replace generic slider with a single hero image/video with strong value proposition: "Top 1% California General Contractor Since 1982"
- Fix or replace the broken counter section with real, verifiable numbers
- Add a "Why We're Different" section featuring: 40+ years, BuildZoom Top 1%, 7-state coverage, triple CSLB license
- Add a featured projects section with 3-4 case studies (not just a photo carousel)
- Modernize testimonials with client photos, company names, and star ratings
- Add a Google Reviews embed/widget
- Replace emoji checkmarks with proper icon design

**Overall Design:**
- Remove all emoji characters from body copy (checkmarks, location pins, etc.)
- Invest in professional project photography with proper file naming
- Create consistent page templates for service pages (hero, service details, related projects, CTA)
- Add breadcrumb navigation for SEO and UX
- Fix the capitalization inconsistency in "Why Choose bravo Building co."

---

### 3. Content Strategy

**Content to Keep:**
- Blog infrastructure and topical coverage (54 posts is a strong foundation)
- Gallery photos (just need reorganization and context)
- Service descriptions for Commercial and Residential (as a starting point)
- Core business information and service lists

**Content to Rewrite:**
- All page copy -- remove AI/generic tone, add specific project references, numbers, and Greg's voice
- Testimonials section -- add context, update from G.D.L. references, explain company evolution
- About page -- completely rewrite with authentic story, timeline, and team bios
- Meta descriptions for every page -- add specific differentiators and locations
- All image alt text -- descriptive, keyword-appropriate text

**Content to Add:**
- **Greg Di Loreto bio/leadership page** -- this is a founder-led company; his 40+ years of experience is the brand
- **Team page** with photos and bios for key personnel (superintendents, project managers)
- **10-15 project case studies** with before/after photos, scope descriptions, budgets, timelines, client testimonials tied to specific projects
- **Location landing pages** for each state (7 pages minimum) and key metro areas in California (Walnut Creek, Concord, Clayton, Pittsburg, East Bay, San Francisco, etc.)
- **Service-specific pages** for each major service offering (8-12 pages)
- **Video content** -- drone footage of completed projects, client testimonial videos, "Day in the Life" crew content
- **FAQ page** addressing common contractor questions
- **Process page** detailing the Bravo construction process from inquiry to completion
- **Company timeline/history page** -- 1982 founding to present

**Blog Strategy:**
- Rewrite top-performing posts to add first-person expertise, project photos, and Bravo-specific references
- Add author bios (Greg Di Loreto and/or team members) with credentials
- Implement proper BlogPosting schema on all posts
- Add publish dates and categories to the blog feed
- Create location-specific posts (e.g., "Commercial Construction Trends in [City], CA")
- Reduce frequency but increase quality -- one deeply authoritative post per month beats four generic ones

---

### 4. SEO Strategy

**Technical SEO (Immediate):**
- Add H1 tags to the homepage (currently missing)
- Implement LocalBusiness schema (with address, phone, service area, founding date, license number)
- Add lazy loading to all images
- Rename image files from camera names to descriptive keywords
- Convert images to WebP format
- Fix the duplicate H3 "Our Achievements" heading
- Consolidate CSS/JS files (28 each is excessive)
- Add proper BlogPosting/Article schema to all blog posts
- Fix broken charity links in footer (currently all point to "#")

**On-Page SEO:**
- Rewrite all title tags to include: company name + primary keyword + location
  - Homepage: "Bravo Building Co. | Top 1% General Contractor in California Since 1982"
  - Commercial: "Commercial Construction Services | Bravo Building Co. | CA, NV, OR"
  - Residential: "Custom Estate Home Builders | Bravo Building Co. | Luxury Construction"
- Rewrite all meta descriptions with specific differentiators (Top 1%, 40+ years, 7 states)
- Add descriptive alt text to all images with location and service keywords
- Implement proper heading hierarchy on every page (H1 > H2 > H3, no skipping)

**Local SEO (Multi-State):**
- Create individual location landing pages for all 7 states
- Create city-level pages for top California markets (Walnut Creek, Concord, Clayton, Pittsburg, Lafayette, Danville, San Ramon, Oakland, San Francisco)
- Optimize Google Business Profile (verify it exists and is claimed)
- Build NAP (Name, Address, Phone) consistency across all directories -- fix the Walnut Creek vs. Clayton discrepancy
- Create and optimize listings on: Google Business, Yelp, Houzz, Angi, HomeAdvisor, BuildZoom (already present), BBB
- Pursue BBB accreditation or at minimum respond to the existing listing

**Content SEO:**
- Add E-E-A-T signals throughout: author bios with credentials, CSLB license numbers, years of experience, specific project references
- Internal linking strategy: every blog post should link to relevant service pages; every service page should link to relevant case studies
- Target long-tail keywords specific to their niche: "seismic retrofit contractor California", "luxury estate builder East Bay", "commercial ground-up construction Nevada"

---

### 5. Conversion Optimization

**Immediate Fixes:**
- Consolidate `/contact/` and `/get-a-quote/` into a single, prominent conversion page
- Standardize one email address across the entire site
- Fix phone input field type from `spinbutton` to `tel`
- Add Google Maps embed to contact page
- Add office hours and response time expectations
- Fix the broken counter widgets (showing "0") -- either configure with real numbers or remove entirely

**Conversion Enhancements:**
- Add a sticky header CTA that follows the user on scroll
- Add contextual CTAs on every service page (not just a generic "Get a Quote" button)
- Implement a project-type-specific intake form (what type of project, approximate budget, timeline, location)
- Add trust badges above the fold: BuildZoom Top 1%, ABC member, AGC member, CSLB licensed, 40+ years
- Add a Google Reviews widget showing real ratings and review count
- Create a "Request Consultation" chatbot or scheduling tool (Calendly integration)
- Add phone click-to-call tracking for analytics
- Add form submission tracking in Google Analytics/Tag Manager

**Social Proof Enhancements:**
- Actively solicit Google Reviews from past clients
- Create a dedicated testimonials page with categorized reviews (commercial, residential)
- Add client logos for commercial work (with permission)
- Display specific metrics: projects completed, square footage built, years in business, states served

---

### 6. Social Media & Directory Improvements

**Social Media (Currently Zero Presence):**
- Create and maintain profiles on:
  - LinkedIn (critical for commercial clients) -- company page + Greg Di Loreto personal profile
  - Instagram (essential for showcasing residential luxury work)
  - Facebook (general presence, community engagement)
  - YouTube (project walkthroughs, drone footage, testimonial videos)
- Post cadence: 3-4 times per week on Instagram/Facebook, 2 times per week on LinkedIn
- Content: project progress photos, completed project reveals, team spotlights, safety milestones, community involvement

**Directory Optimization:**
- Claim and optimize: Google Business Profile, Yelp, Houzz, Angi, HomeAdvisor, Porch, Thumbtack
- Ensure NAP consistency across all directories (resolve Walnut Creek vs. Clayton)
- Add photos, service descriptions, and response to reviews on all platforms
- Consider BBB accreditation (currently listed but not accredited)

---

### 7. Technical Recommendations

| Priority | Item | Impact |
|----------|------|--------|
| Critical | Fix counter widgets (showing "0") | Trust/credibility |
| Critical | Add H1 to homepage | SEO |
| Critical | Standardize email address across site | Trust/conversion |
| Critical | Fix broken charity footer links | UX/trust |
| High | Add LocalBusiness schema | Local SEO |
| High | Add lazy loading to images | Performance |
| High | Rename/optimize images (WebP, descriptive names) | SEO/Performance |
| High | Fix phone input type on forms | Mobile UX |
| High | Add Google Maps to contact page | Conversion |
| Medium | Consolidate JS/CSS files | Performance |
| Medium | Add BlogPosting schema to posts | SEO |
| Medium | Implement breadcrumb navigation | SEO/UX |
| Medium | Fix capitalization in "Why Choose bravo Building co." | Brand consistency |
| Medium | Resolve HQ location discrepancy (Walnut Creek vs. Clayton) | Local SEO/trust |
| Low | Add accessibility improvements (alt text, link text) | Compliance |
| Low | Remove emoji characters from copy | Brand polish |

---

### 8. Priority Order of Improvements

**Phase 1 -- Critical Fixes (Week 1-2):**
1. Fix the counter widgets showing "0" on homepage
2. Add H1 tag to homepage
3. Standardize one email address across the entire site
4. Fix broken charity/cause links in footer
5. Fix "bravo Building co." capitalization
6. Correct headquarters location (Clayton, not Walnut Creek)
7. Fix phone input field type on forms

**Phase 2 -- SEO Foundation (Week 2-4):**
1. Rewrite all title tags and meta descriptions
2. Add LocalBusiness schema markup
3. Add descriptive alt text to all images
4. Rename image files to descriptive keywords
5. Enable lazy loading
6. Add H1 tags to any pages missing them
7. Fix heading hierarchy across all pages

**Phase 3 -- Content & Trust (Month 2):**
1. Write Greg Di Loreto leadership bio and team page
2. Create 5 initial project case studies with photos and details
3. Consolidate Contact and Get a Quote pages
4. Add Google Reviews widget
5. Add trust badges (BuildZoom Top 1%, CSLB, ABC, AGC) prominently on homepage
6. Rewrite About page with authentic company story and timeline
7. Add Google Maps embed to contact page

**Phase 4 -- Expansion (Month 2-3):**
1. Create location landing pages for all 7 states
2. Create city-level pages for key California markets
3. Create individual service pages for each major offering
4. Create social media profiles (LinkedIn, Instagram, Facebook)
5. Begin blog content refresh -- rewrite top 10 posts with E-E-A-T signals

**Phase 5 -- Ongoing (Month 3+):**
1. Publish 1-2 high-quality blog posts per month
2. Post on social media 3-4 times per week
3. Actively solicit Google Reviews after project completion
4. Add video content (project walkthroughs, testimonials)
5. Build out remaining case studies (target 15-20 total)
6. Monitor and optimize based on search console data

---

### 9. What Makes This Site Better Than Competitors (After Redesign)

After implementing these changes, Bravo Building Co. would differentiate from competitors through:

1. **Heritage Authority** -- Very few contractors can claim 40+ years of continuous operation since 1982. A well-told company story with timeline and evolution from GDL to Bravo creates unmatched credibility.

2. **BuildZoom Top 1% Ranking** -- This third-party verification (top 1% of 336,931 California contractors) is an extraordinary credential that almost no competitor can match. It should be front and center, not buried in a footer logo.

3. **Multi-State Reach** -- Most general contractors serve a single metro area. Active licensing across 7 western states positions Bravo for large-scale commercial clients and developers who need a contractor capable of working across multiple jurisdictions.

4. **Triple CSLB Classification** -- Holding General Engineering, General Building, AND Swimming Pool licenses demonstrates breadth of capability that most competitors lack.

5. **Dual Expertise** -- The ability to execute both multi-million-dollar commercial developments and luxury custom estate homes is rare. Most contractors specialize in one or the other.

6. **Founder-Led Authenticity** -- Once Greg Di Loreto's story, expertise, and personal involvement are showcased, the company transforms from a generic contractor website into a relationship-driven, trust-based brand.

7. **Community Involvement** -- Support for Wounded Warrior Project, Freedom Alliance, and veterans causes differentiates from competitors and resonates emotionally with clients. This story needs to be told, not just shown as broken logo links.

8. **Content Authority** -- With 54 existing blog posts (more than most competitors) and a plan to upgrade quality with real project expertise, Bravo can dominate search results for construction-related queries in their service areas.

---

### Summary of Critical Findings

| Category | Current Grade | Post-Redesign Target |
|----------|--------------|---------------------|
| Design & UX | C+ | A- |
| Content & Copy | C | A |
| SEO | C+ | A |
| Trust & Conversion | D+ | A |
| Technical | B- | A |
| Branding | C | A- |
| Social Presence | F | B+ |
| **Overall** | **C** | **A-** |

The Bravo Building Co. website has a solid WordPress/Elementor foundation and decent technical infrastructure, but it dramatically underperforms relative to the company's actual credentials and reputation. The most significant gaps are: (1) broken elements damaging credibility (zero counters, broken links, inconsistent contact info), (2) failure to leverage extraordinary differentiators (BuildZoom Top 1%, 40+ year history, 7-state coverage), (3) generic AI-sounding content that does not reflect the authentic expertise of a founder-led company, and (4) extremely thin site architecture (8 pages) for a company that should have 40-60 pages targeting multiple services, locations, and projects.

The raw materials for an exceptional website are all present -- the company history, the credentials, the project portfolio, the blog foundation. What is missing is the strategic packaging of those assets into a conversion-optimized, SEO-dominant, trust-building online presence.
