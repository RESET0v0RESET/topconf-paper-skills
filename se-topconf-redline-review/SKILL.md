---
name: se-topconf-redline-review
description: Perform final error-only red-line review of LaTeX manuscripts for ICSE, FSE, ASE, ISSTA, and adjacent top software engineering venues. Use when the user asks for pre-submission review, critical consistency check, grammar/Chinglish/logic/LaTeX error fixing, red-line revision, clean final tex output, or review report generation.
---

# SE Top-Conference Red-Line Review

Use this skill for final-stage review, not broad rewriting. Assume the manuscript has already been revised and should only receive critical fixes.

## Scope

Focus on:

1. Abstract, Introduction, Conclusion alignment.
2. RQ-method-result-contribution consistency.
3. Terminology, method names, task definitions, dataset/model names.
4. Logical gaps, contradictions, ambiguity, unsupported novelty, or overclaiming.
5. Serious grammar, spelling, Chinglish, and readability errors.
6. LaTeX issues: unmatched braces, broken labels, bad references, malformed commands, table/figure/caption problems.
7. Submission risks: anonymity leaks, missing threats, missing data/artifact availability, template/page-policy conflicts.

## Error-Only Principle

- Fix only issues affecting correctness, readability, or submission quality.
- Do not make optional stylistic changes.
- Do not replace technically precise text with more sophisticated but less accurate phrasing.
- Do not change math symbols, variables, method names, dataset names, citations, table values, labels, algorithms, or results unless explicitly authorized.
- If a technical issue is suspected but uncertain, add it to the review report instead of silently editing.

## Red-Line Format

When editing LaTeX, produce:

1. `<original-name>-revised.tex`
   - Preserve original text with visible corrections.
   - Recommended markup: `\st{original text} \textcolor{red}{revised text}`.
   - Ensure the preamble contains:

```latex
\usepackage{xcolor}
\usepackage{soul}
```

2. `<original-name>-final.tex`
   - Clean final version with all accepted corrections and no markup.

3. `review.md`
   - Brief report in Chinese unless the user requests another language.
   - Include only critical issues.
   - For each issue: location, type, reason for modification, and whether it was fixed or needs author confirmation.

## Review Procedure

1. Compile or inspect compile logs if possible.
2. Read Abstract, Introduction, RQs/EQs, Results, Threats, Data/Artifact Availability, and Conclusion first.
3. Build a short consistency map:

| Item | Abstract | Intro | Results | Conclusion | Issue |
|---|---|---|---|---|---|

4. Scan the whole paper for terminology, labels, citations, table/figure references, and overclaims.
5. Apply only critical corrections.
6. Produce the revised file, final file, and report.

## Critical Issue Types

- `Logic`: contradiction, missing bridge, unsupported conclusion.
- `Consistency`: terminology, RQ, metric, dataset, model, baseline, or contribution mismatch.
- `Evidence`: claim lacks result/table/figure/citation support.
- `Overclaim`: excessive novelty, generality, significance, or causality.
- `Language`: grammar or Chinglish that impairs comprehension.
- `LaTeX`: compile, cross-reference, citation, float, command, or package problem.
- `Policy`: anonymity, artifact/data availability, ethics, template, page-limit, or disclosure risk.

## Default Report Style

Use concise Chinese:

```markdown
# Review Report

## Critical Issues

1. Location: Abstract, sentence 3
   Type: Consistency
   Reason: The abstract claims evaluation on five models, but Section 4 reports four models.
   Action: Marked for author confirmation; no numeric edit was made.
```

If there are no critical issues, say so and list remaining residual risks such as "未运行 LaTeX 编译" or "未核对最新 CFP".
