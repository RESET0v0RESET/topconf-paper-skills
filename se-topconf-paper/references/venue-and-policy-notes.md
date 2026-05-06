# Venue and Policy Notes

Use this reference when submission compliance matters. These notes are a starting point, not a substitute for the current CFP. Always verify the target venue/year before final submission.

## Current Snapshot Used to Build This Skill

The skill was built after checking public venue pages and ASE 2025 accepted/preprint papers on 2026-05-06.

Observed policy direction across ICSE/FSE/ASE/ISSTA:

- Double-anonymous reviewing is standard for research tracks.
- Artifact/data availability and open science are increasingly expected.
- Page/template rules differ by year and venue.
- FSE and ISSTA have been using PACMSE-style single-column `acmsmall` formatting in recent calls, while ASE 2025 used IEEE-style two-column formatting.
- Accepted/preprint papers commonly include explicit `Threats to Validity`, `Limitations`, `Data Availability`, `Artifact Availability`, or equivalent sections.

## Venue Rule Checks

Before enforcing formatting, check:

- Target venue and year.
- Track: research, industry, tool demo, NIER, journal-first, artifact, data/benchmark.
- Template: ACM `acmart` `sigconf`, ACM `acmsmall`, IEEEtran, or venue-specific template.
- Main-body page limit and whether references/appendices count.
- Double-anonymous rules and self-citation policy.
- Artifact evaluation expectations.
- Open science, data availability, replication package, and ethics/IRB requirements.
- Generative-AI usage/disclosure policy.

## Sources Consulted

- ASE 2025 Research Papers: https://conf.researchr.org/track/ase-2025/ase-2025-papers
- ICSE 2026 Research Track: https://conf.researchr.org/track/icse-2026/icse-2026-research-track
- FSE 2026 Research Papers: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers
- ISSTA 2026 Research Papers: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers
- Sample ASE 2025 accepted/preprint paper, software engineering agents: https://conf.researchr.org/details/ase-2025/ase-2025-papers/40/Understanding-Software-Engineering-Agents-A-Study-of-Thought-Action-Result-Trajector
- Sample arXiv preprint: https://arxiv.org/abs/2506.18824

## Submission Compliance Output

When the user asks for a submission check, return:

1. `Blockers`: items likely to cause desk rejection or serious reviewer confusion.
2. `Must fix`: unsupported claims, broken references, anonymity leaks, missing artifacts/data statements, missing threats, page/template conflicts.
3. `Should fix`: clarity issues affecting reader comprehension.
4. `Ask user`: factual/policy items that cannot be safely inferred.

Do not claim that a manuscript is submission-ready unless the current CFP has been checked and the manuscript compiles.
