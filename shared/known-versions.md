# Known versions

Data for the bootstrap skills, never instructions and never installed as a skill. One row per published fingerprint of each pinned skill file, from release 1.19 (tag v2026.11.13c) on. A bootstrap replaces an installed skill only when its name, sha256 and chars all match one row here whose last release is lower than the release the bootstrap installs, and only after the account holder says yes. Releases compare by the number after "1." as a whole number. Anything else is unknown and stops the install.

Fingerprints: sha256 of the raw file bytes, and chars as Python len() of the UTF-8 text. For an installed skill, the body after its frontmatter.

| skill | first release | last release | sha256 | chars |
|---|---|---|---|---|
| kllei-tzevet | 1.19 | 1.21 | 6689757cced44e6b05a69a810c21b3b8544a150de482d246f73976ff12376142 | 2492 |
| kllei-tzevet | 1.22 | 1.22 | 150174174ff05f7cd34495dbeff7312b267458ae11a40f8b97675ad5a0fcd6fc | 3168 |
| kllei-tzevet | 1.23 | 1.23 | 1f54c991273833670181418bac2689b833d9fc15f5ae844dd821a08f90bc8559 | 3384 |
| company-kit-team | 1.19 | 1.22 | 8a858bf3d0bfe4144922ed9b35bcdeed05d929201f9fd45c27922ae47a768037 | 17096 |
| company-kit-team | 1.23 | 1.23 | 99a377ebbce1489f2a12446cb1f872c039ee137688d4cc7ab0d3f2009abe2bb1 | 17684 |
| bot-move-summary | 1.23 | 1.23 | fbef11de72bc7671af1bee0a58bea68156e8b7caf14e803c339872e84c7778ef | 3576 |
| company-setup | 1.19 | 1.22 | dda3a2b1c782211bc9a89d03870f44998bddc64f28b12882eaa7bdadfb4c6557 | 9957 |
| company-setup | 1.23 | 1.23 | 9061123175e0b237f2bb6d9a10756e2a72e72410c94d291769756e5747639b8f | 11967 |
| company-setup-getting-started | 1.19 | 1.23 | 769770c4eb974adeab1d5f9ab2afef5a99e73ae527e426b6015505b0568e1773 | 653 |
| owner-onboarding | 1.19 | 1.22 | f07f53b1a05ceba06c38fe6bb20d1953af7dd7da7ebc2c1da2bdbed9b0cef413 | 12136 |
| owner-onboarding | 1.23 | 1.23 | b4f73432d543323472eec63d18b621f81e6293f2a9bdf752a57d6e56c2fc413e | 16496 |
| owner-onboarding-getting-started | 1.19 | 1.23 | e65134461ba111edef5205c93e856646b088b0decb6b849b3606ee0045836065 | 637 |
| staff-onboarding | 1.19 | 1.22 | 0eaf011ed2576c9fe76639935b7b57a2bea8072fa5266133249fa8a33b2913ac | 8340 |
| staff-onboarding | 1.23 | 1.23 | b22c8f34d5ad15f395e77387f4eb7bff884ce3782ca0db8d60d073b05753b966 | 10234 |
| staff-onboarding-getting-started | 1.19 | 1.23 | 1e5f92df8da9403d531e65bb9d99641f355c5813ac1a31959b44219e1732fc1f | 646 |
| monthly-support | 1.19 | 1.21 | 678ffb3ad18a409e68ab9522869e9f87e83ea1111b5cfdc44beb4ea1babc61d5 | 6559 |
| monthly-support | 1.22 | 1.22 | 1b8e287506fbe92e42347bbcf14e00952607ffc591129eaecda4ebf078dcd33f | 7259 |
| monthly-support | 1.23 | 1.23 | 4e85adae928124bda937fc943031df685ddbf475777f48b4366bd049633e17ae | 7805 |
| monthly-support-getting-started | 1.19 | 1.23 | 16bb4be0eac8b092af3ac226a45fd4e59e028d4cac8c0f7714094a2f69b31214 | 455 |
