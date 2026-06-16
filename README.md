# Skill Generator

Build safer OpenClaw skills from rough idea to reviewable folder.

`skill-generator` is an OpenClaw-native skill-development aid for designing, drafting, reviewing, and validating `SKILL.md`-based agent skills.

It helps OpenClaw users turn a loose skill concept into a clear, maintainable, auditable skill folder that can be reviewed before installation.

## Why this exists

OpenClaw skills are powerful because they let users teach agents repeatable behaviors through plain Markdown instructions.

But without a clear design process, a skill can become:

* too vague to use reliably
* too broad to review safely
* unclear about required tools or permissions
* overloaded with long instructions
* risky because secrets, shell commands, or third-party assumptions are not reviewed carefully

Skill Generator helps solve that problem by guiding the skill author through a structured, security-conscious workflow.

## What it helps you create

A reviewable OpenClaw skill folder such as:

```text
my-skill/
  SKILL.md
  references/
    usage.md
    security-notes.md
  examples/
    input.json
    output.json
```

The goal is not to make skills more complicated. The goal is to make them easier to understand, test, review, and maintain.

## How it works

Skill Generator guides the author through five practical steps:

1. **Clarify the idea**
   Define what the skill should do, when it should be used, and when it should not be used.

2. **Design the folder**
   Choose the smallest useful structure for the skill.

3. **Draft `SKILL.md`**
   Keep the main skill instructions concise, operational, and easy for an agent to follow.

4. **Add support files only when useful**
   Move longer examples, schemas, checklists, or notes into `references/`, `examples/`, or scripts when they improve reviewability.

5. **Review before installation**
   Check metadata, dependencies, permissions, security risks, examples, and failure behavior before treating the skill as ready.

## What is included

This repository includes:

```text
skill-generator/
  SKILL.md
  README.md
  NOTICE.md
  LICENSE.txt
  references/
    skill-design-workflow.md
    review-checklist.md
    security-guidelines.md
    third-party-review.md
    skill-workshop-flow.md
  examples/
    minimal-skill/
      SKILL.md
    third-party-api-skill/
      SKILL.md
      references/
        source-packets.md
    skill-with-reference/
      SKILL.md
      references/
        usage.md
```

## Use cases

Use Skill Generator when you want to:

* design a new OpenClaw skill
* rewrite a rough skill idea into a reviewable folder
* improve an existing `SKILL.md`
* separate concise instructions from longer reference material
* review a third-party skill before adapting it
* model external API requirements without embedding credentials or tool access
* prepare a skill for human review before installation

## Safety model

A skill is instruction, not capability.

Skill Generator does not grant tool access, credentials, filesystem permissions, network access, or API access. Any required capability must exist separately in the user’s OpenClaw environment.

This project is designed to help authors avoid common skill risks, including:

* unclear scope
* hidden assumptions
* overbroad permissions
* unreviewed third-party code
* unsafe shell commands
* embedded secrets or credentials
* confusing generated drafts with approved installed skills

## What this is not

Skill Generator does not:

* install skills automatically
* bypass OpenClaw Skill Workshop
* replace official OpenClaw documentation
* act as a ClawHub marketplace or publishing system
* make unreviewed third-party skills safe by default
* modify active skills without review

## Project status

This repository is currently a v0.1 scaffold.

It has been drafted, committed, pushed publicly, and reviewed for baseline structure and safety. It has not yet been installed or runtime-tested as an active OpenClaw skill.

Treat it as reviewable source material until installation and testing are completed deliberately.

## License

Apache License 2.0. See `LICENSE.txt`.

## Provenance

This project was informed by comparative review of public ClawHub skill-authoring examples, including `skill-creator` and `write-a-skill`.

No upstream files are copied into this repository unless explicitly documented in `NOTICE.md`.
