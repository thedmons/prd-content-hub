# PRD: FinTech Consumer Content Hub
### fintech.com/stories — MVP Launch

---

## Overview

This repository contains the Product Requirements Document for the MVP launch of a FinTech consumer content hub — a dedicated editorial destination migrated from a disconnected WordPress blog into Adobe Experience Manager (AEM), designed to deliver financial guidance, product education, and money-life content at scale.

This is the platform PRD for the content hub initiative. It established the content model, taxonomy, AEM component requirements, SEO and accessibility foundations, and a phased post-MVP roadmap through Engagement, Personalization, and Delight phases.

📄 **[Read the full PRD →](./prd-content-hub.md)**

---

## What This Demonstrates

**Platform-level product thinking** — This PRD defines the foundation that downstream features (including the [Visual Stories feature PRD](https://github.com/thedmons/prd-visual-stories)) are built on. It shows how I approach a platform initiative: establishing the content model, taxonomy, and component library as infrastructure that other teams and features depend on, not just a one-time migration deliverable.

**Taxonomy and content model design** — The PRD includes a full AEM content model and tag-based taxonomy structure that drives related content matching, category page queries, and analytics attribution. Taxonomy governance is treated as a launch dependency, not an afterthought.

**Phased roadmap with architectural intent** — The post-MVP roadmap is organized into four phases (MVP, Engagement, Personalization, Delight), each scoped to what can be built on the existing foundation vs. what requires new infrastructure. This framing was intentional — it gave engineering confidence that MVP decisions wouldn't need to be undone in later phases.

**Cross-functional scope management** — The PRD covers content migration, SEO continuity, WCAG 2.1 AA accessibility requirements, Adobe Analytics tagging, and a launch readiness checklist — reflecting the coordination surface area of a platform initiative that touches content, engineering, SEO, accessibility, tagging, and marketing simultaneously.

**Author experience as a first-class requirement** — The AEM content author is treated as a distinct persona with explicit success criteria. Authoring cycle time (from 5+ days on WordPress to 2 days in AEM) is a tracked success metric, not a side effect.

---

## Document Metadata

| | |
|---|---|
| **Product** | Consumer Content Hub (fintech.com/stories) |
| **Document Type** | Platform PRD |
| **Status** | Completed |
| **Date** | Q1 2022 |
| **Platform** | Adobe Experience Manager (AEM) |

---

## Related Artifacts

| Artifact | Description |
|---|---|
| [System Design: FinTech Consumer Content Hub](https://github.com/thedmons/system-design-content-hub) | AEM component architecture built from this PRD — component library, JCR taxonomy, authoring pipeline, caching strategy |
| [PRD: Visual Stories](https://github.com/thedmons/prd-visual-stories) | Feature PRD for the Phase 4 Delight feature built on this platform |
