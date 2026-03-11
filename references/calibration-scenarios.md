# Calibration Scenarios

These scenarios are fixtures for routing, prioritization, and follow-up behavior.

## Scenario 1: Ambiguous Full-Stack (`full-review`)

- Input: Resume says `Full Stack Engineer`, but all bullets are React and CSS. User targets backend roles.
- Expected: Route to `swe-infra`, flag positioning as a must-fix, and explain that current evidence reads frontend-first.

## Scenario 2: New Grad Coursework Soup (`full-review`)

- Input: New grad resume with 15 courses, a 3.1 GPA, and one CRUD project.
- Expected: Route to `swe-infra`, treat clutter as should-fix, and recommend replacing course lists with deeper project detail.

## Scenario 3: MLOps Infra Builder (`jd-tailor`)

- Input: Resume centers on Kubernetes clusters for GPU workloads. JD is for an ML engineer focused on training models.
- Expected: Route to `ml-eng`, mark model-training evidence as a gap, and tailor only where the resume can credibly support the JD.

## Scenario 4: Three-Page Senior (`layout-review`)

- Input: 15-year senior engineer with a 3-page PDF, 5-line bullets, and dense paragraphs.
- Expected: Use [layout-ats.md](layout-ats.md), mark density and bullet length as critical, and recommend a tighter 2-page structure.

## Scenario 5: Impact-Free Bullet (`bullet-rewrite`)

- Input: `Responsible for managing the database migrations and writing new API endpoints.`
- Expected: Explain what is missing, then produce 2-3 rewrites that move from acceptable specificity to stronger impact while keeping placeholders for missing proof.

## Scenario 6: Missing Context (`full-review`)

- Input: User pastes raw resume text with no target role, level, or JD.
- Expected: Infer the closest branch, state assumptions, add **[Provisional Review: Assumed {Role} at {Level}]**, and proceed.

## Scenario 7: Career Switcher (`resume-rebuild`)

- Input: Former teacher targeting junior SWE roles with one bootcamp project and one internship.
- Expected: Keep a short summary only if it frames the transition, move relevant projects up, and avoid treating prior teaching work as engineering experience.

## Scenario 8: Overqualified Candidate Down-Leveling (`jd-tailor`)

- Input: Staff engineer targeting senior roles for work-life balance.
- Expected: Treat over-level signaling as a must-fix, downplay org-wide strategy bullets that create mismatch, and keep technical depth without reading as staff-plus.

## Scenario 9: Employment Gap (`full-review`)

- Input: Strong backend resume with an 18-month gap and no explanation.
- Expected: Flag only if the gap materially affects risk perception, suggest a brief neutral explanation if appropriate, and avoid over-weighting it above weak role evidence.

## Scenario 10: Non-US Resume Format (`layout-review`)

- Input: Two-page EU-style CV with photo, full address, and long personal statement.
- Expected: Separate regional convention from ATS risk, explain which items are common locally, and recommend US-targeted edits only if the user is applying in the US.

## Scenario 11: Already-Strong Resume (`full-review`)

- Input: Senior engineer resume with clear positioning, concise impact bullets, appropriate scope evidence, and clean formatting.
- Expected: Acknowledge what is working, limit feedback to minor polish (word choice, ordering tweaks, optional additions). Do not manufacture problems or over-critique a resume that is already effective. A short review is the correct output for a strong resume.

## Scenario 12: User Disagrees with the Review (`follow-up`)

- Input: User insists a summary or multi-column layout should stay.
- Expected: Explain the recruiter or ATS tradeoff once, keep the conversation in the same mode, and offer the least-risk alternative instead of restarting the review. Never override the user's final decision — if they insist after hearing the tradeoff, defer and move on.
