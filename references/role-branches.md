# Role Branches

Load only the section that matches the target role unless the user clearly targets multiple families.

## Contents

- `Shared Standard`
- `Level Calibration`
- `swe-infra`
- `frontend`
- `data`
- `ml-eng`
- `devops-sre`
- `technical-pm`

## Shared Standard

- Good bullets usually show action, scope, and why the work mattered.
- `Acceptable` means specific and honest without invented metrics.
- `Stronger` means the same bullet plus defensible scale, outcomes, or cross-team effect.
- Use placeholders such as `[X%]`, `[X users]`, or `[timeframe]` when the resume lacks evidence.

## Level Calibration

Use these benchmarks when assessing whether bullet evidence matches the claimed or targeted level. These apply across all branches.

- **Junior / New Grad**: Executes well-scoped tasks within an existing system. Evidence shows learning speed, code quality, and completing assigned work. Ownership is at the feature or bug-fix level. Cross-team work is not expected.
- **Mid-level**: Owns features or small systems end-to-end with limited guidance. Evidence shows independent delivery, technical judgment on implementation tradeoffs, and some mentoring or onboarding. Scope is typically one team or service.
- **Senior**: Drives design and delivery of significant components or projects. Evidence shows technical leadership, cross-team influence, setting technical direction for a domain, and raising the bar for others. Scope spans multiple services or a meaningful product surface.
- **Staff+**: Shapes technical strategy across teams or org-wide. Evidence shows ambiguous problem framing, multi-quarter impact, architectural decisions with lasting effect, and growing other senior engineers. Scope is org-level or company-level.

When bullet evidence is 1+ level below the target, flag it as a scope mismatch. When it reads 1+ level above, flag it as over-level signaling (see calibration scenario 8).

## `swe-infra`

Route here for backend, full-stack, platform, distributed systems, mobile, and infrastructure-leaning IC resumes.

- What good looks like: systems owned, complexity handled, end-to-end delivery, technical judgment, level-appropriate scope
- Hiring-manager lens: can this person ship production software, explain tradeoffs, and handle ambiguous business-critical work
- Resume guidance: group skills by relevance; keep projects only if they add depth, prove a pivot, or matter for early-career candidates
- Red flags: tool-list bullets, ticket-shaped work, senior titles with task-level evidence, distributed-systems claims without design or ops details

Rewrite patterns:

- Weak: `Worked on backend APIs`
- Acceptable: `Built backend APIs for subscription billing and partner integrations, improving coverage of core checkout workflows`
- Stronger: `Built and operated 6 backend APIs for subscription billing, improving checkout success and reducing support escalations`

- Weak: `Improved performance`
- Acceptable: `Profiled slow request paths and reduced latency in the core request pipeline for peak traffic`
- Stronger: `Profiled hot paths in the request pipeline, cut p95 latency from 480 ms to 210 ms, and reduced timeout-related failures during peak traffic`

- Weak: `Collaborated with cross-functional teams on microservices`
- Acceptable: `Led the design of an order-processing service with product and payments teams, owning the API contract and rollout plan`
- Stronger: `Led the design and rollout of an order-processing service handling [X orders/day], coordinating API contracts with payments and product teams and reducing order failures by [X%]`

- Weak: `Responsible for database migrations and writing API endpoints`
- Acceptable: `Designed and executed schema migrations for the billing database and built API endpoints that supported the new pricing model`
- Stronger: `Designed zero-downtime schema migrations for the billing database serving [X] customers and built pricing API endpoints that enabled the launch of a new plan tier`

## `frontend`

Route here for frontend, UI engineering, design systems, and web performance roles.

- What good looks like: component architecture, performance, accessibility, cross-browser quality, design collaboration, frontend DX
- Hiring-manager lens: can this person build polished, performant, accessible interfaces and make sound UI architecture choices
- Resume guidance: keep projects only if they show visible craft, live demos, complex interactions, or open-source frontend work
- Red flags: backend-heavy resume with React mentioned once, no a11y or performance evidence, broken portfolio links, senior titles without architecture or mentoring

Rewrite patterns:

- Weak: `Built frontend components in React`
- Acceptable: `Built reusable React and TypeScript components for shared product flows and reduced UI inconsistency across screens`
- Stronger: `Architected a shared component library in React and TypeScript used by 5 product teams, reducing UI inconsistencies and cutting new feature development time by 30%`

- Weak: `Improved website performance`
- Acceptable: `Optimized the critical rendering path and deferred non-essential modules to improve page-load performance`
- Stronger: `Optimized critical rendering path and lazy-loaded below-fold modules, improving Largest Contentful Paint from 4.2s to 1.1s and lifting mobile conversion rate by 12%`

- Weak: `Collaborated with designers on UI updates`
- Acceptable: `Partnered with design to rebuild the onboarding flow, implementing new interaction patterns and reducing form abandonment`
- Stronger: `Partnered with design to rebuild the onboarding flow across web and mobile web, reducing form abandonment by [X%] and improving new-user activation within the first session`

## `data`

Route here for data engineering, analytics engineering, BI-heavy technical roles, and warehouse-centric work.

- What good looks like: pipeline reliability, model quality, scale, freshness, trust, governance, business enablement
- Hiring-manager lens: can this person build data systems stakeholders trust and connect technical work to usable data products
- Resume guidance: separate languages, processing, warehouse, and governance tools; keep projects only when they show real data-system depth
- Red flags: dashboard-heavy resume without data engineering depth, ML claims without deployment or use, unsupported tool lists, vague warehouse claims

Rewrite patterns:

- Weak: `Built data pipeline for analytics`
- Acceptable: `Built Airflow and Spark pipelines that prepared recurring analytics datasets for downstream reporting and stakeholder use`
- Stronger: `Built an Airflow and Spark pipeline processing 120M daily events, reducing data freshness from 6 hours to 20 minutes for growth analytics`

- Weak: `Created dashboards for stakeholders`
- Acceptable: `Modeled acquisition and retention tables in dbt and published dashboards that replaced manual reporting for business teams`
- Stronger: `Modeled core acquisition and retention tables in dbt and published executive dashboards that replaced manual weekly reporting across three business teams`

- Weak: `Responsible for data quality`
- Acceptable: `Built data validation checks across ingestion pipelines and established alerting for schema drift and freshness SLA breaches`
- Stronger: `Built automated data validation across [X] ingestion pipelines, catching schema drift and freshness violations before downstream consumers, reducing data incident tickets by [X%]`

## `ml-eng`

Route here for ML engineering, applied AI, model serving, ML platform, and MLOps with a model-lifecycle center of gravity.

- What good looks like: training through deployment, inference optimization, ML platform ownership, reproducibility, monitoring, cross-functional delivery
- Hiring-manager lens: can this person take models to production and make good quality, latency, and cost tradeoffs
- Resume guidance: keep projects only if they show deployed models, real adoption, meaningful open source, or top-tier competition outcomes
- Red flags: notebook-only work, accuracy claims without impact, long algorithm lists, no monitoring or lifecycle detail, senior titles without platform or cross-team scope

Rewrite patterns:

- Weak: `Trained a machine learning model for recommendations`
- Acceptable: `Built and deployed a recommendation model that replaced a rules-based approach for a user-facing workflow`
- Stronger: `Built and deployed a real-time recommendation model serving 50M daily requests, improving click-through rate by 18% over the rule-based baseline while maintaining p99 latency under 30ms`

- Weak: `Improved model performance`
- Acceptable: `Reduced inference cost by shrinking model size and improving serving efficiency for production traffic`
- Stronger: `Reduced inference cost by 60% by distilling a 7B-parameter model to 1.3B parameters with <2% quality regression, enabling on-device deployment for the mobile app`

- Weak: `Collaborated with data scientists on feature engineering`
- Acceptable: `Built and maintained the feature store used by data scientists for training and serving, standardizing feature computation across online and offline paths`
- Stronger: `Built a feature store serving [X] features across online and batch paths, reducing feature skew incidents and cutting new model onboarding time from [X days] to [X hours]`

## `devops-sre`

Route here for SRE, production engineering, platform engineering, cloud infrastructure, and reliability-first roles.

- What good looks like: reliability, automation, incident response, safe infrastructure design, platform leverage for other teams
- Hiring-manager lens: would I trust this person with production, operational tradeoffs, and reducing risk while increasing delivery speed
- Resume guidance: group skills by cloud, containers, IaC, CI/CD, and observability; prefer outcomes tied to MTTR, paging, release safety, provisioning, or SLOs
- Red flags: tool-heavy resume with no production outcomes, generic AWS bullets, no observability or incident detail, certifications without hands-on evidence

Rewrite patterns:

- Weak: `Managed Kubernetes cluster`
- Acceptable: `Operated Kubernetes clusters for shared services and standardized deployment practices across environments`
- Stronger: `Operated and standardized multi-tenant Kubernetes clusters for 40+ services, cutting environment drift and reducing failed deployments during weekly releases`

- Weak: `Improved monitoring`
- Acceptable: `Defined service dashboards and alerting for critical APIs to improve visibility into production regressions`
- Stronger: `Defined service-level alerts and dashboards for critical APIs, reducing mean time to detect production regressions and eliminating noisy pages from legacy thresholds`

- Weak: `Responsible for CI/CD pipelines`
- Acceptable: `Owned and maintained CI/CD pipelines for [X] services, standardizing build and deploy steps across teams`
- Stronger: `Redesigned CI/CD pipelines for [X] services, cutting average deploy time from [X min] to [X min] and reducing rollback incidents by enforcing canary stages`

## `technical-pm`

Route here for PM resumes where technical fluency materially affects hiring.

- What good looks like: product judgment under technical constraints, roadmap ownership, engineering partnership, platform or developer-tool leverage, measurable outcomes
- Hiring-manager lens: can this person lead technical products without pretending to be the engineering lead and still make sound system-level tradeoffs
- Resume guidance: keep the skills section modest; emphasize problem framing, technical scope, cross-functional leadership, and adoption or business results
- Red flags: project-manager framing, technical claims without decisions, launch bullets without adoption, keyword-dumped engineer tools, every bullet starting with collaboration

Rewrite patterns:

- Weak: `Worked with engineers to build API features`
- Acceptable: `Defined requirements and rollout priorities for partner API features with engineering and GTM stakeholders`
- Stronger: `Defined the roadmap for partner APIs used by enterprise integrations, aligning engineering and GTM teams to launch self-serve capabilities that reduced onboarding time for new partners`

- Weak: `Owned product backlog`
- Acceptable: `Prioritized platform backlog across reliability, usability, and partner requests to improve delivery focus`
- Stronger: `Prioritized platform backlog across reliability, usability, and partner requests, improving delivery focus and increasing adoption of the developer console among high-value accounts`

- Weak: `Collaborated with engineering and design on new features`
- Acceptable: `Defined requirements and success criteria for the self-serve onboarding flow, aligning engineering and design on scope and phased rollout`
- Stronger: `Defined requirements and phased rollout for self-serve onboarding, aligning engineering and design to ship in [X weeks] and increasing trial-to-paid conversion by [X%]`
