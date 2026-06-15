# Skill Workshop Flow

Use this reference when a skill change should go through OpenClaw Skill Workshop before installation.

## 1. Purpose

Skill Workshop is the governed proposal path for agent-drafted skill changes.

Use it when a user wants an agent to help propose, revise, or review skill files before those files are installed or activated.

## 2. Preserve the Boundary

`skill-generator` may help draft or review skill content.

It should not bypass review, install skills automatically, or modify active OpenClaw skill roots without explicit approval.

## 3. When to Use Skill Workshop

Use Skill Workshop when:

- creating a new skill for installation
- revising an existing installed skill
- adding scripts to a skill
- changing security-relevant instructions
- changing tool or permission assumptions
- adapting third-party skill material
- preparing a skill for team or public use
- uncertainty exists about safety or scope

## 4. Proposal Contents

A skill proposal should include:

- skill name
- purpose
- intended user
- trigger conditions
- non-goals
- proposed folder structure
- proposed `SKILL.md`
- supporting reference files
- scripts, if any
- required external capabilities
- security considerations
- third-party provenance
- testing or validation notes
- open questions

## 5. Review Before Apply

Before a proposed skill change is applied, review:

- whether the skill is necessary
- whether `SKILL.md` is concise
- whether references are justified
- whether scripts are justified
- whether secrets are absent
- whether third-party provenance is documented
- whether permission boundaries are clear
- whether installation risk is acceptable

## 6. Apply Only After Approval

Do not treat a generated proposal as installed.

A skill remains draft until a user or authorized reviewer approves installation or update.

## 7. Maturity Labels

Use these maturity labels:

- draft: created but not reviewed
- reviewed: inspected but not approved
- approved: accepted for installation or publication
- installed: active in the OpenClaw environment
- deprecated: no longer recommended
- unsafe: should not be installed or used

## 8. Safe Default

When uncertain, keep the skill in draft form and ask for review.
