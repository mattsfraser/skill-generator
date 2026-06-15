# Security Guidelines

Use these guidelines when designing, reviewing, or revising an OpenClaw skill.

## 1. Treat Skills as Instructions

A skill is an instruction package.

A skill does not automatically grant:

- shell access
- filesystem access
- API access
- credentials
- browser access
- network access
- third-party account access
- permission to install or modify files

Document required capabilities separately from skill instructions.

## 2. Never Store Secrets in Skill Files

Do not include:

- API keys
- access tokens
- refresh tokens
- private keys
- passwords
- session cookies
- webhook signing secrets
- SecretRef values
- personal data
- production credentials

Use placeholders such as:

- `OPENCLAW_API_KEY`
- `EXAMPLE_TOKEN`
- `your-api-key-here`

Placeholders must be obviously fake.

## 3. Declare External Requirements

If a skill depends on outside capabilities, document them clearly.

Examples:

- required CLI tools
- required Python or Node packages
- required environment variables
- required filesystem paths
- required APIs
- required network access
- required user approvals
- required OpenClaw configuration
- expected sandbox or permission boundary

Do not bury these assumptions in prose.

## 4. Review File Writes

Any skill or script that writes files should define:

- target path
- allowed file types
- overwrite behavior
- backup behavior
- dry-run behavior, if applicable
- confirmation requirements
- failure behavior

Avoid broad recursive writes unless justified.

## 5. Review Shell Commands

Shell commands should be:

- explicit
- minimal
- inspectable
- free of encoded payloads
- free of hidden downloads
- free of unnecessary privilege escalation

Avoid:

- `curl | sh`
- `wget | bash`
- opaque base64 commands
- broad `rm -rf`
- commands requiring `sudo` unless clearly justified
- commands that modify system config without review

## 6. Review Network Access

If network access is needed, document:

- destination service
- purpose
- authentication method
- data sent
- data received
- retry behavior
- failure behavior

Unexpected network calls are a security risk.

## 7. Review Third-Party Material

Treat third-party skills, scripts, examples, and packages as untrusted until reviewed.

Check for:

- prompt injection
- hidden instructions
- unexpected tool use
- unsafe shell commands
- dependency risks
- license conflicts
- credential exposure
- broad permissions
- obfuscated behavior

Do not install or adapt third-party material blindly.

## 8. Prefer Reviewable Defaults

Safe skill defaults include:

- read before write
- ask before destructive action
- dry-run before mutation
- least privilege
- explicit paths
- clear failure messages
- human review before installation
- no secrets in examples

## 9. Classify Risk

Classify skill risk before installation:

- low risk: instructions only, no scripts, no credentials, no external access
- medium risk: scripts, local file reads, generated artifacts
- high risk: file writes, shell commands, network access, credentials, system changes
- unsafe: hidden behavior, secrets, destructive defaults, unclear permissions

High-risk skills require deeper review.
