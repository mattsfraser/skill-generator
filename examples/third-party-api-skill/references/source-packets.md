# Source Packet Notes

Use source packets to separate collection from judgment.

## Public Source Packet Fields

Record only reviewed public evidence:

- platform
- source URL
- handle
- tweet ID or post ID
- query text
- capture timestamp
- public metrics visible at capture time
- short summary
- caveats

## Example Packet

```json
{
  "platform": "x-twitter",
  "source_url": "https://x.com/example/status/1234567890",
  "handle": "example",
  "post_id": "1234567890",
  "query": "brand name example",
  "captured_at": "2026-06-16T04:00:00Z",
  "public_metrics": {
    "likes": 12,
    "replies": 3,
    "reposts": 1
  },
  "summary": "Public post mentioning the reviewed brand term.",
  "caveats": [
    "Metrics are point-in-time values.",
    "The packet is evidence, not a final assessment."
  ]
}
```

## Review Boundary

TweetClaw source: <https://github.com/Xquik-dev/tweetclaw>

Do not include raw cookies, API keys, private account data, direct messages,
or unrelated personal data in source packets.
