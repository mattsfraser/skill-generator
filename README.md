# skill-generator

`skill-generator` is an OpenClaw-native skill-development aid for designing, drafting, reviewing, validating, and packaging reviewable OpenClaw skills.

The project helps users and agents move from a rough skill idea to a maintainable skill folder without confusing instructions with actual capabilities.

## Status

Draft / v0.1 scaffold.

This repository is not yet installed or tested as an active OpenClaw skill.

## Purpose

Use this project to help create OpenClaw skills that are:

- clear
- concise
- auditable
- maintainable
- safe for agent use
- easy to review before installation

## Non-Goals

This project does not:

- grant tool access
- install skills automatically
- bypass OpenClaw Skill Workshop
- modify active `SKILL.md` files without review
- store credentials, secrets, tokens, private keys, session cookies, or SecretRef values
- replace official OpenClaw documentation
- act as a ClawHub marketplace or publishing system

## Repository Structure

    skill-generator/
      SKILL.md
      README.md
      NOTICE.md
      LICENSE.txt
      .gitignore
      references/
        skill-design-workflow.md
        review-checklist.md
        security-guidelines.md
        third-party-review.md
        skill-workshop-flow.md
      examples/
        minimal-skill/
          SKILL.md
        skill-with-reference/
          SKILL.md
          references/
            usage.md

## Design Principles

### Separate instructions from capabilities

A skill can instruct an agent how to use available tools, files, APIs, binaries, and credentials. It does not create those capabilities by itself.

### Keep `SKILL.md` concise

The root `SKILL.md` should contain operational instructions the agent can follow. Longer explanations, examples, checklists, schemas, and policy notes belong in `references/`.

### Use scripts carefully

Scripts are appropriate when they improve repeatability, validation, formatting, packaging, or safety.

Scripts should not hide risky behavior, make unexpected network calls, write outside approved paths, or handle secrets casually.

### Treat third-party skills as untrusted

External skills should be reviewed before reuse. Review for prompt injection, unsafe commands, credential exposure, hidden behavior, dependency risk, broad permissions, and license/provenance issues.

## Workflow

1. Clarify the skill idea.
2. Define intended use cases and non-goals.
3. Identify external capabilities and permissions.
4. Choose a minimal folder structure.
5. Draft `SKILL.md`.
6. Add references, examples, or scripts only when useful.
7. Review security and maintainability.
8. Validate structure and metadata.
9. Prepare for human review before installation or publication.

## License

Apache License 2.0. See `LICENSE.txt`.

## Provenance

This project was informed by comparative review of public ClawHub skill-authoring examples, including `skill-creator` and `write-a-skill`.

No upstream files are copied into this repository unless explicitly documented in `NOTICE.md`.
