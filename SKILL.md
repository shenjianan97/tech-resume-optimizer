---
name: tech-resume-optimizer
description: Review, critique, and improve resumes for technical hiring. Use for software engineering, frontend, data, ML, DevOps/SRE, or technical PM resumes; ATS and recruiter-focused edits; bullet rewrites; and tailoring to technical job descriptions.
---

# Tech Resume Optimizer

Use this skill to review or improve a technical resume with a hiring-manager lens. Optimize for role fit, fast scanability, honest impact, and ATS-safe formatting.

## Workflow

1. Require resume text or a readable file (use the Read tool for PDFs and image files to inspect the resume visually). If missing, stop and ask. Helpful extras: target role, level, JD, years of experience, geography, and company type. If the user provides a JD URL, use WebFetch to retrieve it; use WebSearch only when the user asks to research a company or role and no direct URL is available.
2. Pick one mode: `full-review` (default when unspecified), `jd-tailor`, `bullet-rewrite`, `layout-review`, or `resume-rebuild`.
3. If the mode uses role-specific guidance (`full-review`, `jd-tailor`, `resume-rebuild`), pick a branch from [references/role-branches.md](references/role-branches.md): `swe-infra`, `frontend`, `data`, `ml-eng`, `devops-sre`, or `technical-pm`. For `bullet-rewrite`, load the branch only if the target role is known. For `layout-review`, skip branch selection entirely.
4. Load reference material: always load `Shared Standard` and `Level Calibration` from [references/role-branches.md](references/role-branches.md), plus the selected branch section if applicable. Load [references/layout-ats.md](references/layout-ats.md) when layout or ATS matters. Load [references/calibration-scenarios.md](references/calibration-scenarios.md) when behavior is ambiguous: missing context, career switch, down-leveling, employment gaps, non-US formats, already-strong resumes, or follow-up disagreement. Review in severity order.

Tie-breaks:

| Ambiguous signal | Route to |
|---|---|
| Mobile | `swe-infra` |
| Analytics engineering | `data` |
| ML platform / MLOps | `ml-eng` (unless clearly infra-first, then `devops-sre`) |
| Hybrid backend/SRE | `devops-sre` (default when unclear) |
| Security / crypto engineering | `swe-infra` if AppSec or product-security; `devops-sre` if infra-security or cloud-security |

For out-of-scope roles, choose the closest branch and label the review as best-effort.

If the user targets multiple role families, load only the relevant branch subsections, call out overlapping vs conflicting signals, and recommend one version or split versions when needed.

## Non-Negotiables

- Never invent metrics, tools, titles, ownership, or outcomes. Use placeholders like `[X%]`, `[X users]`, or `[timeframe]` when evidence is missing.
- Tie every recommendation to exact resume text or visible layout, not generic advice.
- If role or level is missing, label the response exactly as **[Provisional Review: Assumed {Role} at {Level}]**.
- On follow-ups, stay in the same mode unless the user clearly changes intent. Do not re-review unchanged sections.

## Review Standard

Prioritize findings in this order:

1. Positioning and relevance: the target role should be obvious quickly, and the strongest evidence should appear early.
2. Bullet quality: bullets should be concise accomplishment statements with an action verb, context or tech, and a result or business impact when supported.
3. Scope and credibility: claims should match the targeted level and survive interview scrutiny.
4. Layout and ATS: prefer reverse-chronological structure, standard headings, single-column layout, and no tables, graphics, icons, or headers/footers for critical content.
5. Concision: cut filler summaries, stale coursework, weak projects, and unsupported skill dumps before trimming strong experience.

Default resume standards:

- One page is the default for students, early-career candidates, and most non-academic roles; use two pages only when experience clearly justifies it.
- Keep bullets readable and usually 1-2 lines. Prefer about 2-4 bullets for recent roles and fewer for older roles.
- Group skills by category and keep only tools relevant to the target role.
- Use consistent dates and clean links. PDF should come from a text source and pass a plain-text copy test.

Use [references/layout-ats.md](references/layout-ats.md) whenever layout or parsing risk matters.

## Modes

Shared output definitions used across modes:

- **Modification map**: a prioritized list of specific edits tied to exact bullets or sections — what to change, the suggested rewrite or direction, and why.
- **Missing proof**: claims in the resume that lack supporting evidence (unsupported metrics, vague ownership, unverified scale) and gaps relative to the target role that the resume doesn't address at all.

Mode details:

- `full-review`: output `Targeting assessment`, `What's working`, `Top must-fix changes`, `Modification map`, and `Missing proof`. Add `Layout / ATS` when a PDF or image is provided. If the resume is already strong, keep the review short and focus on minor polish rather than manufacturing issues.
- `jd-tailor`: output `Requirement matching`, `Modification map`, and `Missing proof`. Focus on the highest-value JD gaps only. For down-leveling or adjacent-role transitions, tailor only where the resume can credibly support the target.
- `bullet-rewrite`: output `Original bullet`, `Critique`, and 2-3 `Rewritten options`. Keep placeholders for unsupported metrics.
- `layout-review`: apply [references/layout-ats.md](references/layout-ats.md) and group findings by severity.
- `resume-rebuild`: ask the user whether they want an **improvement map** (default — section-by-section change map with reasoning and remaining information gaps) or a **full rewrite** (complete markdown resume plus a note on structural changes and information gaps). If the user's intent is already clear, skip the question and proceed. When producing a full rewrite, preserve all original claims verbatim and only restructure, reword, or cut — never add content the original resume did not contain.

## Rebuild Defaults

- Section order by default: `Header`, optional `Summary`, `Skills`, `Experience`, optional `Projects`, `Education`.
- Move `Education` near the top for students and new grads; keep it near the bottom once experience carries the story.
- Keep a summary only when it sharpens positioning; remove it when it adds filler.
- For edge cases, routing checks, already-strong resumes, and follow-up disagreements, use [references/calibration-scenarios.md](references/calibration-scenarios.md).

## References

- [references/role-branches.md](references/role-branches.md) for role-specific guidance, red flags, and rewrite patterns
- [references/layout-ats.md](references/layout-ats.md) for layout and ATS checks
- [references/calibration-scenarios.md](references/calibration-scenarios.md) for routing and edge-case calibration
