# Writing Patterns

Use this reference for English phrasing, abstract/introduction/conclusion moves, and reviewer-facing language.

## Abstract Pattern

```text
[Problem/object] has become increasingly important for [stakeholders/tasks].
However, [specific limitation/gap] remains unclear or unsupported.
This paper [presents/conducts/evaluates] [method/study/tool] to [objective].
We analyze/evaluate [data scale, systems, projects, models, tasks] using [method].
Our results show that [finding 1] and [finding 2].
These findings suggest/provide [implication or reusable contribution].
```

Keep the abstract grounded in the paper's strongest evidence. Do not put contribution bullets in the abstract unless the style is common for the venue/paper and the text remains concise.

## Introduction Move Sequence

Default sequence:

`importance -> object -> concrete use/risk -> prior focus -> gap -> consequence -> this paper -> RQs/EQs -> method -> findings -> contributions`

Useful sentence roles:

- Background: `Recent advances in [area] have enabled [capability].`
- Object: `[Object] refers to [definition].`
- Scale: `[Number/source] indicates that [object] is widely used or practically relevant.`
- Problem: `Despite [value/adoption], [problem] remains poorly understood.`
- Prior: `Existing work has primarily focused on [covered scope].`
- Gap: `However, it remains unclear how/why/to what extent [specific unknown].`
- Consequence: `This gap limits [developer/researcher/tool-builder action].`
- Objective: `This paper presents/conducts [study/tool/analysis].`
- Scope: `We focus on [scope] because [reason].`
- Method: `To answer these questions, we [collect/analyze/measure/evaluate].`
- Finding: `Our findings show/reveal/indicate that [result], suggesting [meaning].`
- Contribution: `In summary, this paper makes the following contributions.`

## RQ Wording

Prefer specific `what` and `how` questions:

- `RQ1: What is the prevalence and distribution of [phenomenon]?`
- `RQ2: What categories or root causes explain [phenomenon]?`
- `RQ3: How do [groups/tools/models] differ in [metric/outcome]?`
- `RQ4: What implications do these findings have for [audience]?`

Avoid vague yes/no RQs unless a controlled hypothesis test is central.

## Result Phrasing

Good:

```text
The results show that [method] improves [metric] by [effect size] over [baseline] on [dataset], with [condition/caveat].
This improvement is concentrated in [subset], suggesting that [mechanism].
```

Good for qualitative findings:

```text
We identify [n] recurring patterns. The most frequent pattern, [category], accounts for [x%] of cases and typically arises when [condition].
```

Avoid:

- `The results fully prove that...`
- `Our method significantly outperforms all existing methods...` unless statistical and experimental conditions justify it.
- `This has great practical significance.`
- `The experiment is perfect/comprehensive.`

## Contribution Phrasing

Use concrete nouns:

- `benchmark`
- `dataset`
- `taxonomy`
- `measurement framework`
- `analysis pipeline`
- `tool`
- `evaluation protocol`
- `replication package`
- `guidelines`

Contribution examples:

```text
We construct [dataset], containing [scale], and document its collection and validation pipeline.
We design [method/tool], which [mechanism] to address [limitation].
We conduct [evaluation/study] across [scope] and find [main result].
We distill [n] implications for [audience].
```

## Conclusion Pattern

Use 1 to 2 paragraphs for most top-SE papers:

```text
This paper [presented/conducted] [work] to address [problem]. By [evidence/method], we showed/found that [finding 1] and [finding 2]. We also [artifact/taxonomy/guidelines], which [reuse/value].

These results highlight [broader implication] for [audience]. Future work should [specific next step tied to limitation]. Overall, [strong but grounded final takeaway].
```

Use the focused `se-topconf-conclusion` skill when conclusion work is the main task.

## Tone Guardrails

Prefer:

- `we find`
- `we observe`
- `we show`
- `our results indicate`
- `this suggests`
- `this highlights`
- `we provide evidence that`
- `we release`
- `we make available`

Use with care:

- `first`
- `novel`
- `comprehensive`
- `large-scale`
- `state-of-the-art`
- `significant`
- `robust`

Delete or rewrite:

- `with the rapid development of`
- `has attracted widespread attention`
- `great significance`
- `fills the blank`
- `perfectly solves`
- `fully proves`
- `obvious advantages`
