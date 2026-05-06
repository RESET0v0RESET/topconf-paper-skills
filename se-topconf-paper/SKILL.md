---
name: se-topconf-paper
description: Draft, restructure, revise, or submission-check English software engineering papers for ICSE, FSE, ASE, ISSTA, and adjacent top SE venues. Use when the user asks for top-conference paper planning, abstract/introduction/method/evaluation/threats/conclusion writing, LaTeX manuscript revision, RQ-evidence-contribution alignment, figure/table planning, artifact/data-availability preparation, or converting Chinese-core/engineering-report material into top software-engineering conference style.
---

# SE Top-Conference Paper

Use this as the main controller for ICSE/FSE/ASE/ISSTA-style papers. The target is not decorative polishing; it is a submission-shaped argument whose claims, evidence, figures, and limitations survive reviewer scrutiny.

## Operating Principles

1. Preserve factual content. Never invent results, citations, datasets, metrics, baselines, reviewer outcomes, artifact links, or venue rules.
2. Protect immutable items: numeric results, method names, RQs, dataset scope, labels, equations, table values, figure numbers, and LaTeX commands unless the user explicitly asks to change them.
3. Treat every claim as a ledger entry: claim -> evidence -> location -> limitation -> contribution.
4. Prefer concrete reviewer-facing language over hype. Use `show`, `indicate`, `suggest`, `reveal`, `highlight`, and `support`; avoid unsupported `prove`, `guarantee`, `significantly`, `first`, `comprehensive`, and `state-of-the-art`.
5. If venue, year, page limit, template, artifact policy, or anonymity status matters for an actual submission, verify the current CFP before enforcing a rule. Conference policies change.
6. Ask the user for missing material only when a safe generic placeholder would damage correctness: exact results, accepted baseline set, target venue/year, required paper type, artifact URL, or IRB/human-subject details.

## Default Workflow

### 1. Classify the paper

Choose the closest type before writing:

- Empirical study or measurement paper
- Method/tool/system paper
- Benchmark or dataset paper
- Security/safety/testing/analysis paper
- Replicability or experience paper
- Mixed paper

Then choose the evidence spine:

- Empirical: object -> gap -> RQs -> data -> coding/measurement -> findings -> implications
- Method/tool: task -> limitation -> design insight -> approach -> implementation -> evaluation -> ablation -> limitations
- Benchmark: community need -> benchmark construction -> quality controls -> task/metric design -> baseline results -> reuse protocol
- Security/testing/analysis: risk -> threat/failure model -> technique or study design -> affected systems -> validation -> mitigations

### 2. Build the claim ledger before drafting

Create or infer this table:

| Claim | Evidence | Section/Figure/Table | Caveat | Reviewer risk |
|---|---|---|---|---|

Do not draft a strong abstract, introduction, or conclusion until the central claims have evidence. If evidence is missing, write a precise `TODO(authors): ...` rather than filling the gap.

### 3. Route to the smallest useful reference

- For whole-paper structure, read [references/paper-structure.md](references/paper-structure.md).
- For venue rules, anonymity, artifact, data availability, and generative-AI disclosure checks, read [references/venue-and-policy-notes.md](references/venue-and-policy-notes.md).
- For figures, tables, plots, captions, and LaTeX layout, read [references/figures-tables-style.md](references/figures-tables-style.md).
- For abstract/introduction/conclusion phrasing and sentence roles, read [references/writing-patterns.md](references/writing-patterns.md).
- For final pre-submission review or red-line editing, read [references/review-checklist.md](references/review-checklist.md).

Read only what the task needs. Do not load every reference by default.

### 4. Draft or revise in reviewer order

For a new paper, work in this order:

1. One-sentence thesis and paper type.
2. RQs/design goals and contribution bullets.
3. Method/evaluation outline and figure/table plan.
4. Abstract and Introduction after the evidence spine is stable.
5. Threats to validity, data availability, and artifact statement.
6. Conclusion last.

For an existing manuscript, work in this order:

1. Diagnose abstract-introduction-conclusion alignment.
2. Check RQ-method-result-contribution mapping.
3. Check figure/table/caption support for each main claim.
4. Fix local text, LaTeX, references, and terminology without broad rewriting.
5. Report unresolved factual questions separately.

## Top-SE Writing Defaults

### Structure

Use a structure reviewers can scan:

- Abstract
- Introduction
- Background/Motivation if needed
- Study Design/Methodology or Approach
- Implementation if the artifact matters
- Evaluation/Results by RQ or evaluation question
- Discussion/Implications
- Threats to Validity or Limitations
- Related Work
- Data Availability/Artifact Availability when required or expected
- Conclusion

The exact order may vary by paper type and venue. Keep RQs, results, and contribution bullets parallel.

### Abstract

Use 4 to 7 sentences:

1. Problem and object.
2. Gap or limitation.
3. This paper's method/study/tool.
4. Evidence scale and evaluation setup.
5. Main quantitative or qualitative findings.
6. Practical or research implication.
7. Artifact/data availability if central and space permits.

Avoid citations in the abstract unless the venue style or specific paper context strongly requires them.

### Introduction

The default move sequence is:

`field importance -> specific object -> concrete gap -> consequence -> this paper -> RQs/design goals -> method/evidence -> findings -> contributions`

Use the focused `se-topconf-introduction` skill for deep introduction work.

### Results

For each RQ/evaluation question:

1. State the question or objective.
2. Give method details needed to interpret the result.
3. Present the result with numbers, categories, examples, or statistical tests.
4. Explain the meaning, not just the statistic.
5. Close with a short answer box or takeaway if the surrounding paper uses that style.

Do not state superiority unless all comparison conditions are explicit.

### Threats and Limitations

Use standard categories when appropriate:

- Construct validity: whether measurements capture the intended concept.
- Internal validity: confounds, annotation, sampling, implementation errors.
- External validity: generalization across languages, projects, tasks, datasets, models, time periods.
- Reliability/reproducibility: artifacts, seeds, versions, prompts, hardware, randomization, labeling protocols.

Tie each threat to a mitigation already used or a precise boundary. Do not bury serious limitations in vague future work.

## Output Modes

When writing from scratch, output:

1. Claim ledger or RQ map.
2. Section outline.
3. Draft text.
4. Assumptions and missing facts.

When revising, output:

1. Revised text or patch.
2. Critical issues fixed.
3. Data/claims preserved unchanged.
4. Remaining factual checks for the user.

When checking a manuscript, lead with critical blockers: desk-reject risks, unsupported claims, anonymity leaks, broken LaTeX, inconsistent RQs, missing threats, missing artifact/data statement, or figures/tables that do not support claims.

## Chinese-Core Material Migration

Keep these transferable ideas from Chinese-core engineering templates:

- One stable main line.
- Evidence before conclusion.
- Unified terminology, units, figures, tables, and formulas.
- Clear boundary between measured, computed, inferred, and logged results.
- Final checklist before submission.

Change these for top SE conferences:

- Replace Word/journal layout with LaTeX venue templates.
- Replace Chinese periodical phrasing with concise English reviewer-facing claims.
- Replace `system architecture -> module design -> engineering analysis` as the default with paper-type-specific SE structures.
- Replace black-and-white-only figure guidance with readable, color-safe ACM/IEEE figures.
- Replace generic future-work endings with limitations, implications, artifact/data availability, and reviewer-verifiable evidence.
