# Paper Structure for Top SE Conferences

Use this reference when planning, restructuring, or diagnosing a full ICSE/FSE/ASE/ISSTA-style manuscript.

## Universal Submission Shape

Every strong top-SE paper should expose these links:

| Element | Must answer | Common failure |
|---|---|---|
| Problem | What concrete SE pain, uncertainty, risk, or limitation matters? | Opens with broad technology hype. |
| Gap | What is not known, not supported, or not measured? | Says only "little work has studied X." |
| Scope | What exact systems, projects, languages, models, data, tasks, or users are covered? | Scope arrives late or changes across sections. |
| Evidence | What data, experiments, artifacts, or analysis support the claim? | Abstract/conclusion claim has no table/figure/result. |
| Contribution | What reusable knowledge, method, artifact, dataset, taxonomy, benchmark, or finding remains? | Contribution bullets are just a table of contents. |
| Boundary | Where should readers not generalize? | Limitations are vague or hidden. |

## Empirical or Measurement Paper

Recommended section path:

1. Introduction
2. Background and motivation
3. Study design
4. Dataset construction and quality control
5. Results organized by RQ
6. Discussion and implications
7. Threats to validity
8. Related work
9. Data availability
10. Conclusion

Default RQ pattern:

- RQ1: Landscape, prevalence, scale, or overall properties.
- RQ2: Categories, patterns, root causes, or behavioral mechanisms.
- RQ3: Differences across groups, tools, languages, models, severity, time, or outcomes.
- Optional RQ4: Implications, mitigation, guidelines, or developer needs.

Good result structure:

```text
RQ1: [question]
Method. [only the details needed to understand this RQ]
Result. [main quantitative/qualitative result]
Interpretation. [what the result means]
Takeaway. [one sentence answer to the RQ]
```

Use takeaway boxes only if the venue/paper style has room and the boxes do not repeat the same prose.

## Method, Tool, or System Paper

Recommended section path:

1. Introduction
2. Motivation or motivating example
3. Design goals
4. Approach
5. Implementation
6. Evaluation setup
7. Results by evaluation question
8. Ablation/sensitivity/overhead if relevant
9. Discussion and threats
10. Related work
11. Artifact availability
12. Conclusion

Default evaluation questions:

- EQ1: Effectiveness on the target task.
- EQ2: Efficiency, scalability, or cost.
- EQ3: Generality across projects, languages, datasets, models, or scenarios.
- EQ4: Ablation or contribution of each component.
- EQ5: Qualitative cases, failure analysis, or usability if relevant.

Reviewers expect the method to be reproducible enough to implement or inspect. A high-level idea without implementation details usually reads as incomplete.

## Benchmark or Dataset Paper

Recommended section path:

1. Introduction
2. Need for the benchmark/dataset
3. Construction pipeline
4. Quality controls and validation
5. Tasks and metrics
6. Baseline results
7. Intended uses and non-uses
8. Threats and ethics/licensing
9. Artifact/data availability
10. Conclusion

Checklist:

- Define inclusion/exclusion criteria.
- Explain de-duplication, filtering, annotation, and validation.
- Report inter-annotator agreement when human labeling is used.
- Include baseline results to calibrate difficulty, not to oversell a method.
- State licenses, privacy, PII, and usage constraints.

## Security, Testing, or Program-Analysis Paper

Recommended section path:

1. Introduction with concrete risk or failure scenario.
2. Background/threat model/problem model.
3. Approach or study design.
4. Implementation details.
5. Dataset and experimental setup.
6. RQ/EQ results.
7. False positives/false negatives or failure modes.
8. Mitigations/implications.
9. Threats to validity.
10. Artifact availability.

Avoid vague security claims. Name the attacker/bug/failure model, assumptions, scope, and what the paper does not defend against.

## Contribution Bullets

Use 3 bullets unless the paper has a real fourth contribution. Make bullets parallel:

1. `We present/construct/release [artifact/method/dataset] that ...`
2. `We conduct/evaluate/analyze [evidence] and find ...`
3. `We distill/provide [implications/guidelines/taxonomy] for [audience/task].`

Bad contribution bullet:

```text
We introduce the background and evaluate our method.
```

Good contribution bullet:

```text
We construct HUNK4J, a benchmark of 372 real-world multi-hunk Java bugs, and use it to evaluate repair performance across model families and prompting strategies.
```

Use `first`, `largest`, or `comprehensive` only when the comparison basis is defensible and the manuscript can cite or explain it.

## Related Work

Related work should position, not dump citations.

Use buckets:

- Same object, different goal.
- Same goal, different object or data.
- Same method family, different evidence.
- Complementary studies or tools.

Sentence pattern:

```text
Prior work on [area] has shown [specific contribution]. However, these studies primarily focus on [covered scope], whereas our work examines [distinction]. Our findings complement this line by [specific added value].
```

## Discussion and Implications

A discussion section is useful when results need interpretation beyond RQ answers. It can include:

- Design implications for tool builders.
- Methodological implications for researchers.
- Operational implications for developers/maintainers.
- Security, safety, or ethics implications.
- Failure modes and why they matter.

Do not use discussion to introduce unsupported new claims.
