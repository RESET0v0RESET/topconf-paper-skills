---
name: se-topconf-conclusion
description: Write, revise, diagnose, or teach Conclusion sections for ICSE, FSE, ASE, ISSTA, and adjacent top software engineering papers. Use when the user asks for an English top-SE conclusion, final paragraph, conclusion template, sentence-role analysis, or alignment between results, implications, limitations, and closing claims.
---

# SE Top-Conference Conclusion

Use this skill when the Conclusion is the main task. A strong top-SE conclusion closes the paper by compressing evidence and implications without adding unsupported claims.

## Core Chain

Default chain:

`paper object -> method/evidence -> main findings -> reusable contribution -> implications -> boundary/future direction -> grounded final takeaway`

Do not simply restate the abstract. Do not introduce new results.

## Minimum Inputs

Infer when possible; ask briefly if missing:

- Paper type and target venue.
- Research object and scope.
- Evidence scale: datasets, systems, models, projects, participants, experiments, artifacts.
- 2 to 4 main findings.
- Reusable output: tool, benchmark, dataset, taxonomy, framework, guidelines, replication package.
- Main limitation or future direction.
- Claims/data that must not change.

## Default Structure

Use 1 paragraph for short or page-limited papers.

Use 2 paragraphs for most empirical, method, benchmark, and SE tool papers.

Use 3 paragraphs only when the paper needs a separate safety/security/policy implication or future agenda.

## Paragraph 1: Work Recap and Findings

Sentence plan:

1. Topic closure: name the exact paper object and problem.
2. Evidence anchor: mention the method, dataset, experiments, systems, or scale.
3. Finding summary: strongest result.
4. Contrast/nuance: second result, trade-off, failure mode, or subgroup difference.
5. Contribution artifact: taxonomy/tool/dataset/benchmark/guidelines/replication package.

Example pattern:

```text
This paper presented [method/study/tool], designed to address [problem] in [scope]. By analyzing/evaluating [evidence], we found that [finding 1]. We further showed that [finding 2 or trade-off], highlighting [interpretation]. We also provide [artifact/contribution] to support [reuse].
```

## Paragraph 2: Implications and Closing

Sentence plan:

1. Practical value: name concrete audiences.
2. Academic value: explain what future research can build on, if justified.
3. Future direction or boundary: tie to the paper's limitations.
4. Strong takeaway: leave a grounded memory of the contribution.

Example pattern:

```text
These findings offer actionable guidance for [audience] by [specific use]. More broadly, they suggest that [field-level implication]. Future work should [specific next step tied to limitation]. Overall, [grounded final takeaway].
```

## Optional Paragraph 3: Security, Safety, or Policy

Use only when the paper has a real broader-impact claim.

Plan:

1. Name the risk or opportunity.
2. Explain why current practice is insufficient.
3. Recommend the next collective action.
4. Close with the desired grounded state.

## Sentence Role Tags

When diagnosing or teaching, label each sentence:

- Topic Closure
- Evidence Anchor
- Finding Summary
- Contrast/Nuance
- Contribution Artifact
- Practical Value
- Academic Value
- Boundary
- Future Direction
- Strong Takeaway

If a sentence has no role, delete or merge it.

## Style Rules

- Use present tense for stable findings: `Our results show...`
- Use past tense for completed study actions: `We analyzed...`
- Prefer `suggest`, `indicate`, `highlight`, `provide evidence`, and `offer guidance`.
- Avoid `great significance`, `fully proves`, `perfectly solves`, `obvious superiority`, and unsupported `state-of-the-art`.
- Name concrete audiences: `agent developers`, `benchmark designers`, `security researchers`, `tool builders`, `maintainers`.
- Keep future work specific and tied to observed limits.
- Keep the conclusion shorter than the abstract unless the user requests a detailed closing section.

## Output Modes

When writing:

1. Polished conclusion.
2. Optional sentence-role table.
3. Assumptions or missing facts.

When revising:

1. Sentence-role diagnosis.
2. Minimal-change revision.
3. Optional stronger version if the user wants a more assertive close.
