# tech-resume-optimizer

A custom agent skill that reviews, critiques, and improves technical resumes — optimized for ATS compatibility, recruiter readability, and role-specific impact. Works with [Claude Code](https://docs.anthropic.com/en/docs/claude-code), [Codex](https://github.com/openai/codex), and other AI coding agents.

## What It Does

This skill acts as a technical hiring-manager lens for your resume. It evaluates positioning, bullet quality, scope credibility, layout, and concision — then gives you specific, actionable edits tied to your actual resume text.

### Supported Roles

- **SWE / Infrastructure** — backend, full-stack, platform, distributed systems, mobile
- **Frontend** — UI engineering, design systems, web performance
- **Data** — data engineering, analytics engineering, BI, warehouse
- **ML Engineering** — applied AI, model serving, ML platform, MLOps
- **DevOps / SRE** — reliability, cloud infrastructure, platform engineering
- **Technical PM** — developer tools, platform products, API products

### Modes

| Mode | What you get |
|---|---|
| `full-review` | Targeting assessment, strengths, must-fix changes, modification map, missing proof |
| `jd-tailor` | Requirement matching against a specific job description, modification map, gap analysis |
| `bullet-rewrite` | Critique of individual bullets with 2-3 rewritten options |
| `layout-review` | ATS compatibility and visual scanability audit |
| `resume-rebuild` | Section-by-section improvement map or full markdown rewrite |

## Installation

### Claude Code

Add as a custom skill:

```bash
git clone https://github.com/<your-username>/tech-resume-optimizer.git

# Symlink
ln -s /path/to/tech-resume-optimizer ~/.claude/skills/tech-resume-optimizer

# Or copy
cp -r /path/to/tech-resume-optimizer ~/.claude/skills/tech-resume-optimizer
```

Once installed, the skill is available as `/tech-resume-optimizer`.

### Other Agents

Point your agent to `SKILL.md` as a system prompt or instruction file. The skill is self-contained — `SKILL.md` references the files in `references/` for role-specific guidance, layout checks, and edge-case calibration.

## Usage

In a Claude Code session:

```
# Full review (default) — paste or attach your resume
/tech-resume-optimizer

# Tailor to a job description
/tech-resume-optimizer Here's my resume [paste] and the JD: [paste or URL]

# Rewrite specific bullets
/tech-resume-optimizer bullet-rewrite: "Responsible for managing database migrations and writing new API endpoints"

# Layout and ATS audit on a PDF
/tech-resume-optimizer layout-review [attach PDF]
```

The skill can read PDFs, images, and plain text. If you provide a JD URL, it will fetch and parse it automatically.

## Key Principles

- **Never invents content.** Metrics, tools, titles, and outcomes are never fabricated. Missing evidence gets placeholders like `[X%]` or `[X users]`.
- **Specific, not generic.** Every recommendation ties to exact resume text or visible layout issues.
- **Level-calibrated.** Feedback is calibrated to your target level (junior through staff+) with explicit scope-mismatch flags.
- **ATS-aware.** Checks for parsing risks: tables, columns, non-standard headings, image-based content, header/footer placement.

## Project Structure

```
├── SKILL.md                          # Skill definition and workflow
├── references/
│   ├── role-branches.md              # Role-specific guidance, red flags, rewrite patterns
│   ├── layout-ats.md                 # Layout rubric and ATS compatibility checklist
│   └── calibration-scenarios.md      # Edge-case routing and behavior calibration
├── LICENSE                           # MIT
└── README.md
```

## License

MIT
