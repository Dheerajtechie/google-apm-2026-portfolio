# PRD: AI-Powered User Insights Platform

## 1. Overview

### 1.1 Goal
Enable PM and research teams to identify, prioritize, and act on user pain points from multi-source feedback with high confidence.

### 1.2 North-star metric
**Insight-to-action rate** = percentage of surfaced insights that become a concrete team action (experiment, design change, roadmap item) within 30 days.

### 1.3 Success metrics
- Median time from data ingest to insight review
- Insight acceptance rate by PMs
- Action conversion rate
- 30-day retained active workspaces

## 2. Users & JTBD

### Primary user: Product Manager
**JTBD:** When planning roadmap priorities, help me quickly understand the highest-impact user problems so I can make confident tradeoff decisions.

### Secondary user: UX Researcher
**JTBD:** When synthesizing large qualitative datasets, help me produce credible themes and evidence quickly without losing nuance.

## 3. Scope

### In scope (MVP)
- Data ingestion connectors: CSV uploads, Intercom exports, app reviews
- AI clustering and theme generation
- Evidence-backed insight cards with confidence scoring
- Opportunity prioritization (impact × reach × confidence)
- Collaboration: comments, status, and owner assignment

### Out of scope (MVP)
- Real-time streaming ingestion
- Fully automated roadmap writing
- Multilingual semantic clustering beyond English

## 4. Functional requirements
1. User can upload/import feedback datasets with basic schema mapping.
2. System generates themes with representative quotes and source links.
3. Each insight card shows confidence score + rationale.
4. User can convert insight into an action item.
5. Dashboard tracks insight-to-action funnel.

## 5. Non-functional requirements
- P95 insight generation latency < 90s for 10k records
- 99.5% monthly availability
- Audit log for key user actions
- Role-based access controls for workspace members

## 6. Risks & mitigations
- **Hallucinated synthesis:** Require source citation display and confidence gating.
- **User trust:** Enable manual override/edit and feedback loop on model outputs.
- **Privacy concerns:** PII redaction pipeline and configurable data retention.

## 7. Launch plan

### Phase 1 (Alpha)
- 5 design partners
- Weekly calibration on output quality and trust

### Phase 2 (Beta)
- Self-serve onboarding for SMB segment
- Expand connectors and dashboard depth

### Phase 3 (GA)
- Enterprise controls, SLAs, and procurement readiness
