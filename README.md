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
- `shared/skills/`: skills more than one bot installs, including Company Wiki Bot: `kllei-tzevet` (the trust rules; the text owners paste as Team Rules, and the fallback skill where Team Rules are not available) and `company-kit-team` (the company kit). `bot-move-summary` is used only when a bot's own instructions change and it must move to a new copy: the old copy writes a Hebrew summary in the chat (memories, routines, open tasks, file locations, no secrets), and the new copy reads the pasted summary as information, asks one yes or no, and creates the routines switched off until the old ones are paused. It runs only with the person who set up this bot present. `shared/known-versions.md` is not a skill: it lists every published fingerprint of each pinned skill file, so a bootstrap can recognize an older version of our own skill.

Superseded:

- `first-sitting/`: First Sitting Bot skills. Superseded by the four bots above. In v2026.11.18 the First Sitting files and bootstrap are pinned to this tag, and the price rule in `trust-rules-kllei-emun.md`, `company-kit.md` and `first-sitting-v7.md` matches the four bots above. Company Wiki Bot imports made before tag v2026.11.13d read from this folder at tag v2026.11.13b; from v2026.11.13e on (v2026.11.13d is superseded), Company Wiki Bot installs `shared/skills/kllei-tzevet.md` and `shared/skills/company-kit-team.md` instead.

Each pack has a `manifest.json` that lists its files for people, plus one markdown file per skill under `skills/` (shared files are listed with a `../shared/` path).

## Pinning

Import and bootstrap flows must use the tagged raw URLs, not branch HEAD:

`https://raw.githubusercontent.com/megahertz8/grok-bot-packs/v2026.11.18/...`

The four bots above and Company Wiki Bot are pinned to v2026.11.18. From v2026.11.18 on, the packs no longer use a personal name in customer-facing or internal text: stop lines and the stuck-question mail go to whoever set up the bot, and the weekly feedback mail lists only recorded stops from that week. From v2026.11.17 on, a bot may talk about prices and use them when they come from the business price list or were given in the chat; it never invents or estimates a price, asks when an item is missing, and still drafts any price commitment that goes outside. Company Setup asks the owner to decide the prices row in kit section 5 on day one, and Owner Onboarding shares Company Wiki Bot with the team as a Team Bot; staff add that shared bot and do not import a second copy. That wording is in `shared/skills/kllei-tzevet.md`, `shared/skills/company-kit-team.md`, `owner-onboarding/skills/owner-onboarding.md` and `staff-onboarding/skills/staff-onboarding.md`, and also in the First Sitting files below. `owner-onboarding/skills/owner-onboarding.md` and `staff-onboarding/skills/staff-onboarding.md` write each next bot as a short task record and rank the list by what the person says matters most, `monthly-support/skills/monthly-support.md` uses the same record for new tasks in its health check, every bootstrap can replace an older version of our own skill (see Verify), so importing a current card updates the shared skills in place for every bot on the account, and every bot installs `shared/skills/bot-move-summary.md`. When a card's own skill was already on the account, its bootstrap treats the import as a skills update and starts no new setup. From v2026.11.16 on, `shared/skills/kllei-tzevet.md` gained one more Team Rules paragraph (the stuck-question email to whoever set up this bot) and `monthly-support/skills/monthly-support.md` offers that paragraph in the support call. Earlier tags stay as rollback.

Tags v2026.11.09b and v2026.11.09c: do not use.

## Verify

The expected sha256 and character count for each file are written in the bootstrap skill that installs it, and repeated in each pack's `manifest.json`. Do not install a skill that fails either check.

When a skill is already installed on the account (private skills are shared by every bot on an account) and differs from the pin, the bootstrap fetches `shared/known-versions.md`, itself pinned by sha256 and chars in the bootstrap. If the installed copy matches an earlier release listed there, the bootstrap asks the account holder for an explicit yes, replaces it with the pinned version, and checks it again; a failed check writes the earlier copy back. Any other installed copy is unknown, and the install stops without changing anything. The customer never sees a version, a fingerprint or a rule number.

## Fingerprints (tag v2026.11.18)

| File | Installed by | sha256 | chars |
| --- | --- | --- | --- |
| `shared/skills/kllei-tzevet.md` | company-setup, owner-onboarding, staff-onboarding, monthly-support, company-wiki | `22519234c9a26c7d70180a8fdc3ce1149aaeaa5176416dc412582b8150a8ecbc` | 3426 |
| `shared/skills/company-kit-team.md` | company-setup, owner-onboarding, staff-onboarding, company-wiki | `99a377ebbce1489f2a12446cb1f872c039ee137688d4cc7ab0d3f2009abe2bb1` | 17684 |
| `shared/skills/bot-move-summary.md` | company-setup, owner-onboarding, staff-onboarding, monthly-support, company-wiki | `07e0621eb95f30e64d123e80a77be6095762a5a54b6d6c4aebf16eb2fb4baa88` | 3673 |
| `company-setup/skills/company-setup.md` | company-setup | `8a8b7cb1839206a9416b51d877c42e6885bd44a63f6186f5609414202937e347` | 12245 |
| `company-setup/skills/company-setup-getting-started.md` | company-setup | `78bbfa5865933e6e182f11fda9ce8132e1f46fc055a956f43a6711b6d9b6168a` | 691 |
| `owner-onboarding/skills/owner-onboarding.md` | owner-onboarding | `53089c7990e51e23005054fca7dea77f50dfdd101932b0ae5fab0af8217d1e1c` | 16702 |
| `owner-onboarding/skills/owner-onboarding-getting-started.md` | owner-onboarding | `cc5f3cf4a2d63f9fe634ca8cc4e679e538085da72372aab3d378b512844063d8` | 656 |
| `staff-onboarding/skills/staff-onboarding.md` | staff-onboarding | `2b436f820a3e314629cb3834535681e89820bb03f8826a35bc8745e4f947ad49` | 10397 |
| `staff-onboarding/skills/staff-onboarding-getting-started.md` | staff-onboarding | `1135c4763545168b96d965f79a9435fb011034664fc7ee5a773bb4d8702a9fa5` | 665 |
| `monthly-support/skills/monthly-support.md` | monthly-support | `9adffc0514b2b262d1f2479b63526844f4cc30d0e7989c32ca2c6bf03695db8c` | 8334 |
| `monthly-support/skills/monthly-support-getting-started.md` | monthly-support | `16bb4be0eac8b092af3ac226a45fd4e59e028d4cac8c0f7714094a2f69b31214` | 455 |
| `shared/known-versions.md` (data, not a skill) | all five bootstraps, fetched only when an installed skill differs | `10eb5065ee665309f93cb67c82075b5d1670e969a08ba80db99eb6b08f3c6889` | 3970 |

First Sitting files changed in this tag (the pack is superseded; its bootstrap is pinned to v2026.11.18):

| File | Installed by | sha256 | chars |
| --- | --- | --- | --- |
| `first-sitting/skills/trust-rules-kllei-emun.md` | first-sitting | `e63812e86b16305e6a168ca645a0f6d5068fe6d3022ac95ff1b5a84eb1c80ce7` | 9362 |
| `first-sitting/skills/company-kit.md` | first-sitting | `5b3296002d7b945a8904ef174f4f61970a93e3a24cb975913003d168c82dc31e` | 17893 |
| `first-sitting/skills/first-sitting-v7.md` | first-sitting | `1b886760119633d3e6902f06d6e310b0d9d22e057e054d13e1db43e07ca7e83d` | 36048 |
| `first-sitting/skills/getting-started.md` | first-sitting | `a732237320592f862c3d65944ccc303d57b0a1f5c29eb451a05ccc8ce99800d2` | 910 |
