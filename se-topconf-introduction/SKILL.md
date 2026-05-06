---
name: se-topconf-introduction
description: Write, rewrite, diagnose, or teach Introduction sections for ICSE, FSE, ASE, ISSTA, and adjacent top software engineering papers. Use when the user asks for an English top-SE introduction, paragraph blueprint, sentence-function annotation, gap/RQ/contribution alignment, or conversion from Chinese/engineering-report introduction style into reviewer-facing conference style.
---

# SE Top-Conference Introduction

Use this skill when the Introduction is the main task. The goal is a reviewer-readable logical chain, not generic academic polish.

## Core Chain

Build the Introduction as:

`field importance -> specific object -> evidence of relevance -> concrete gap -> consequence -> this paper -> RQs/design goals -> method/evidence -> findings -> positioning -> contributions`

Every sentence needs one rhetorical job. If a sentence cannot be labeled, revise or delete it.

## Minimum Inputs

Infer from the manuscript when possible. Ask only if missing facts would force invention:

- Target venue/year and paper type.
- Research object and exact scope.
- Closest prior work or baseline.
- Dataset/artifact scale.
- RQs or design/evaluation goals.
- Main findings and contribution bullets.
- Claims that must not be changed.

## Sentence Function Labels

Use these labels for planning, annotation, and revision:

| Label | Function |
|---|---|
| BACKGROUND | Establish broad SE context. |
| OBJECT | Define the exact research object. |
| SCALE | Prove relevance with adoption, usage, prevalence, dataset, or risk evidence. |
| VALUE | Explain why the object matters to a concrete audience. |
| MECHANISM | Explain how the object/system/process works at a high level. |
| PROBLEM | Introduce a limitation, risk, or unresolved challenge. |
| PRIOR | Summarize what prior work covers. |
| GAP | State the precise missing knowledge, capability, or evidence. |
| CONSEQUENCE | Explain why the gap matters. |
| OPPORTUNITY | Explain why the gap can now be studied or solved. |
| OBJECTIVE | State what this paper does. |
| SCOPE | Bound systems, languages, models, projects, datasets, tasks, or time. |
| RQ | Present research questions or evaluation goals. |
| METHOD | Preview data collection, implementation, analysis, or evaluation. |
| FINDING | Preview key results and meaning. |
| POSITION | Differentiate from closest work. |
| CONTRIBUTION | Package concrete contributions. |

## Default Paragraph Blueprint

### P1: Importance and Object

Purpose: make the reader understand why the topic matters and what is being studied.

Plan:

1. BACKGROUND: current SE trend, practice, or technical shift.
2. OBJECT: exact object of study or method.
3. SCALE: adoption, dataset, ecosystem, user, bug, vulnerability, model, benchmark, or project evidence.
4. VALUE: why researchers/developers/tool builders/maintainers care.

Avoid empty openings such as `With the rapid development of...` unless followed by concrete evidence.

### P2: Concrete Setting or Mechanism

Purpose: narrow from the field to the paper's operating context.

Plan:

1. MECHANISM: how the object works or is used.
2. VALUE/SCALE: representative tools, projects, workflows, or failure scenarios.
3. SCOPE: exact domain, language, model family, artifact, or task.

For security/testing papers, include a concrete harm or failure scenario early.

### P3: Prior Work, Gap, Consequence

Purpose: create the need for the paper.

Plan:

1. PRIOR: what existing studies/tools/benchmarks have covered.
2. PROBLEM/GAP: what remains unknown or unsupported.
3. CONSEQUENCE: why that missing piece blocks research or practice.

Weak gap:

```text
Few studies have explored X.
```

Strong gap:

```text
It remains unclear how failed and successful agent trajectories differ across reasoning, action selection, and environment feedback, which limits failure diagnosis and agent design.
```

### P4: This Paper and Scope

Purpose: convert the gap into a concrete paper.

Plan:

1. OBJECTIVE: `This paper presents/conducts/evaluates...`
2. SCOPE: studied systems, projects, models, languages, vulnerabilities, bugs, or tasks.
3. SCALE: numbers, time range, datasets, experiments, participants, or artifacts.
4. JUSTIFICATION: why this scope is appropriate.

Use `first` only if the manuscript can defend it. Prefer `systematic`, `large-scale`, `in-depth`, `developer-centered`, or `ecosystem-scale` when accurate.

### P5: RQs or Evaluation Goals

Purpose: make navigation clear.

Empirical pattern:

```text
Our study is guided by the following research questions:
RQ1: What is the overall landscape of [phenomenon]?
RQ2: What [patterns/root causes/categories] explain [phenomenon]?
RQ3: How do [systems/groups/strategies] differ in [metric/outcome]?
```

Method/tool pattern:

```text
We evaluate [tool/method] along three dimensions: effectiveness, efficiency, and generality.
```

Keep RQs parallel and map them to result sections.

### P6: Method and Findings Preview

Purpose: prove credibility without duplicating the method section.

Plan:

1. METHOD: collect/build/implement.
2. METHOD: filter/normalize/annotate/measure/evaluate.
3. FINDING: 2 to 4 strongest results, each paired with meaning.

Use specific numbers only if supplied by the paper.

### P7: Positioning and Contributions

Purpose: leave reviewers with the paper's package.

Plan:

1. POSITION: how this differs from closest work by object, data, method, granularity, or goal.
2. CONTRIBUTION bullets: 3 concrete, parallel bullets.

Contribution pattern:

```text
In summary, this paper makes the following contributions:
1. We [construct/propose/release] [artifact/method/dataset] ...
2. We [conduct/evaluate/analyze] [evidence] and find ...
3. We [distill/provide] [implications/guidelines/taxonomy] for ...
```

## Paper-Type Adaptations

- Empirical/measurement: emphasize RQs, dataset construction, coding/measurement, findings, implications.
- Method/tool/system: emphasize limitation, design insight, implementation, effectiveness, efficiency, ablation.
- Benchmark/dataset: emphasize need, construction pipeline, validation, metrics, baselines, reuse protocol.
- Security/testing: emphasize threat/failure model, risk scenario, affected scope, validation, false positives/negatives, mitigation.
- LLM/agent SE: define task and system boundaries carefully; distinguish model capability, agent orchestration, benchmark, prompt, tool, and environment feedback.

## Output Modes

When drafting from scratch:

1. Sentence-function outline.
2. Full Introduction draft.
3. Assumptions and missing facts.

When revising an existing Introduction:

1. Sentence-by-sentence function annotation.
2. Problems by severity: missing gap, weak consequence, unsupported novelty, unclear scope, weak contribution.
3. Revised Introduction or patch.

When teaching:

1. Paragraph blueprint.
2. Sentence roles.
3. Reusable sentence starters.
4. A short example tailored to the topic.
