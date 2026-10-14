---
name: paper-ppt-outline
description: Turn an academic paper, paper-reading note, or literature summary into a concise Chinese slide outline for a research presentation. Use for 组会提纲, 汇报提纲, slide bullets, and presentation-ready Markdown; do not use to build a finished PPTX.
---

# Paper PPT Outline

Create a speaker-facing Chinese Markdown outline for presenting one academic paper. The outline should make the paper's argument, method, evidence, and limitations easy to explain aloud; it is not a section-by-section paper summary.

## Source handling

Prefer the most structured source available:

1. An existing detailed reading note
2. Extracted paper text
3. The paper PDF

When a note is available, compress it instead of re-reading the paper from scratch. Keep the original source untouched and save the outline as a separate Markdown file. If information is absent or ambiguous, say so rather than inferring it.

## Narrative structure

Adapt the slide count to the paper, but normally organize the presentation as:

1. Paper information and one-sentence positioning
2. Background and practical motivation
3. Research gap and its consequence
4. Contributions, each mapped to a gap
5. Method overview
6. Method stages in execution order
7. Experimental setup: research questions, data, metrics, and comparable baselines
8. Results organized by research question
9. Conclusion and evidence limits
10. Optional research implications or open questions

Make the method the densest section. Introduce the complete pipeline before its components. For each core component, explain its role in the end-to-end pipeline, why a direct or prior approach is insufficient, its inputs and outputs, its intermediate artifacts, and any feedback, verification, memory, or iteration mechanism. Separate conceptual contributions from implementation support.

Organize empirical claims as an evidence chain:

```text
paper claim -> RQ / table / figure -> concise takeaway -> mechanism interpretation -> evidence boundary
```

Keep ablations, robustness, generalization, cost, and case studies with the research question they address. Compare like with like; identify differences in backbone, data split, or evaluation setting before making ranking claims.

## Slide writing

- Write in Chinese with short, speakable bullets.
- Use a conclusion, question, or mechanism as each slide title. Avoid page numbers and bare labels such as `方法`, `实验`, or `结果` when a concrete title is possible.
- Put the takeaway first, then source-grounded evidence, then a brief mechanism explanation or caveat.
- Retain only key formulas, numbers, tables, and figures needed to support a claim. Cite the original table, figure, or page when that information is available.
- Use compact Markdown tables for comparable experimental results. State the benchmark/split, metric, and comparison target alongside numerical claims.
- Distinguish paper evidence from the presenter's interpretation. Use clear caveats such as `论文没有给出`, `证据不足`, or `这里只能推测` where needed.
- Preserve explicitly supplied presenter notes, questions, and possible extensions as separate `研究备注` callouts; do not present them as paper findings.
- Avoid promotional language and claims stronger than the cited evidence supports.

## Formulas

Use inline math for short expressions and display math for standalone equations. After every key equation, explain what it computes, where it occurs in the pipeline, and all symbols that could otherwise be ambiguous. If the paper omits an implementation detail, identify the omission.

```markdown
$$
<formula>
$$

| 符号 | 含义 | 作用 |
|---|---|---|
| $x$ | ... | ... |
```

## Final check

Before delivering the outline, verify that:

- It is separate from the original note and has no duplicated or truncated text.
- The paper information, task, gap, contribution, method, experimental setup, results, and conclusion are all present when supported by the source.
- Method stages follow the paper's execution order and receive adequate space.
- Each major result answers a stated research question and includes its evidence boundary.
- Slide headings are audience-facing claims, questions, or mechanisms rather than navigation labels.
- Personal interpretation and missing information are explicitly labeled.
