# grok-bot-packs

Public skill packs for Grok Bot templates that bootstrap themselves on first chat.

## Packs

- `first-sitting/`: First Sitting Bot skills
- `first-sitting/docs/prereq-checklist-he.md`: the Hebrew pre-meeting checklist the instructor sends customers before the first meeting (not a skill, not installed by the bootstrap)

Each pack has a `manifest.json` that lists its files for people, plus one markdown file per skill under `skills/`.

## Pinning

Import and bootstrap flows must use the tagged raw URLs, not branch HEAD:

`https://raw.githubusercontent.com/megahertz8/grok-bot-packs/v2026.11.12/...`

Tags v2026.11.09b and v2026.11.09c: do not use.

## Verify

The expected sha256 and character count for each file are written in the bootstrap skill that installs it. Do not install a skill that fails either check.
