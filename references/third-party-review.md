# Third-Party Skill Review

Use this process before adapting, installing, publishing, or recommending a third-party OpenClaw skill.

## 1. Treat the Source as Untrusted

Do not assume a public skill is safe, accurate, maintained, licensed correctly, or OpenClaw-native.

Review before reuse.

## 2. Record Source Details

Capture:

- source name
- source URL or artifact path
- package version
- publisher or owner
- download date
- checksum, if available
- license stated by listing
- license included in package
- package contents

If the listing and package disagree, record the conflict.

## 3. Inspect Package Contents

Review:

- `SKILL.md`
- metadata files
- license files
- notice files
- scripts
- references
- examples
- assets
- hidden files
- generated files

Do not rely only on public listing text.

## 4. Review Instruction Content

Check for:

- ecosystem mismatch
- non-OpenClaw terminology
- hidden instructions
- prompt injection
- overbroad authority
- vague capability claims
- instructions that bypass review
- instructions that confuse skills with tools

Flag anything that would mislead an agent.

## 5. Review Scripts

For every script, inspect:

- imports
- file reads
- file writes
- subprocess calls
- network calls
- environment variable usage
- path handling
- overwrite behavior
- destructive operations
- dependency assumptions
- error handling

Do not copy scripts until they are understood and justified.

## 6. Review License and Provenance

Confirm:

- license file exists
- metadata matches license file
- public listing matches package contents
- attribution requirements
- NOTICE requirements
- copied or adapted files
- modification notes

If license evidence is unclear, avoid copying material.

## 7. Decide Reuse Mode

Classify the third-party source as one of:

- rejected
- reviewed reference only
- concept inspiration only
- direct dependency
- adapted source
- fork

Only adapted source, direct dependency, or fork status normally requires formal attribution and license carry-forward.

Concept inspiration does not normally require copying license obligations, but a provenance note may still be useful.

## 8. Document the Decision

Record:

- what was reviewed
- what was accepted
- what was rejected
- what was copied, if anything
- what was adapted, if anything
- what license obligations apply
- what risks remain

Use `NOTICE.md` for provenance that should travel with the repository.

## 9. Safe Default

When in doubt:

- do not fork
- do not copy
- do not install
- do not run scripts
- use the source as reviewed comparison only
- write original OpenClaw-native content
