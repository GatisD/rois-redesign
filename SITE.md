# ROIS — Site Architecture

## About
**ROIS** is a Latvian digital marketing agency delivering measurable growth through Google Ads, Meta Ads, SEO, web development, and branding.

---

## Pages

### 1. Home (`/`)
- **Hero** — Bold headline, subheadline, primary CTA ("Sākt sadarbību"), secondary CTA ("Skatīt darbus")
- **Services Overview** — 5 service cards with icon, name, 1-line description
- **Results / Case Studies** — 3 metric-driven client wins (ROAS, traffic, conversions)
- **Why ROIS** — 4 differentiators (transparency, reporting, local expertise, speed)
- **Testimonials** — 3 client quotes with logo + name
- **CTA Banner** — Full-width "Ready to grow?" section
- **Footer** — Nav links, social icons, legal

### 2. Services (`/pakalpojumi`)
- Overview of all 5 services in a grid
- Each card links to dedicated service page

### 3. Google Ads (`/pakalpojumi/google-ads`)
- Hero with service headline
- What's included (Search, PMax, Shopping, Remarketing)
- Process (Audit → Strategy → Launch → Optimise → Report)
- Relevant case study
- FAQ
- CTA

### 4. Meta Ads (`/pakalpojumi/meta-ads`)
- Hero with service headline
- What's included (Facebook, Instagram, Reels, Retargeting)
- Process section
- Relevant case study
- FAQ
- CTA

### 5. SEO (`/pakalpojumi/seo`)
- Hero with service headline
- What's included (Technical, On-page, Content, Local SEO)
- Process section
- Relevant case study
- FAQ
- CTA

### 6. Web Development (`/pakalpojumi/web-izstrade`)
- Hero with service headline
- What's included (Next.js sites, landing pages, e-commerce, CRO)
- Tech stack showcase
- Relevant case study
- FAQ
- CTA

### 7. Branding (`/pakalpojumi/brendings`)
- Hero with service headline
- What's included (Logo, identity, visual system, brand guidelines)
- Portfolio grid (placeholder images)
- FAQ
- CTA

### 8. Case Studies (`/darbi`)
- Filterable grid by service type
- Each card: client industry, service, key metric, thumbnail

### 9. Case Study Detail (`/darbi/[slug]`)
- Client background
- Challenge
- Solution
- Results (metrics with visual callouts)
- Testimonial
- Next case study link

### 10. About (`/par-mums`)
- Agency story / mission
- Team section (photo, name, role)
- Values
- Partners / tools logos

### 11. Contact (`/kontakti`)
- Contact form (Name, Email, Company, Service interest, Message)
- Office location / map embed
- Response time promise
- Social links

### 12. Privacy Policy (`/privatuma-politika`)
### 13. Terms (`/noteikumi`)

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
