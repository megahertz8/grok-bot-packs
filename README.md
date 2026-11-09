# grok-bot-packs

Public skill packs for Grok Bot templates that bootstrap themselves on first chat.

## Packs

- `first-sitting/`: First Sitting Bot skills

Each pack has a `manifest.json` with sha256 and character counts, plus one markdown file per skill under `skills/`.

## Pinning

Import and bootstrap flows must use the tagged raw URLs, not branch HEAD:

`https://raw.githubusercontent.com/megahertz8/grok-bot-packs/v2026.11.09d/...`

## Verify

After download, check sha256 and character count against `manifest.json`. Do not install a skill that fails either check.
