# PRD: FinTech Consumer Content Hub
### fintech.com/stories — MVP Launch

---

| | |
|---|---|
| **Product** | Consumer Content Hub (fintech.com/stories) |
| **Document Type** | Product Requirements Document (PRD) |
| **Status** | Completed |
| **PRD Initiated** | Q1 2022 |
| **Sprint Zero** | Late March 2022 |
| **Full Platform Cutover** | May 2023 |
| **Platform** | Adobe Experience Manager (AEM) |
| **Author** | Digital Product |
| **Stakeholders** | Marketing, Digital PO, UX, AEM Tech/Dev, SEO, Accessibility, Tagging |

---

## Table of Contents

1. [Overview](#1-overview)
2. [Background & Problem Statement](#2-background--problem-statement)
3. [Goals & Success Metrics](#3-goals--success-metrics)
4. [Scope](#4-scope)
5. [User Personas](#5-user-personas)
6. [Functional Requirements](#6-functional-requirements)
7. [Non-Functional Requirements](#7-non-functional-requirements)
8. [Content Model](#8-content-model)
9. [Team & Governance](#9-team--governance)
10. [Dependencies & Risks](#10-dependencies--risks)
11. [Launch Readiness Checklist](#11-launch-readiness-checklist)
12. [Future Roadmap](#12-future-roadmap-post-mvp)
- [Appendix](#appendix)

---

## 1. Overview

This document defines the requirements for the MVP launch of the FinTech Consumer Content Hub — a dedicated editorial destination at fintech.com/stories designed to deliver financial guidance, product education, and money-life content that deepens consumer relationships and drives conversion.

The Content Hub represents a strategic evolution from an aging, disconnected WordPress blog. The MVP consolidates existing article content into Adobe Experience Manager (AEM), establishes the content taxonomy and UX foundation, and creates the infrastructure for a personalized, high-engagement content experience in future phases.

> **Strategic Objective**
> - Develop deeper relationships with consumers through relevant, timely financial content
> - Deliver the right content at the right time to move consumers through the funnel
> - Turn consumers into customers by connecting content to product moments
> - Propagate content value throughout the broader digital ecosystem (app, email, social, unauthenticated webpages)

---

## 2. Background & Problem Statement

### 2.1 Current State

Prior to this initiative, the company's consumer financial content lived on a standalone WordPress instance that had become unintegrated with the broader digital ecosystem and difficult to maintain. Content management was siloed from the primary AEM platform, creating authoring friction, inconsistent brand experiences, and an inability to connect content to product pages, calculators, or conversion flows.

A cross-functional discovery process — including stakeholder interviews, an experience audit, and competitive analysis — surfaced consistent themes:

- Content is great, but it is not connected across the ecosystem
- Articles function as dead ends — when users reach the bottom of a page, there is nowhere meaningful to go
- The content hub does not reward user engagement or surface related content intelligently
- Users do not realize the full benefit of the company's content library
- Product placement within content is underdeveloped — it is not about your mortgage, it is about your home

### 2.2 The Opportunity

The company has 2+ years of content strategy investment and a growing library of financial guidance content. The opportunity is to build a content hub that functions less like a blog archive and more like a personalized financial media destination — one that builds trust, surfaces the right content at the right moment, and creates natural pathways to product consideration.

Best-in-class benchmarks identified during discovery included Pinterest (discovery and personalization), Spotify (curated content feeds), NerdWallet (financial content + product integration), Medium (editorial reading experience), and Netflix (recommendation logic). These informed the design principles for the MVP and future roadmap.

---

## 3. Goals & Success Metrics

### 3.1 MVP Goals

- Migrate and consolidate existing WordPress article content into AEM
- Establish a scalable content taxonomy (topics, subtopics, product affiliation)
- Launch a production-grade editorial experience at fintech.com/stories
- Implement foundational SEO, accessibility, and tagging infrastructure
- Enable AEM authors to create and publish new articles without engineering support
- Surface related content to reduce dead-end article experiences
- Establish baseline analytics to track engagement and content performance

### 3.2 Success Metrics

| Metric | Baseline (Pre-Launch) | MVP Target |
|---|---|---|
| Pages per session (content hub) | 1.2 | 1.8+ |
| Avg. time on page (articles) | Establish baseline | 2:30+ minutes |
| Article-to-product click-through rate | Establish baseline | Track & report |
| Content authoring cycle time | 5+ days (WordPress) | 2 days (AEM) |
| Content hub organic search traffic | Establish baseline | Month-over-month growth |
| Accessibility compliance (WCAG 2.1 AA) | Unknown | 100% on launch |

---

## 4. Scope

### 4.1 In Scope — MVP

- **Content migration:** Import and restructure existing WordPress articles into AEM content model
- **Article page template:** AEM component-based layout for long-form editorial content
- **Content hub homepage** (fintech.com/stories): Featured content, topic navigation, article listing
- **Topic/category pages:** Filtered article listings by financial topic (e.g., Home Buying, Saving, Investing)
- **Related content module:** Rule-based or tag-driven surfacing of related articles at article conclusion
- **Author profile component:** Byline, credentials, photo for editorial trust signals
- **Product callout component:** Inline or end-of-article CTA linking to relevant product pages
- **Search integration:** Articles indexed and surfaced through site search
- **SEO foundations:** Metadata, canonical URLs, structured data (Article schema), XML sitemap inclusion
- **Tagging:** Adobe Analytics event tagging for content engagement tracking
- **Accessibility:** WCAG 2.1 AA compliance validated across all new components
- **CMS authoring:** Author-friendly component configuration, no-code article publishing workflow

### 4.2 Out of Scope — MVP (Future Phases)

- Personalization engine or behavioral content recommendations
- User accounts, saved articles, or reading history
- Video content hosting or native video player
- Interactive tools or calculators embedded in articles
- Email newsletter integration or content subscription flows
- Social sharing optimization beyond Open Graph tags
- AI-generated content or dynamic content assembly
- Mobile app content syndication

---

## 5. User Personas

The Content Hub serves two primary user types and one internal user type.

### 5.1 The Researching Consumer

A non-customer actively exploring a financial decision — buying a home, opening a savings account, refinancing a loan. They arrive via organic search or social referral and are in a trust-building phase. They need credible, accessible financial guidance and subtle exposure to product options without hard-sell interruption.

- **Needs:** Trustworthy, readable financial content; clear next steps; relevant product context
- **Behaviors:** Skims headers, reads comparisons and lists, bounces if content feels promotional
- **Success:** Reads full article, clicks related article or product CTA

### 5.2 The Existing Customer

A current account holder exploring adjacent financial topics — expanding their financial relationship with the brand. They may arrive from email, the app, or direct navigation. They have baseline trust and are more likely to convert on product CTAs if content is relevant to their current life stage.

- **Needs:** Content tailored to where they are in their financial journey; easy access to account actions
- **Behaviors:** More likely to read deeply, more receptive to product placement
- **Success:** Engages with related content, clicks through to product pages

### 5.3 The AEM Content Author

An internal marketing team member responsible for creating, editing, and publishing articles. They are not engineers. They need a component-based authoring experience that allows them to produce high-quality articles quickly without developer support, with clear guardrails on design and SEO requirements.

- **Needs:** Intuitive AEM component authoring, clear field labels, preview capability
- **Success:** Publishes a new article end-to-end in under 2 hours without IT tickets

---

## 6. Functional Requirements

Features are organized by area. Priority designations: **P0** = launch blocker, **P1** = MVP required, **P2** = post-MVP.

### 6.1 Content Hub Homepage (fintech.com/stories)

| Feature | Description | Priority | Notes |
|---|---|---|---|
| Hero / Featured Article | Prominent placement for editorially-selected lead article with image, headline, and summary | P0 | AEM author-configured |
| Topic Navigation Bar | Horizontal nav filtering articles by primary topic category | P0 | Topics: Home, Savings, Auto, Investing, etc. |
| Article Card Grid | Listing of recent articles with thumbnail, title, topic tag, and read time | P0 | Paginated or load-more |
| Topic Category Filters | Filter article grid by topic tag | P1 | URL parameter-driven |
| Trending / Editors Picks Module | Curated secondary content placement | P1 | Manual curation by author |
| Email Signup Module | Optional newsletter opt-in placement | P2 | Post-MVP integration |

### 6.2 Article Page Template

| Feature | Description | Priority | Notes |
|---|---|---|---|
| Article Body | Rich text with headings, paragraphs, callout blocks, inline images | P0 | AEM RTE component |
| Article Header | Headline, subheadline, hero image, publish date, read time | P0 | Structured fields |
| Author Byline | Author name, title, photo, credentials | P0 | Author profile component |
| Topic Tags | Article topic tags linking to category pages | P0 | Taxonomy-driven |
| Related Articles Module | 3–4 article cards at article end, tag-matched | P0 | Rule-based, no ML required |
| Product Callout CTA | Inline or end-of-article product link with descriptive copy | P1 | Configurable by author |
| Social Share Buttons | Share to Facebook, X (Twitter), LinkedIn, copy link | P1 | Open Graph meta required |
| Table of Contents | Anchor-linked section navigation for long-form articles | P1 | Auto-generated from H2s |
| Article Series Module | Link to next/previous article in an editorial series | P2 | Post-MVP |
| Comments / Community | Reader comments or Q&A section | P2 | Post-MVP |

### 6.3 Topic / Category Pages

| Feature | Description | Priority | Notes |
|---|---|---|---|
| Category Header | Topic name, description, hero image | P0 | Author-configurable |
| Article Listing | Filtered grid of articles by topic tag | P0 | Sorted by recency |
| Sub-topic Filters | Secondary filter within a topic (e.g., Home Buying > Mortgages) | P1 | Phase 1 taxonomy design |
| Topic SEO Metadata | Unique meta title, description per category page | P0 | AEM page properties |

### 6.4 Content Migration

| Feature | Description | Priority | Notes |
|---|---|---|---|
| WordPress Content Import | Migrate existing article library from WordPress to AEM content model | P0 | One-time migration |
| URL Redirect Mapping | 301 redirects from WordPress URLs to AEM URLs | P0 | SEO continuity |
| Media Asset Migration | Transfer images and media from WordPress to AEM DAM | P0 | Image optimization required |
| Content QA Review | Author review of migrated content for formatting and accuracy | P0 | Manual QA process |
| Taxonomy Mapping | Map legacy WordPress categories/tags to new AEM taxonomy | P0 | Pre-migration deliverable |

---

## 7. Non-Functional Requirements

### 7.1 SEO

- All article pages implement Article structured data (schema.org/Article)
- Unique, author-configurable meta title and meta description per page
- Canonical URL implementation on all article and category pages
- XML sitemap inclusion for all published content hub pages
- Clean URL structure: `fintech.com/stories/[topic]/[article-slug]`
- Core Web Vitals targets: LCP < 2.5s, CLS < 0.1, FID < 100ms

### 7.2 Accessibility

- WCAG 2.1 Level AA compliance required on all new components before launch
- All images require descriptive alt text — enforced in AEM authoring dialog
- Color contrast ratios must meet AA minimums (4.5:1 for body text)
- Keyboard navigation and screen reader compatibility validated by the accessibility team
- Accessibility sign-off required as a launch gate

### 7.3 Performance

- Page load time target: < 3 seconds on a 4G mobile connection
- Images must use responsive srcset and lazy loading
- AEM component output must pass front-end performance review before release

### 7.4 Analytics & Tagging

- Adobe Analytics: page views, scroll depth, time on page, outbound CTA clicks
- Content hub section tag on all pages for funnel segmentation
- Article topic and product affiliation captured as eVars for content performance reporting
- Tagging QA sign-off required before launch

---

## 8. Content Model

The following fields define the AEM content model for Article pages. All fields are author-configurable in the AEM Touch UI authoring dialog.

| Field Name | Type | Description | Required |
|---|---|---|---|
| Headline | Text | Primary article title (H1). Also populates meta title if not overridden. | Yes |
| Subheadline | Text | Optional secondary headline displayed below the H1. | No |
| Hero Image | DAM Asset | 16:9 image for article header and social share preview. | Yes |
| Hero Image Alt Text | Text | Descriptive alt text. Required for accessibility compliance. | Yes |
| Author | Reference | Reference to Author Profile component. | Yes |
| Publish Date | Date | Original publication date. Displayed on byline. | Yes |
| Last Updated Date | Date | Date of most recent editorial update. Displayed if differs from publish date. | No |
| Estimated Read Time | Number | Minutes. Auto-calculated from word count or manually set. | Yes |
| Primary Topic | Taxonomy | Single primary category (e.g., Home Buying, Saving, Auto). | Yes |
| Secondary Tags | Taxonomy (multi) | Additional topic tags for related content matching. | No |
| Product Affiliation | Taxonomy | Product line associated with article (e.g., Mortgage, HYSA). | No |
| Body Content | Rich Text | Full article body. Supports H2–H4, lists, callout blocks, images. | Yes |
| Meta Title | Text | Overrides headline for `<title>` tag. Max 60 characters. | No |
| Meta Description | Text | SEO meta description. Max 155 characters. | Yes |
| Canonical URL | URL | Canonical override. Defaults to page URL if blank. | No |
| Product CTA Headline | Text | Headline for end-of-article product callout module. | No |
| Product CTA Body | Text | Short descriptive copy for product callout. | No |
| Product CTA Link | URL | Target URL for product callout CTA button. | No |
| Related Articles Override | Reference (multi) | Manual override for related article selections. Max 4. | No |

---

## 9. Team & Governance

The Content Hub MVP follows the standard AEM Design + Build process, with a dedicated squad model.

| Role | Responsibilities |
|---|---|
| Digital Product Owner (PO) | Owns backlog, EPICs/Stories in JIRA, requirements gathering, sprint planning, stakeholder communication |
| Marketing Owner | Business partner; provides content strategy direction, final BV sign-off, approves design concepts |
| Design Agency | UX/design concept, experience brief, wireframes, design system components |
| AEM Tech Lead | Component architecture, sprint scoping, AEM platform decisions |
| AEM Author Lead | Content migration, authoring workflow, AEM authoring standards |
| UX Designer | Design/tech reviews, component design handoff, interaction specs |
| AEM Test | Component QA, accessibility validation, regression testing |
| SEO | Metadata requirements, URL structure, structured data, sitemap |
| Tagging | Adobe Analytics tagging spec, QA validation |
| Scrum Master | Sprint ceremonies, impediment removal, velocity tracking |

---

## 10. Dependencies & Risks

### 10.1 Dependencies

- AEM platform version compatibility confirmed before component development begins
- WordPress content export available and in agreed format before migration sprint
- Taxonomy finalized and signed off before content migration begins — retroactive remapping is high-cost
- Design system components approved by legal and compliance before build begins
- Adobe Analytics tagging spec completed and reviewed before Author/Test/Publish phase
- 301 redirect mapping completed and validated by SEO before go-live

### 10.2 Risks

| Risk | Likelihood | Impact | Mitigation | Status |
|---|---|---|---|---|
| WordPress content doesn't map cleanly to AEM content model | Medium | Medium | Conduct content audit and taxonomy mapping before migration sprint; budget for manual cleanup | Anticipated |
| SEO authority loss during URL migration | Medium | High | Implement 301 redirects pre-launch; monitor GSC for coverage errors post-launch | Anticipated |
| Accessibility defects blocking launch | Low–Medium | High | Involve accessibility team in component design reviews, not just final QA | Anticipated |
| Scope creep from stakeholder feature requests | High | Medium | Lock P0/P1 features at sprint kick-off; route new requests to post-MVP backlog | Anticipated |
| AEM component development delays | Medium | Medium | Front-load component mapping and requirements; identify critical path components early | Anticipated |
| Content migration volume underestimated | Medium | Medium | Audit WordPress content library before committing to migration timeline | Anticipated |
| UX resource gap and budget misalignment | High | High | **Realized.** Original project budget allocated capacity for a content author, not a UX designer — creating a structural mismatch when UX design work (reconciling agency-provided styles against the enterprise design system) could not begin. Gap escalated through product and UX leadership to executive level. Resolved by borrowing designer capacity from an adjacent team. Resulted in a multi-month delay before development could begin; Sprint Zero started late March 2022. | ⚠️ Realized |

---

## 11. Launch Readiness Checklist

All items below must be completed and signed off before production publish.

- [ ] All P0 components built, tested, and approved by all stakeholders
- [ ] Content migration complete with QA review sign-off from AEM Author Lead
- [ ] 301 redirects implemented and validated by SEO
- [ ] Adobe Analytics tagging validated by Tagging team
- [ ] WCAG 2.1 AA compliance validated by accessibility team
- [ ] SEO metadata, structured data, and sitemap reviewed and approved
- [ ] Core Web Vitals benchmarked — LCP, CLS, FID within targets
- [ ] Cross-browser and responsive QA completed (Chrome, Safari, Firefox, Edge; mobile and desktop)
- [ ] AEM authoring workflow tested end-to-end by AEM Author Lead
- [ ] Marketing Owner BV sign-off on final published pages
- [ ] Stakeholder demo completed and launch approved by Digital PO

---

## 12. Future Roadmap (Post-MVP)

The following capabilities are explicitly out of scope for MVP but represent a prioritized post-launch roadmap informed by the discovery phase.

#### Phase 2 — Engagement
- Email signup, subscription management, and automated content digest newsletter
- Content series and multi-part editorial journeys linking related articles
- Content performance dashboard with engagement metrics and conversion attribution by article
- Targeted content strategy informed by audience segmentation and topic affinity data
- Product page modules surfacing related hub articles inline on unauthenticated product pages

#### Phase 3 — Personalization
- Personalized content recommendations driven by browse behavior and product affiliation
- Topic preferences and sentiment reactions allowing users to shape their content feed

#### Phase 4 — Delight
- Visual stories and mobile-web optimized experiences designed for social referral traffic
- User authentication enabling deeper personalization tied to account relationship and life stage
- In-house tools and quizzes (calculators, assessments) embedded within editorial content

---

## Appendix

### A. Glossary

| Term | Definition |
|---|---|
| AEM | Adobe Experience Manager — the enterprise CMS platform used to build and manage the content hub |
| BV Sign-off | Business Value sign-off — final approval from the Marketing Owner confirming the delivered experience meets business requirements |
| CMS | Content Management System — software platform for creating, managing, and publishing digital content |
| Component Mapping | The process of identifying which AEM components are needed or require enhancement for a new feature |
| DAM | Digital Asset Management — AEM's repository for images, PDFs, and other media files |
| EPIC / Story | Agile work units in JIRA. EPICs are large bodies of work; Stories are individual deliverable tasks within an EPIC |
| Legal & Compliance | The approval body for design concepts and content before they go live |
| RTE | Rich Text Editor — the AEM authoring component used to input and format article body content |
| SWAG | Sized Wild-Ass Guess — informal effort estimate used during early sprint planning before full requirements are defined |
| WCAG 2.1 AA | Web Content Accessibility Guidelines, Level AA — the accessibility compliance standard required for all new digital experiences |

### B. Source Documents

- FinTech Consumer Content Hub — Experience Brief (Design Agency, 2021/2022)
- AEM Design + Build Process Overview v3 (Internal, February 2025)
- Stakeholder Discovery Interviews — Tom, Jessica, Chris, Sari, Tony, Jim
- Competitive & Comparative Analysis — Pinterest, Spotify, Airbnb, Netflix, NerdWallet, TikTok, Medium, Patagonia

### C. Assumptions

- AEM is the confirmed CMS platform for build — no platform evaluation in scope
- WordPress content library is fully owned by the company and cleared for migration
- The design agency deliverables serve as the UX source of truth for the MVP experience
- SEO authority (domain/URL) continuity is achievable via 301 redirect strategy
- A dedicated AEM squad will be staffed for this initiative prior to sprint start
