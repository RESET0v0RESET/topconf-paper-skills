# Figures, Tables, Captions, and LaTeX Style

Use this reference when planning or revising visuals for ICSE/FSE/ASE/ISSTA-style papers.

## Observed ASE 2025 Visual Patterns

From a small sample of ASE 2025 accepted/preprint papers, common visual forms include:

- Methodology or pipeline diagrams near the approach/study-design section.
- Architecture and dependency graphs for tools, agents, program analysis, and supply-chain studies.
- Bar charts for comparisons across tools, models, repositories, categories, or RQs.
- Stacked bars for distributions and phase/action/category breakdowns.
- Violin/box plots for metric distributions and outcome differences.
- UpSet-style plots for overlap among models/tools/techniques.
- Time-series plots for longitudinal ecosystem behavior.
- Patch/code excerpts for repair, vulnerability, or reduction examples.
- Tables for datasets, benchmark composition, model settings, ablations, and result summaries.

The dominant style is not decorative. Figures are compact, evidence-focused, and captioned to explain what the reader should learn.

## Visual Design Rules

1. Choose the figure type from the claim:
   - Pipeline/architecture: method steps, data flow, component relation.
   - Bar/stacked bar: category comparison.
   - Box/violin: distribution.
   - Line/time series: temporal trend.
   - Scatter/heatmap: relation or matrix.
   - UpSet/Venn-like: overlap among techniques or tools.
   - Code/patch excerpt: concrete qualitative evidence.
2. Make color helpful but not essential. Use color-safe palettes, distinct markers/hatches, and readable grayscale contrast.
3. Use direct labels when possible. Keep legends short and terminology identical to the paper.
4. Use axis labels with units and sample sizes when relevant.
5. Use consistent ordering across related plots: same model/tool order, same category order, same color mapping.
6. Do not overload one figure with every metric. Split into subfigures or move details to a table.
7. Avoid PPT effects: gradients, shadows, large decorative icons, heavy borders, and unnecessary color blocks.
8. Prefer vector outputs (`pdf`, `svg`, `eps`) for plots and diagrams. Use high-resolution `png` only when raster is unavoidable.

## Caption Rules

Captions should identify the claim, not only name the object.

Weak:

```text
Fig. 3: Evaluation results.
```

Stronger:

```text
Fig. 3: Repair success by hunk proximity and model family. Bars report the percentage of correctly repaired bugs; error bars show bootstrap 95% confidence intervals.
```

Caption checklist:

- What is plotted?
- What are the units or denominator?
- What do colors/markers/subfigures mean?
- What condition, dataset, or model set is used?
- What caveat prevents misreading?

## Tables

Use `booktabs` style for ACM/IEEE LaTeX unless the venue template says otherwise:

```latex
\begin{table}
\caption{Dataset composition by project type.}
\label{tab:dataset}
\centering
\begin{tabular}{lrrr}
\toprule
Category & Projects & Instances & Bugs \\
\midrule
Libraries & 42 & 1,203 & 187 \\
Tools & 18 & 642 & 93 \\
\bottomrule
\end{tabular}
\end{table}
```

Table design rules:

- Put units in headers: `Time (s)`, `Cost (USD)`, `Accuracy (%)`.
- Align comparable numbers and use consistent precision.
- Report denominators for percentages.
- Avoid excessive vertical rules and dense grids.
- Use `table*` only when a table genuinely needs full width.
- Put detailed configuration in an appendix or artifact when it would crowd the main paper.

## LaTeX Float Rules

- Always use `\label{}` after `\caption{}`.
- Use semantic labels: `fig:method-overview`, `tab:dataset`, `rq:effectiveness`.
- Do not hard-code "Figure 3" in prose; use `Figure~\ref{fig:...}` or the venue's reference style.
- Check that every figure/table is referenced before or near its placement.
- Avoid `[H]` unless the template and final layout tolerate it.
- For ACM `acmart`, prefer `\Description{...}` for accessibility when required.
- Keep anonymous submissions free of artifact URLs, organization names, and repository paths that reveal authors unless the CFP explicitly permits anonymized artifacts.

## Figure Planning Matrix

Before drafting results, map each main claim:

| Claim | Best visual | Required data | Caption takeaway |
|---|---|---|---|
| Tool improves repair success | Bar/point plot with CI | Baseline, metric, tests | Shows effect size and uncertainty |
| Behavior differs across phases | Stacked bar/sequence plot | Phase labels, counts | Shows where the behavior concentrates |
| Dataset is diverse | Table + distribution plot | Sources, filters, categories | Shows coverage and limits |
| Approach scales | Line plot/log-scale plot | Size, runtime, memory | Shows trend and failure point |

If a figure does not support a claim or help answer an RQ, remove it or move it to supplemental material.
