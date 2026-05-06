# Final Review and Red-Line Checklist

Use this reference for final-stage manuscript checks, especially LaTeX submissions.

## Error-Only Review Principle

At final stage, fix only issues that affect:

- Correctness
- Readability
- Logical consistency
- Submission compliance
- LaTeX compilation or cross-reference integrity
- Anonymity
- Artifact/data availability
- Reviewer comprehension

Do not perform optional stylistic polishing or rewrite technically precise sentences into fancier but less accurate prose.

## Critical Checks

### Abstract, Introduction, and Conclusion

- Do they state the same problem, object, method, evidence scale, and contribution?
- Does the abstract contain results that are missing from results/conclusion?
- Does the conclusion introduce new claims?
- Do contribution bullets match the evaluated evidence?
- Are `first`, `large-scale`, `comprehensive`, or `state-of-the-art` defensible?

### RQ and Evidence Alignment

- Each RQ has a method subsection and a result subsection.
- Each main result has a figure/table/textual evidence location.
- Each figure/table is referenced and interpreted.
- Metrics, denominators, datasets, and baselines are consistent.
- Statistical claims have tests or uncertainty where expected.

### Terminology

- Method/tool/dataset/model names are spelled consistently.
- Acronyms are defined at first use.
- RQ labels, section labels, and captions use the same terms.
- Human-study, vulnerability, repair, benchmark, model, and dataset terms are not mixed.

### LaTeX

- The paper compiles.
- No undefined references or citations.
- No duplicate labels.
- No broken commands, unmatched braces, bad math mode, or malformed tables.
- Captions and labels are in the right order.
- The bibliography style matches the template.
- Author-identifying comments, paths, or metadata are removed for anonymous submissions.

### Anonymity and Policy

- Remove author names, institutions, grants, acknowledgments, self-revealing artifact URLs, and repository ownership from anonymous versions unless the CFP allows them.
- Use anonymized artifacts when required.
- Check whether generative-AI assistance disclosure is required by the venue or publisher.
- Check artifact and data availability statements for consistency with anonymity and open science policy.

### Threats to Validity

- Construct, internal, external, and reliability threats are considered when relevant.
- Limitations match the actual scope.
- Mitigations are real and described in the method/evaluation.
- Generalization claims do not exceed languages, projects, datasets, models, or tasks studied.

## Red-Line Output Format

When asked to edit a LaTeX manuscript, produce:

1. `*-revised.tex`: original text preserved with visible corrections, preferably `\st{old} \textcolor{red}{new}`.
2. `*-final.tex`: clean final version with corrections applied and no markup.
3. `review.md`: Chinese or user-requested-language report containing only critical issues.

Ensure the revised file includes required packages if red-line macros are used:

```latex
\usepackage{xcolor}
\usepackage{soul}
```

Never alter math symbols, variable names, table values, labels, citations, algorithm logic, or experimental results unless the user explicitly authorizes it.

If a technical issue is suspected but uncertain, add a reviewer-style comment in `review.md` instead of silently changing the paper.
