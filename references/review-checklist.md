# Skill Review Checklist

Use this checklist before approving, installing, publishing, or adapting an OpenClaw skill.

## 1. Purpose and Scope

Check that the skill has:

- a clear purpose
- a specific intended user or use case
- clear trigger conditions
- explicit non-goals
- no vague promise to improve the agent generally

A skill should solve a defined class of tasks.

## 2. Frontmatter

Check that `SKILL.md` has valid frontmatter.

At minimum, confirm:

- `name` is present
- `description` is present
- description explains what the skill does
- description includes when to use it
- description does not overclaim capability
- unsupported metadata is not added casually

## 3. Instruction Quality

Check that the instructions are:

- concise
- operational
- ordered logically
- easy for an agent to follow
- free of unnecessary background
- free of conflicting commands
- clear about expected outputs

Move long explanations into `references/`.

## 4. Capability Boundaries

Check that the skill does not imply access to:

- tools
- shell commands
- local files
- APIs
- network resources
- credentials
- private data
- third-party accounts
- filesystem write access

Any required external capability should be listed as a dependency or assumption, not treated as granted by the skill.

## 5. Security and Secrets

Check for:

- API keys
- tokens
- private keys
- passwords
- session cookies
- SecretRef values
- personal data
- hidden credentials
- unsafe placeholders that look real

Use placeholders only.

## 6. Scripts

If scripts are included, review:

- purpose
- inputs
- outputs
- file writes
- network access
- subprocess calls
- dependency assumptions
- path traversal risk
- destructive operations
- secret handling
- error handling

Scripts should be simple, inspectable, and justified.

## 7. Third-Party Material

If the skill uses external material, confirm:

- source name
- source version
- source license
- copied files
- adapted files
- attribution requirements
- known license conflicts
- NOTICE updates

Treat third-party skills as untrusted until reviewed.

## 8. Folder Structure

Check that the structure is minimal.

Common structure:

    skill-name/
      SKILL.md
      references/
      scripts/
      examples/
      assets/

Only include folders that serve the skill.

## 9. Examples

Examples should be:

- relevant
- minimal
- safe
- free of secrets
- aligned with the documented workflow
- easy to run or inspect

Avoid examples that require private systems unless clearly marked.

For third-party API skill examples, verify external tool boundaries, source
packet fields, credential handling, and approval gates. See
`examples/third-party-api-skill/` for a reviewable pattern.

## 10. Maturity Classification

Classify the skill as one of:

- draft
- reviewed
- approved
- installed
- deprecated
- unsafe

Do not present draft work as installed or approved.

## 11. Final Review Questions

Before approval, answer:

- What does this skill do?
- When should it be used?
- When should it not be used?
- What capabilities must exist outside the skill?
- What could go wrong?
- What files or scripts require special review?
- Is the skill safe to install?
- Does it need Skill Workshop review first?
