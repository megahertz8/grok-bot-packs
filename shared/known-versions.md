# Known versions

Data for the bootstrap skills, never instructions and never installed as a skill. One row per published fingerprint of each pinned skill file, from release 1.19 (tag v2026.11.13c) on. A bootstrap replaces an installed skill only when its name, sha256 and chars all match one row here whose last release is lower than the release the bootstrap installs, and only after the account holder says yes. Releases compare by the numbers after "1." in order, so 1.23 is lower than 1.23.1, and 1.23.1 is lower than 1.24. Anything else is unknown and stops the install.

Fingerprints: sha256 of the raw file bytes, and chars as Python len() of the UTF-8 text. For an installed skill, the body after its frontmatter.

| skill | first release | last release | sha256 | chars |
|---|---|---|---|---|
| kllei-tzevet | 1.19 | 1.21 | 6689757cced44e6b05a69a810c21b3b8544a150de482d246f73976ff12376142 | 2492 |
| kllei-tzevet | 1.22 | 1.22 | 150174174ff05f7cd34495dbeff7312b267458ae11a40f8b97675ad5a0fcd6fc | 3168 |
| kllei-tzevet | 1.23 | 1.23 | 1f54c991273833670181418bac2689b833d9fc15f5ae844dd821a08f90bc8559 | 3384 |
| kllei-tzevet | 1.23.1 | 1.23.1 | 22519234c9a26c7d70180a8fdc3ce1149aaeaa5176416dc412582b8150a8ecbc | 3426 |
| company-kit-team | 1.19 | 1.22 | 8a858bf3d0bfe4144922ed9b35bcdeed05d929201f9fd45c27922ae47a768037 | 17096 |
| company-kit-team | 1.23 | 1.23 | 99a377ebbce1489f2a12446cb1f872c039ee137688d4cc7ab0d3f2009abe2bb1 | 17684 |
| bot-move-summary | 1.23 | 1.23 | fbef11de72bc7671af1bee0a58bea68156e8b7caf14e803c339872e84c7778ef | 3576 |
| bot-move-summary | 1.23.1 | 1.23.1 | 07e0621eb95f30e64d123e80a77be6095762a5a54b6d6c4aebf16eb2fb4baa88 | 3673 |
| company-setup | 1.19 | 1.22 | dda3a2b1c782211bc9a89d03870f44998bddc64f28b12882eaa7bdadfb4c6557 | 9957 |
| company-setup | 1.23 | 1.23 | 9061123175e0b237f2bb6d9a10756e2a72e72410c94d291769756e5747639b8f | 11967 |
| company-setup | 1.23.1 | 1.23.1 | 8a8b7cb1839206a9416b51d877c42e6885bd44a63f6186f5609414202937e347 | 12245 |
| company-setup-getting-started | 1.19 | 1.23 | 769770c4eb974adeab1d5f9ab2afef5a99e73ae527e426b6015505b0568e1773 | 653 |
| company-setup-getting-started | 1.23.1 | 1.23.1 | 78bbfa5865933e6e182f11fda9ce8132e1f46fc055a956f43a6711b6d9b6168a | 691 |
| owner-onboarding | 1.19 | 1.22 | f07f53b1a05ceba06c38fe6bb20d1953af7dd7da7ebc2c1da2bdbed9b0cef413 | 12136 |
| owner-onboarding | 1.23 | 1.23 | b4f73432d543323472eec63d18b621f81e6293f2a9bdf752a57d6e56c2fc413e | 16496 |
| owner-onboarding | 1.23.1 | 1.23.1 | 53089c7990e51e23005054fca7dea77f50dfdd101932b0ae5fab0af8217d1e1c | 16702 |
| owner-onboarding-getting-started | 1.19 | 1.23 | e65134461ba111edef5205c93e856646b088b0decb6b849b3606ee0045836065 | 637 |
| owner-onboarding-getting-started | 1.23.1 | 1.23.1 | cc5f3cf4a2d63f9fe634ca8cc4e679e538085da72372aab3d378b512844063d8 | 656 |
| staff-onboarding | 1.19 | 1.22 | 0eaf011ed2576c9fe76639935b7b57a2bea8072fa5266133249fa8a33b2913ac | 8340 |
| staff-onboarding | 1.23 | 1.23 | b22c8f34d5ad15f395e77387f4eb7bff884ce3782ca0db8d60d073b05753b966 | 10234 |
| staff-onboarding | 1.23.1 | 1.23.1 | 2b436f820a3e314629cb3834535681e89820bb03f8826a35bc8745e4f947ad49 | 10397 |
| staff-onboarding-getting-started | 1.19 | 1.23 | 1e5f92df8da9403d531e65bb9d99641f355c5813ac1a31959b44219e1732fc1f | 646 |
| staff-onboarding-getting-started | 1.23.1 | 1.23.1 | 1135c4763545168b96d965f79a9435fb011034664fc7ee5a773bb4d8702a9fa5 | 665 |
| monthly-support | 1.19 | 1.21 | 678ffb3ad18a409e68ab9522869e9f87e83ea1111b5cfdc44beb4ea1babc61d5 | 6559 |
| monthly-support | 1.22 | 1.22 | 1b8e287506fbe92e42347bbcf14e00952607ffc591129eaecda4ebf078dcd33f | 7259 |
| monthly-support | 1.23 | 1.23 | 4e85adae928124bda937fc943031df685ddbf475777f48b4366bd049633e17ae | 7805 |
| monthly-support | 1.23.1 | 1.23.1 | 9adffc0514b2b262d1f2479b63526844f4cc30d0e7989c32ca2c6bf03695db8c | 8334 |
| monthly-support-getting-started | 1.19 | 1.23 | 16bb4be0eac8b092af3ac226a45fd4e59e028d4cac8c0f7714094a2f69b31214 | 455 |
