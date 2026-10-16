# COMP 447 Security Log Analysis — Dataset Notes

This folder contains **sanitized sample extracts** derived from the COMP 447 coursework reports. It is intended to show the structure and methods of authentication log reporting without publishing the full course dataset.

## Findings from the original completed reports

| Report | Complete original report rows | Reported events |
| --- | ---: | ---: |
| R1 — Successful authentications | 444 | 2,293 |
| R2 — Failed authentications | 15,450 | 80,994 |
| R3 — Failed authentications for legitimate accounts | 38 | 83 |
| R4 — Aggregated attack-source locations | 5,236 | 80,994 |

R4 groups failed authentications by source address; its reported event count is the same as R2's and **must not** be added to the R2 total. R3 is a subset of failed attempts and likewise should not be added to R2.

## Files

- `reports/R1_successful_authentications_SANITIZED_SAMPLE.csv` — sample successful logins
- `reports/R2_failed_authentications_SANITIZED_SAMPLE.csv` — sample failed logins
- `reports/R3_legitimate_user_failures_SANITIZED_SAMPLE.csv` — sample failures involving legitimate account names
- `reports/R4_attack_source_geolocation_SANITIZED_SAMPLE.csv` — sample source-location summary

## Sanitization procedure

- These are **selected, de-identified sample extracts**, not the complete original reports. The individual occurrence counts in samples come from selected original records; the sample data are not fully synthetic. Do not treat the placeholder locations as real geolocation results.
- Original account names are replaced by pseudonyms such as `user_001`.
- Original IP addresses are consistently mapped to non-routable documentation-only addresses from `192.0.2.0/24`, `198.51.100.0/24`, and `203.0.113.0/24`.
- Original geographic values are **not published**: `ZZ`, `Sample Region`, and `Sample City` are placeholders with no real geographic meaning.
- The sampled occurrence counts are retained from coursework; because these are subsets, **do not add the sample counts and interpret them as complete project totals**.
- Pseudonyms stay consistent between the four sample reports, where matching source records appear.
- No original username, original IP, password, or original geolocation value is intended to appear in this package.

**Important:** These reports remain derived from university coursework. Confirm your instructor permits publishing derivative samples before uploading them to a public repository. They are samples to illustrate analysis output, not datasets suitable for live network security investigations or IP geolocation.
