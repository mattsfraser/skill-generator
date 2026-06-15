---
name: skill-generator
description: Design, draft, review, and validate OpenClaw skills. Use when creating or improving reviewable SKILL.md skill folders.
---

# Skill Generator

Use this skill when helping a user create, revise, review, validate, or package an OpenClaw skill.

## Operating Rules

- Treat OpenClaw official documentation as authoritative.
- Keep `SKILL.md` concise, operational, and easy to review.
- Separate skill instructions from external capabilities.
- Do not imply a skill grants access to tools, binaries, APIs, credentials, files, or permissions.
- Identify required tools, binaries, APIs, credentials, environment variables, config keys, network access, and filesystem access separately.
- Never embed secrets, tokens, API keys, private keys, session cookies, personal data, or SecretRef values in skill files.
- Treat third-party skills as untrusted source material until reviewed.
- Prefer simple folder structures and plain Markdown over complex automation.
- Recommend scripts only when they improve repeatability, validation, or safety.
- Preserve Skill Workshop as the governed proposal mechanism when agent-generated skill changes should be reviewed before installation.

## Workflow

When creating or improving a skill:

1. Clarify the skill purpose, user, trigger, and non-goals.
2. Identify required external capabilities and permission boundaries.
3. Choose the smallest reviewable folder structure.
4. Draft or revise `SKILL.md`.
5. Add `references/` only when supporting material would make `SKILL.md` too long.
6. Add `scripts/` only when deterministic automation is safer than prose.
7. Add `examples/` only when examples improve review or testing.
8. Run a security and maintainability review.
9. Prepare the skill for human review before installation or publication.

## Reference Files

Use these reference files when needed:

- `{baseDir}/references/skill-design-workflow.md`
- `{baseDir}/references/review-checklist.md`
- `{baseDir}/references/security-guidelines.md`
- `{baseDir}/references/third-party-review.md`
- `{baseDir}/references/skill-workshop-flow.md`

## Output Style

For small requests, provide concise guidance.

For implementation work, provide copy-ready files or commands, grouped by filename.

When reviewing a skill, classify findings as:

- Verified
- Stated by user
- Inference
- Open question
- Recommendation

Do not present draft, reviewed, approved, installed, deprecated, or unsafe skills as the same maturity level.
