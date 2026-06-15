# Skill Design Workflow

Use this workflow when designing or revising an OpenClaw skill.

## 1. Clarify the Skill

Identify:

- skill name
- intended user
- primary task
- trigger conditions
- non-goals
- expected outputs
- review requirements

A skill should have a narrow purpose. Avoid broad assistant-personality bundles.

## 2. Separate Instructions from Capabilities

Document what the skill tells the agent to do.

Document separately what must already exist outside the skill:

- tools
- binaries
- APIs
- credentials
- files
- permissions
- environment variables
- network access
- filesystem access
- user approvals

Do not imply the skill creates access by itself.

## 3. Choose the Smallest Structure

Start with:

    skill-name/
      SKILL.md

Add folders only when needed:

    references/   longer guidance, schemas, checklists, examples
    scripts/      deterministic helpers or validators
    examples/     sample inputs, outputs, or minimal skill patterns
    assets/       static resources required by the skill

Do not add folders just to make the skill look complete.

## 4. Draft SKILL.md

The root `SKILL.md` should include:

- frontmatter
- concise description
- when to use the skill
- when not to use the skill
- operating rules
- workflow
- safety boundaries
- references to supporting files

Keep it operational. Move long explanations into `references/`.

## 5. Add References Only When Useful

Use `references/` when the material is too long or too detailed for `SKILL.md`.

Good candidates:

- review checklists
- security rules
- schema notes
- API notes
- examples
- troubleshooting guides
- maturity models

## 6. Add Scripts Only When Safer Than Prose

Scripts may be appropriate for:

- validation
- formatting
- packaging
- parsing
- deterministic file checks
- repeatable setup checks

Scripts should not:

- hide risky behavior
- make unexpected network calls
- write outside approved paths
- install without approval
- handle secrets casually
- use encoded or obfuscated commands

## 7. Review Before Installation

Before installation or publication, review:

- frontmatter
- folder structure
- dependency assumptions
- permission boundaries
- secret handling
- prompt-injection exposure
- third-party provenance
- script behavior
- examples
- failure modes

Classify the skill maturity as draft, reviewed, approved, installed, deprecated, or unsafe.
