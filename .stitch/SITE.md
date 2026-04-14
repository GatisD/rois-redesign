# ROIS — Site Architecture

## About
**ROIS** is a Latvian digital marketing agency delivering measurable growth through Google Ads, Meta Ads, SEO, web development, and branding.

---

## Pages

### 1. Home (`/`) — [x] complete — `index.html`
- **Hero** — Bold headline, subheadline, primary CTA ("Sākt sadarbību"), secondary CTA ("Skatīt darbus")
- **Services Overview** — 5 service cards with icon, name, 1-line description
- **Results / Case Studies** — 3 metric-driven client wins (ROAS, traffic, conversions)
- **Why ROIS** — 4 differentiators (transparency, reporting, local expertise, speed)
- **Testimonials** — 3 client quotes with logo + name
- **CTA Banner** — Full-width "Ready to grow?" section
- **Footer** — Nav links, social icons, legal

### 2. Services (`/pakalpojumi`) — [x] complete — `services.html`
- Overview of all 5 services in a grid
- Each card links to dedicated service page

### 3. Google Ads (`/pakalpojumi/google-ads`) — [x] complete — `google-ads.html`
- Hero with service headline
- What's included (Search, PMax, Shopping, Remarketing)
- Process (Audit → Strategy → Launch → Optimise → Report)
- Relevant case study
- FAQ
- CTA

### 4. Meta Ads (`/pakalpojumi/meta-ads`) — [x] complete — `meta-ads.html`
- Hero with service headline
- What's included (Facebook, Instagram, Reels, Retargeting)
- Process section
- Relevant case study
- FAQ
- CTA

### 5. SEO (`/pakalpojumi/seo`) — [x] complete — `seo.html`
- Hero with service headline
- What's included (Technical, On-page, Content, Local SEO)
- Process section
- Relevant case study
- FAQ
- CTA

### 6. Web Development (`/pakalpojumi/web-izstrade`) — [x] complete — `web-development.html`
- Hero with service headline
- What's included (Next.js sites, landing pages, e-commerce, CRO)
- Tech stack showcase
- Relevant case study
- FAQ
- CTA

### 7. Branding (`/pakalpojumi/brendings`) — [x] complete — `branding.html`
- Hero with service headline
- What's included (Logo, identity, visual system, brand guidelines)
- Portfolio grid (placeholder images)
- Process section
- CTA

### 8. Case Studies (`/darbi`) — [x] complete — `case-studies.html`
- Filterable grid by service type (static tabs)
- 6 case study cards: TechBaltic, NordicDesign, EcoStyle, BalticSaaS, RigaStore, CreativeHub

### 9. Case Study Detail (`/darbi/[slug]`) — [x] complete
- `case-study-techbaltic.html` — TechBaltic: Google Ads, ROAS 1.8× → 6.1×
- `case-study-nordicdesign.html` — NordicDesign: Meta Ads, +180% pārdošana ar Reels, 4 mēneši — [x] complete
- Challenge / Before metrics / 3-part solution / Results grid / Timeline / Testimonial / Next case study strip

### 10. About (`/par-mums`) — [x] complete — `about.html`
- Agency story / mission
- Team section (photo, name, role)
- Values
- Partners / tools logos

### 11. Contact (`/kontakti`) — [x] complete — `contact.html`
- Contact form (Name, Email, Company, Service interest, Message)
- Contact info card with social links
- Response time promise

### 12. Privacy Policy (`/privatuma-politika`) — [x] complete — `privacy.html`
### 13. Terms (`/noteikumi`) — [x] complete — `terms.html`

---

## Navigation Structure

**Primary Nav:** Home | Services ▾ | Case Studies | About | Contact
**Service Dropdown:** Google Ads | Meta Ads | SEO | Web Development | Branding

**Footer Nav:**
- Column 1: Services
- Column 2: Company (About, Case Studies, Contact)
- Column 3: Legal (Privacy, Terms)
- Column 4: Social (LinkedIn, Facebook, Instagram)

---

## Global Components
- **Header** — Logo left, nav center, CTA button right, dark mode toggle
- **Footer** — 4-column grid, copyright
- **Cookie Banner** — GDPR compliant
- **Analytics** — GA4 + Meta Pixel (via environment variables)
