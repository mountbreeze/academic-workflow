# Confirmed reading and presentation requirements

Apply these defaults to future papers. Let the user's current task override any default. Use the approved Fader–Hardie revision as a style and teaching reference, without copying its results, equations, 46-slide count, or subject-specific structure into unrelated papers. For empirical papers, also use the visual preferences below without transferring content or numerical results from any reference deck.

## 1. Select the requested scope

- Support reading-only, individual-equation explanation, storyboard-only, deck revision, presentation-only from verified notes, and end-to-end work.
- Do not produce slides when the user asks only to understand a paper.
- Default to a detailed learning deck when presentation duration is unspecified. Let content determine page count.
- For an explicitly timed presentation, budget actual narration and exhibit explanation. Keep a focused main deck and a linked appendix, or provide a separate detailed version when useful.
- Reuse verified session work. Preserve user edits in an existing source and retain a backup before restructuring.

## 2. Teach the paper in Chinese

Start with the practical or theoretical problem. Explain what the usual benchmark does, why its assumptions matter, and exactly where the paper changes the calculation or interpretation. For papers without a benchmark formula, explain the prior approach or prevailing explanation.

Build understanding in this order where applicable:

1. Research question, importance, prior literature, unresolved gap, and contribution.
2. Definitions and the timing or unit of analysis.
3. Benchmark method and assumptions, with a small example.
4. Evidence or logic showing the benchmark's problem.
5. Proposed model/design, its assumptions, and what those assumptions rule out.
6. Technical derivations or identification logic, with intermediate steps.
7. Main findings, magnitudes, robustness, and interpretation.
8. Managerial/theoretical implications, limitations, and unresolved questions.

Use plain Chinese while preserving important English technical terms and original mathematical notation. Separate author claims, mathematical deductions, empirical evidence, explanatory examples, and the presenter's extensions.

## 3. Explain mathematics from the prerequisites

For each central expression:

- State what question it answers.
- Define every symbol, subscript, domain, unit, time index, conditioning event, and reference category.
- Explain prerequisites such as probability versus density, conditional probability, Bayes' rule, integration as weighted averaging, discounting, geometric-series sums, or derivatives before using them.
- Show substitutions, exponent manipulations, cancellations, changes of variable, boundary conditions, and summation-index changes. Avoid jumping directly from the original expression to a special-function answer.
- Introduce special functions as computational notation for the relevant integral or series, when that interpretation is valid.
- Explain the economic/statistical meaning after the algebra.
- Give a clearly labeled hypothetical numerical example when useful and connect it to the formula.
- Distinguish assumptions from derived results, a changed belief from changed behavior, and observed patterns from identified causal effects.
- For nonlinear functions, explain why averaging inputs can differ from averaging outputs where relevant.
- For elasticities, separate relative changes from percentage-point changes and local approximations from finite changes.

For numerical headline results, reconstruct the complete calculation: inputs, subgroup weights/counts, conditional quantities, intermediate totals, discounting/timing, unrounded calculations, and the final comparison denominator. Label model-based illustrations as such. Do not turn an example's error percentage into a universal empirical claim.

## 4. Organize the presentation around explanation

Default to English audience-facing slides and one primary intellectual step per page. In detailed mode, keep the important derivation steps in the main deck rather than hiding the entire explanation in an appendix.

For a model/method paper, consider this sequence:
- Conventional calculation or benchmark.
- Why aggregate summaries or benchmark assumptions can mislead.
- A complete worked numerical comparison.
- Proposed model and explicit assumptions.
- Definitions, prerequisite tools, and progressive derivation.
- Verified numerical example and interpretable visualizations.
- Key findings.
- Managerial, theoretical, or methodological implications.
- Scope, limitations, clear conclusion, and a technical/reference appendix.

Adapt the order to the paper. An empirical study needs its setting, sample and measurement, estimand or claim type, comparison logic, identification or validity threats, and result evidence. In a multi-study paper, show each study's distinct role before synthesizing. Do not manufacture an irrelevant benchmark or force every paper into a causal design.

## 5. Write findings and implications substantively

Include audience-visible findings and implications, not only notes about them.

- Write a synthesis of the paper's substantive findings, explaining mechanisms, magnitudes, and conditions.
- Write managerial implications as concrete consequences for measurement, valuation, targeting, or decisions, conditional on the evidence.
- Write theoretical/methodological implications separately when they require different reasoning.
- Identify which statements come from the authors and which are the presenter's interpretation or extension.
- Explain what the evidence does and does not establish. Model comparative statics do not establish campaign effects or return on investment.
- Use complete explanatory sentences under figures and in the conclusion. Longer clear sentences are preferable to slogan-like fragments.
- Replace phrases such as "Similar means. Different errors." with a statement explaining the comparison, its verified magnitudes, and the interpretation.
- Do not copy a narrow paper's specific percentages or management advice to another paper.

## 6. Use bilingual speaker notes on every slide

Include notes on the cover, roadmap, every technical page, findings, implications, conclusion, appendix, and references.

Use this exact language order:

```markdown
::: {.notes}
**English**

A complete, natural English narration for this slide.

**中文**

对应的完整中文讲解。
:::
```

Make the two versions equivalent in meaning. Include actual narration, explanation of figures and formulas, transitions, and relevant qualifications. Do not use a one-line placeholder, merely restate the title, or provide Chinese alone. Keep citations and internal evidence IDs in the notes when useful. Also export a separate speaker-notes.md with the same page order and language order. Match English narration to the speaking budget for timed talks.

## 7. Apply the confirmed visual style

- Use a restrained blue academic theme with a very light background, dark blue headings, blue emphasis, and consistent chart colors.
- For empirical decks, favor clear section hierarchy, generous and balanced whitespace, timelines and comparison diagrams, focused result charts, and selective highlighting of estimates or table cells. The provided example decks are visual references only: do not import their claims, values, graphics, or compact five-page density into another paper. An HTML learning deck may use more slides and larger exhibits.
- Prefer Avenir Next on macOS, with Helvetica Neue and Arial fallbacks. Use an available consistent alternative if necessary. Keep equations in suitable math fonts and ensure Chinese notes render.
- Keep the cover's main title on one line. Keep the main closing title on one line as well. Shorten or rephrase an overlong title before reducing it below readable size.
- Retain paper title, verified authors/venue/year, and the presenter's name. Do not invent the presenter's identity if unknown.
- Omit generic cover descriptions such as "A paper discussion with step-by-step derivations."
- Do not put internal evidence labels or dense locator strings such as "C4–C5 · §3, pp.87–88" on audience slides. Preserve full traceability in notes and evidence-index.md, plus formal references. Keep essential exhibit attribution.
- Use informative titles and complete explanatory figure interpretations. Avoid oversized slogan bands that crowd a chart.
- Preserve native editable LaTeX formulas. Do not turn formulas into screenshots merely to control layout.
- Add parameter-distribution or sensitivity visualizations when central to understanding a model. For a probability mixture model, show meaningful parameter contrasts and, when useful, comparisons holding the mean fixed. This is a conditional requirement, not a mandate to add alpha/beta charts to every paper.
- Label density versus probability, simulation versus data, normalization, clipping, and model assumptions where relevant. Pair useful interactive controls with a meaningful static export.

## 8. Provide Beamer-like navigation

- Number content headings by section and subsection (1.1, 1.2, 2.1, ...). Use A.1, A.2, ... in the appendix. Leave the cover unnumbered.
- Include a linked roadmap near the start.
- Put a readable current-page / total-pages indicator on every slide, including cover and appendix. Use one total for the delivered deck.
- Provide permanent clickable previous/next slide links, contents, chapter starts, and appendix navigation on every page.
- Keep navigation visible immediately on entering a slide. Never place it inside incremental fragment wrappers.
- Use stable IDs. Ensure navigation skips reveal fragments and reaches the intended slide, while keyboard fragment progression can still support step-by-step explanations.
- Avoid duplicate page counters, stale hard-coded totals, or a counter restarting unexpectedly at the appendix.
- Keep footers outside content and test content clearance. Preserve functional internal links in PDF where the exporter supports them.
- Use equivalent slide hyperlinks and notes when the requested output is PPTX.

## 9. Verify and deliver

Check:
- Source coverage and all principal numbers/equations against the evidence ledger.
- English-first/Chinese-second notes on every page.
- Key findings and implications are visible and clearly expressed.
- Single-line cover and closing titles, consistent heading numbering, exact page count, and absence of internal locator clutter.
- All navigation routes, including initial page state and appendix return links.
- Every rendered slide and relevant reveal states for clipping, overlap, mathematical errors, chart readability, and footer clearance.
- Static PDF independently for page count, final-state exhibits, formula rendering, and link destinations.
- Offline assets only when offline readiness is claimed.

Deliver the rendered deck, editable source, local dependencies, bilingual notes, evidence index, and inspected PDF when feasible or requested. Follow the active environment's durable-saving rules. For an externally Git-backed project, keep the source in that project rather than duplicating it to unrelated storage. Preserve license/attribution for borrowed tooling. Do not upload copyrighted paper PDFs or private project material to a public repository merely to store the workflow.
