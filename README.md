# grok-bot-packs

Public skill packs for Grok Bot templates that bootstrap themselves on first chat.

## Packs

Four bots for a business on a Team plan, used in this order:

- `company-setup/`: Company Setup Bot skills. Team Rules check, admin settings explained, kit sections 1, 5 and 6, company wiki, one first task per person.
- `company-setup/docs/prereq-checklist-he.md`: the Hebrew checklist the instructor sends before Company setup (not a skill, not installed by the bootstrap).
- `company-setup/docs/room-setup-checklist.md`: the instructor's in-person Team plan setup, done before the Company setup bot (not a skill).
- `owner-onboarding/`: Owner Onboarding Bot skills. One draft-only bot and one real draft for the owner.
- `staff-onboarding/`: Staff Onboarding Bot skills. The same for each staff member, on their own seat.
- `monthly-support/`: Monthly Support Bot skills. One copy on each paying person's own account.
- `shared/skills/`: skills more than one of these bots installs: `kllei-tzevet` (the trust rules; the text owners paste as Team Rules, and the fallback skill where Team Rules are not available) and `company-kit-team` (the company kit).

Superseded:

- `first-sitting/`: First Sitting Bot skills. Superseded by the four bots above. Kept unchanged so existing imports keep working; its bootstrap stays pinned to tag v2026.11.13b. Company Wiki Bot's bootstrap also still reads from this folder at that tag.

Each pack has a `manifest.json` that lists its files for people, plus one markdown file per skill under `skills/` (shared files are listed with a `../shared/` path).

## Pinning

Import and bootstrap flows must use the tagged raw URLs, not branch HEAD:

`https://raw.githubusercontent.com/megahertz8/grok-bot-packs/v2026.11.13c/...`

Tags v2026.11.09b and v2026.11.09c: do not use.

## Verify

The expected sha256 and character count for each file are written in the bootstrap skill that installs it, and repeated in each pack's `manifest.json`. Do not install a skill that fails either check.

## Fingerprints at tag v2026.11.13c

| File | Installed by | sha256 | chars |
| --- | --- | --- | --- |
| `shared/skills/kllei-tzevet.md` | company-setup, owner-onboarding, staff-onboarding, monthly-support | `6689757cced44e6b05a69a810c21b3b8544a150de482d246f73976ff12376142` | 2492 |
| `shared/skills/company-kit-team.md` | company-setup, owner-onboarding, staff-onboarding | `8a858bf3d0bfe4144922ed9b35bcdeed05d929201f9fd45c27922ae47a768037` | 17096 |
| `company-setup/skills/company-setup.md` | company-setup | `dda3a2b1c782211bc9a89d03870f44998bddc64f28b12882eaa7bdadfb4c6557` | 9957 |
| `company-setup/skills/company-setup-getting-started.md` | company-setup | `769770c4eb974adeab1d5f9ab2afef5a99e73ae527e426b6015505b0568e1773` | 653 |
| `owner-onboarding/skills/owner-onboarding.md` | owner-onboarding | `f07f53b1a05ceba06c38fe6bb20d1953af7dd7da7ebc2c1da2bdbed9b0cef413` | 12136 |
| `owner-onboarding/skills/owner-onboarding-getting-started.md` | owner-onboarding | `e65134461ba111edef5205c93e856646b088b0decb6b849b3606ee0045836065` | 637 |
| `staff-onboarding/skills/staff-onboarding.md` | staff-onboarding | `0eaf011ed2576c9fe76639935b7b57a2bea8072fa5266133249fa8a33b2913ac` | 8340 |
| `staff-onboarding/skills/staff-onboarding-getting-started.md` | staff-onboarding | `1e5f92df8da9403d531e65bb9d99641f355c5813ac1a31959b44219e1732fc1f` | 646 |
| `monthly-support/skills/monthly-support.md` | monthly-support | `678ffb3ad18a409e68ab9522869e9f87e83ea1111b5cfdc44beb4ea1babc61d5` | 6559 |
| `monthly-support/skills/monthly-support-getting-started.md` | monthly-support | `16bb4be0eac8b092af3ac226a45fd4e59e028d4cac8c0f7714094a2f69b31214` | 455 |
