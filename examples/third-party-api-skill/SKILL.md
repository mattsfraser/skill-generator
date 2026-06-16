---
name: third-party-api-skill
description: Demonstrate a skill that depends on an external API tool. Use when reviewing capability boundaries and source packet handling.
---

# Third-Party API Skill

Use this example to show how a skill can document an external API dependency
without implying that the skill grants credentials, network access, or tool
permission.

This example uses TweetClaw as an optional public X/Twitter source collector.
TweetClaw must already be installed, configured, and approved in the user's
OpenClaw environment before an agent can use it.

## Instructions

- Treat TweetClaw as an external capability, not as part of this skill.
- Use it only for reviewed public X/Twitter source packets.
- Capture source URLs, handles, tweet IDs, query text, capture timestamps,
  short summaries, and caveats.
- Do not store raw cookies, API keys, private account data, direct messages,
  or unrelated personal data in the skill folder.
- Keep posting, replying, media upload, direct messages, monitor setup,
  webhooks, and giveaway actions outside this skill unless a separate reviewed
  workflow explicitly approves them.
- If TweetClaw is unavailable, ask the user for exported source packets instead
  of inventing evidence.

## External Requirements

- Optional TweetClaw installation or equivalent reviewed source-packet export
- Network access approved by the host environment
- User-approved credentials or configuration stored outside this skill
- Human review before source packets are used for decisions

## Reference Files

Use this file when checking source packet structure:

- `{baseDir}/references/source-packets.md`
