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
- `shared/skills/`: skills more than one bot installs, including Company Wiki Bot: `kllei-tzevet` (the trust rules; the text owners paste as Team Rules, and the fallback skill where Team Rules are not available) and `company-kit-team` (the company kit). `bot-move-summary` is used only when a bot's own instructions change and it must move to a new copy: the old copy writes a Hebrew summary in the chat (memories, routines, open tasks, file locations, no secrets), and the new copy reads the pasted summary as information, asks one yes or no, and creates the routines switched off until the old ones are paused. It runs only with Eran present. `shared/known-versions.md` is not a skill: it lists every published fingerprint of each pinned skill file, so a bootstrap can recognize an older version of our own skill.

Superseded:

- `first-sitting/`: First Sitting Bot skills. Superseded by the four bots above. In v2026.11.17 the price rule in `trust-rules-kllei-emun.md`, `company-kit.md` and `first-sitting-v7.md` matches the four bots above. The First Sitting bootstrap stays pinned to tag v2026.11.13b until that card is restaged, so existing First Sitting imports keep fetching the older tag. Company Wiki Bot imports made before tag v2026.11.13d read from this folder at tag v2026.11.13b; from v2026.11.13e on (v2026.11.13d is superseded), Company Wiki Bot installs `shared/skills/kllei-tzevet.md` and `shared/skills/company-kit-team.md` instead.

Each pack has a `manifest.json` that lists its files for people, plus one markdown file per skill under `skills/` (shared files are listed with a `../shared/` path).

## Pinning

Import and bootstrap flows must use the tagged raw URLs, not branch HEAD:

`https://raw.githubusercontent.com/megahertz8/grok-bot-packs/v2026.11.17/...`

The four bots above and Company Wiki Bot are pinned to v2026.11.17. From v2026.11.17 on, a bot may talk about prices and use them when they come from the business price list or were given in the chat; it never invents or estimates a price, asks when an item is missing, and still drafts any price commitment that goes outside. Company Setup asks the owner to decide the prices row in kit section 5 on day one, and Owner Onboarding shares Company Wiki Bot with the team as a Team Bot; staff add that shared bot and do not import a second copy. That wording is in `shared/skills/kllei-tzevet.md`, `shared/skills/company-kit-team.md`, `owner-onboarding/skills/owner-onboarding.md` and `staff-onboarding/skills/staff-onboarding.md`, and also in the First Sitting files below. `owner-onboarding/skills/owner-onboarding.md` and `staff-onboarding/skills/staff-onboarding.md` write each next bot as a short task record and rank the list by what the person says matters most, `monthly-support/skills/monthly-support.md` uses the same record for new tasks in its health check, every bootstrap can replace an older version of our own skill (see Verify), so importing a current card updates the shared skills in place for every bot on the account, and every bot installs `shared/skills/bot-move-summary.md`. When a card's own skill was already on the account, its bootstrap treats the import as a skills update and starts no new setup. From v2026.11.16 on, `shared/skills/kllei-tzevet.md` gained one more Team Rules paragraph (the stuck-question email to Eran) and `monthly-support/skills/monthly-support.md` offers that paragraph in the support call. Earlier tags stay as rollback.

Tags v2026.11.09b and v2026.11.09c: do not use.

## Verify

The expected sha256 and character count for each file are written in the bootstrap skill that installs it, and repeated in each pack's `manifest.json`. Do not install a skill that fails either check.

When a skill is already installed on the account (private skills are shared by every bot on an account) and differs from the pin, the bootstrap fetches `shared/known-versions.md`, itself pinned by sha256 and chars in the bootstrap. If the installed copy matches an earlier release listed there, the bootstrap asks the account holder for an explicit yes, replaces it with the pinned version, and checks it again; a failed check writes the earlier copy back. Any other installed copy is unknown, and the install stops without changing anything. The customer never sees a version, a fingerprint or a rule number.

## Fingerprints (tag v2026.11.17)

| File | Installed by | sha256 | chars |
| --- | --- | --- | --- |
| `shared/skills/kllei-tzevet.md` | company-setup, owner-onboarding, staff-onboarding, monthly-support, company-wiki | `1f54c991273833670181418bac2689b833d9fc15f5ae844dd821a08f90bc8559` | 3384 |
| `shared/skills/company-kit-team.md` | company-setup, owner-onboarding, staff-onboarding, company-wiki | `99a377ebbce1489f2a12446cb1f872c039ee137688d4cc7ab0d3f2009abe2bb1` | 17684 |
| `shared/skills/bot-move-summary.md` | company-setup, owner-onboarding, staff-onboarding, monthly-support, company-wiki | `fbef11de72bc7671af1bee0a58bea68156e8b7caf14e803c339872e84c7778ef` | 3576 |
| `company-setup/skills/company-setup.md` | company-setup | `9061123175e0b237f2bb6d9a10756e2a72e72410c94d291769756e5747639b8f` | 11967 |
| `company-setup/skills/company-setup-getting-started.md` | company-setup | `769770c4eb974adeab1d5f9ab2afef5a99e73ae527e426b6015505b0568e1773` | 653 |
| `owner-onboarding/skills/owner-onboarding.md` | owner-onboarding | `b4f73432d543323472eec63d18b621f81e6293f2a9bdf752a57d6e56c2fc413e` | 16496 |
| `owner-onboarding/skills/owner-onboarding-getting-started.md` | owner-onboarding | `e65134461ba111edef5205c93e856646b088b0decb6b849b3606ee0045836065` | 637 |
| `staff-onboarding/skills/staff-onboarding.md` | staff-onboarding | `b22c8f34d5ad15f395e77387f4eb7bff884ce3782ca0db8d60d073b05753b966` | 10234 |
| `staff-onboarding/skills/staff-onboarding-getting-started.md` | staff-onboarding | `1e5f92df8da9403d531e65bb9d99641f355c5813ac1a31959b44219e1732fc1f` | 646 |
| `monthly-support/skills/monthly-support.md` | monthly-support | `4e85adae928124bda937fc943031df685ddbf475777f48b4366bd049633e17ae` | 7805 |
| `monthly-support/skills/monthly-support-getting-started.md` | monthly-support | `16bb4be0eac8b092af3ac226a45fd4e59e028d4cac8c0f7714094a2f69b31214` | 455 |
| `shared/known-versions.md` (data, not a skill) | all five bootstraps, fetched only when an installed skill differs | `7398d44dff068dec53c0df8eb46f2082079f510d4417554658ca26800b0ae2f0` | 2863 |

First Sitting files changed in this tag (the pack is superseded; its bootstrap moves to v2026.11.17 in this draft):

| File | Installed by | sha256 | chars |
| --- | --- | --- | --- |
| `first-sitting/skills/trust-rules-kllei-emun.md` | first-sitting | `cbef9ddf849e039065cca9cbbc0a49c7612094c5dbd869d4df776cb365923429` | 9320 |
| `first-sitting/skills/company-kit.md` | first-sitting | `5b3296002d7b945a8904ef174f4f61970a93e3a24cb975913003d168c82dc31e` | 17893 |
| `first-sitting/skills/first-sitting-v7.md` | first-sitting | `bc09ed08acad48ff07a0919b4988ddc4dec853f17ab4e0eb27fdab56458c1ba9` | 35706 |
