# PRD: FinTech Consumer Content Hub
### fintech.com/stories — MVP Launch

---

## Overview

This repository contains the Product Requirements Document for the MVP launch of a FinTech consumer content hub — a dedicated editorial destination migrated from a disconnected WordPress blog into Adobe Experience Manager (AEM), designed to deliver financial guidance, product education, and money-life content at scale.

This is the platform PRD for the content hub initiative. It established the content model, taxonomy, AEM component requirements, SEO and accessibility foundations, and a phased post-MVP roadmap through Engagement, Personalization, and Delight phases.

📄 **[Read the full PRD →](./prd-content-hub.md)**

---

## Outcomes

| Metric | Result | Status |
|---|---|---|
| Annual sessions (FY23 — first full year post-migration) | 3.82M | ✅ Achieved |
| Article page sessions (FY23) | 2.61M | ✅ Achieved |
| YoY traffic growth during active migration (Q1 2023) | +18.35% | ✅ Achieved |
| Traffic retained through full platform cutover | Zero regression vs. WordPress baseline | ✅ Achieved |
| Avg time on page — desktop | 2:02 min | ✅ Achieved |
| Avg time on page — mobile | 1:49 min | ✅ Achieved |
| Authoring cycle time | 5+ days (WordPress) → 2 days (AEM) | ✅ Achieved |
| Content hub visits crossing into Deposit account funnels | 6% of sessions | ✅ Achieved |
| Natural search as dominant traffic channel | 69% of Q1 2025 sessions | ✅ Achieved |

*PRD initiated Q1 2022. Sprint Zero began late March 2022 following UX design reconciliation. Migration phased through May 2023 full cutover. FY23 reflects first complete annual measurement on new platform.*

---

## What This Demonstrates

**Platform-level product thinking** — This PRD defines the foundation that downstream features (including the Visual Stories feature PRD) are built on. It shows how I approach a platform initiative: establishing the content model, taxonomy, and component library as infrastructure that other teams and features depend on, not just a one-time migration deliverable.

**Taxonomy and content model design** — The PRD includes a full AEM content model and tag-based taxonomy structure that drives related content matching, category page queries, and analytics attribution. Taxonomy governance is treated as a launch dependency, not an afterthought.

**Phased roadmap with architectural intent** — The post-MVP roadmap is organized into four phases (MVP, Engagement, Personalization, Delight), each scoped to what can be built on the existing foundation vs. what requires new infrastructure. This framing was intentional — it gave engineering confidence that MVP decisions wouldn't need to be undone in later phases.

**Cross-functional scope management** — The PRD covers content migration, SEO continuity, WCAG 2.1 AA accessibility requirements, Adobe Analytics tagging, and a launch readiness checklist — reflecting the coordination surface area of a platform initiative that touches content, engineering, SEO, accessibility, tagging, and marketing simultaneously.

**Author experience as a first-class requirement** — The AEM content author is treated as a distinct persona with explicit success criteria. Authoring cycle time (from 5+ days on WordPress to 2 days in AEM) is a tracked success metric, not a side effect.

**Realized risk: UX resource gap and budget misalignment** — A multi-month delay occurred prior to Sprint Zero when UX design work — reconciling agency-provided styles against the enterprise design system — could not begin due to a resource gap. The original project budget had allocated capacity for a content author, not a UX designer, creating a structural mismatch between planned and required resourcing. The gap was escalated through product and UX leadership to the executive level and resolved by borrowing designer capacity from another team. Sprint Zero began late March 2022. This is documented in the PRD risks section as both an anticipated risk (UX resource contention) and a realized one — including the budget misalignment root cause and the cross-team resolution path.

---

## Document Metadata

| | |
|---|---|
| **Product** | Consumer Content Hub (fintech.com/stories) |
| **Document Type** | Platform PRD |
| **Status** | Completed |
| **PRD Initiated** | Q1 2022 |
| **Sprint Zero** | Late March 2022 |
| **Full Platform Cutover** | May 2023 |
| **Platform** | Adobe Experience Manager (AEM) |

---

## Related Artifacts

| Artifact | Description |
|---|---|
| [System Design: FinTech Consumer Content Hub](https://github.com/thedmons/system-design-content-hub) | AEM component architecture built from this PRD — component library, JCR taxonomy, authoring pipeline, caching strategy |
| [PRD: Visual Stories](https://github.com/thedmons/prd-visual-stories) | Feature PRD for the Phase 4 Delight feature built on this platform |
