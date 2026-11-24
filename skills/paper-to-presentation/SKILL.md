---
name: paper-to-presentation
description: Read academic papers deeply and transform their arguments into evidence-grounded visual presentations. Use for paper explanation, equation walkthroughs, journal clubs, literature presentations, research talks, visual paper summaries, or requests to turn a paper into slides. Support reading-only, storyboard-only, presentation-only from verified notes, and end-to-end modes, especially for quantitative marketing, economics, and empirical social science.
---

# Paper to Presentation

## Operating defaults

- Select the requested mode: read, storyboard, present, or end-to-end. Do not produce a deck for a reading-only request.
- Default to detailed Chinese reading explanations, English slides, and bilingual speaker notes on EVERY slide: a complete English narration first, followed by its Chinese counterpart. Override only when the user requests a different language. Keep reusable workflow instructions in English. Treat the default blue theme as a default; an explicit palette request overrides it.
- Preserve original mathematical notation and important English technical terms.
- For an unspecified presentation brief, use a detailed learning presentation. Explain the technical core step by step: derivations for model papers, and design, estimands, specifications, and evidence for empirical papers. Set the slide count from the material, without a fixed page cap or a presumed 12-minute limit. When the user specifies a speaking time, create a focused main narrative and place supporting derivations in an appendix or a separate detailed version. State when the detailed version exceeds the requested time.
- Ask only for missing information that materially prevents useful work. Continue source inspection and reading independently. Do not require approval between ordinary stages; pause after a storyboard only if the user requests a checkpoint.
- Use available tools rather than assuming a particular model, connector, absolute path, API key, or institutional integration. Do not install software, connect accounts, publish, or modify this skill merely to read a paper.
- For file deliverables, follow the current environment's storage and artifact instructions. Read the applicable PDF, document, presentation, or visualization guidance before creating those artifacts.

- Read [references/user-requirements.md](references/user-requirements.md) before reading or presenting a paper. Treat its confirmed defaults as part of this workflow; the user's latest explicit instructions override them. Preserve the user's edits when revising a deck.

## 1. Establish the source

1. Prefer the supplied full text and appendices. Record title, authors, year, venue, DOI or source URL, version/date, access level, and materials actually inspected.
2. Resolve missing metadata through authoritative sources when tools permit. Prefer publisher metadata and author or institutional copies. Do not silently substitute another version; name differences and the version used.
3. Distinguish abstract-only access, partial text, full text, and full text with appendix. Never present unread material as inspected. If full text is unavailable, provide a clearly limited overview and request the missing source before claiming a complete reading or evidence-grounded deck.
4. Map sections and exhibits before extracting long text. Inspect rendered pages for equations, figures, tables, or scans that text extraction cannot preserve reliably. Use OCR only when necessary and flag uncertain symbols.
5. Record printed page and PDF page separately when they differ. Use section and exhibit identifiers when page numbering is unavailable. Never invent locators, quotations, references, or numerical results.

## 2. Build a paper map

Explain the following in plain language before technical detail:

- Research question and why it matters.
- Prior explanation or benchmark and the unresolved gap.
- Proposed mechanism, model, or identification approach.
- Setting, sample, units, time period, and studies.
- Main finding, magnitude where verified, contribution, and scope.

For an empirical or multi-study paper, read [references/empirical-papers.md](references/empirical-papers.md) and create a study map linking each study to its role. For theory, distinguish assumptions, propositions, and proof strategy. For methodological work, explain the problem, pipeline, validation, and conditions of use. Do not force every paper into a causal empirical template.

## 3. Maintain an evidence ledger

Create a compact ledger shared by the reading notes and the deck:

| Claim ID | Claim and attribution | Evidence and verified values | Required assumptions | Source locator | Inspection status and limitations |
| --- | --- | --- | --- | --- | --- |
| C1 | [Authors' finding, interpretation, or analyst inference] | [Table, figure, equation, proof, or passage] | [Conditions needed] | [Version; section; printed/PDF page; exhibit] | [Verified, partial, or unresolved] |

Assign stable IDs to substantive claims and reuse them in the storyboard and notes. Include units, denominators, sample restrictions, model columns, uncertainty intervals, and significance information when relevant. For empirical claims, also record the estimand or comparison, baseline, outcome scale, inference unit, and whether the value is reported or calculated. Do not infer an exact p-value or confidence interval from significance stars alone.

Separate the authors' statements, the evidence actually inspected, the assistant's interpretation, and speculative extensions. Distinguish association, causal effects, predictions, structural estimates, and theoretical implications. A mechanism consistent with evidence is not automatically an identified mechanism.

Keep original tables or figures when numerical reconstruction is unsupported. Do not treat good model fit or a non-significant pretrend test as proof of identification.

## 4. Explain the technical core

For each essential equation, follow this sequence:

1. State the problem the equation solves.
2. Define every symbol, index, unit, reference category, and domain.
3. Explain the role of each term.
4. Reproduce the equation faithfully and show the intermediate steps required to understand it.
5. Label supplemental derivations separately from derivations in the paper.
6. Give a small explicitly hypothetical numerical example when helpful.
7. Interpret parameters and marginal effects under the actual specification, including interactions, nonlinear links, transformations, and normalization.
8. State assumptions, limitations, and what changes when a condition fails.

For empirical work, follow references/empirical-papers.md. Identify assignment or exposure, comparison, outcome, estimand and target population, timing, inference unit, identification assumptions, and main threats. Explain how the reported evidence addresses each threat and what remains unresolved. Do not select an estimator merely because the paper's topic resembles a familiar design.

For predictive or structural work, explain the objective, estimation, validation, parameter interpretation, and counterfactual assumptions. For theory, separate intuition, formal statement, proof steps, and comparative statics.

When a derivation requires probability, integration, Bayesian updating, an identity, or a special function, introduce that prerequisite in plain Chinese and show the intermediate algebra. Distinguish a model assumption from a derived implication. Reproduce reported numerical comparisons from inputs through the final denominator, timing convention, and rounding. Do not skip steps merely because the source calls them standard. See the detailed teaching sequence in references/user-requirements.md.

End the reading with a few substantive limitations, transferable ideas, and unresolved questions. Relate them to the user's research only when there is a concrete connection; do not force relevance.

## 5. Design the visual argument

Use the verified reading as the content source. If existing notes are supplied, verify load-bearing claims against the paper before presenting them as established.

Record audience, purpose, duration including discussion, central takeaway, language, format, and available source assets. Distinguish learning material from a spoken research presentation. Attribute the paper to its authors and identify the user as presenter; label the presenter's critique and extensions.

Write a storyboard before slide bodies:

| Slide | Audience question | Assertion title | Primary exhibit | Claim IDs and source | Speaker notes and time |
| --- | --- | --- | --- | --- | --- |
| 1 | [Question] | [Evidence-bounded takeaway] | [Visual] | [C1; locator] | [Narrative and seconds] |

Read titles in order to check the argument. Use clear, numbered titles whose causal language matches the evidence. Prefer informative statements or descriptive academic titles over slogans; name heterogeneity and proposed mechanisms explicitly, without implying a mechanism was causally identified. For empirical decks, make the opening roadmap a concise, clickable English argument map, with only the paper's load-bearing nodes and short labels; follow the selection, layout, and wording guidance in references/user-requirements.md. Keep necessary nuance in a complete explanatory sentence. Give each slide one coherent teaching point. Combine adjacent setup, comparison, or result steps when they form a readable unit; avoid sparse slides that repeat the next page. Keep related evidence and its interpretation together, but split content that would crowd the page. Set the total from the argument and the user's requested density rather than a fixed slides-per-minute rule.

Choose a structure appropriate to the contribution:

- Empirical: question, early answer, setting/data, design, principal results, mechanism or heterogeneity, strongest threat, contribution and discussion.
- Multi-study: shared question and claim, followed by a compact design–result–limitation arc per study, then synthesis.
- Theory/model: question, setup, assumptions, core result, intuition, comparative statics, implications and boundaries.
- Method/framework: problem, pipeline overview, stages with a recurring roadmap, validation, limitations and applications.

In detailed mode, keep the essential reasoning in the main sequence: derivations for model papers; study design, comparison logic, coefficient interpretation, and result evidence for empirical papers. Group tightly related steps on one slide when legibility and the visual hierarchy allow it. Use an appendix for additional identities, full specifications, robustness, and anticipated questions. In timed-talk mode, move supporting derivations to the appendix to respect the speaking budget. Keep the main conclusion visible at the end of the main narrative.

## 6. Translate evidence into visuals

| Explanatory task | Preferred visual |
| --- | --- |
| Motivation or gap | Benchmark-versus-unresolved-question comparison |
| Assignment or experiment | Group and measurement timeline |
| Observational or quasi-experimental design | Sampling and treatment timeline, comparison logic, and main threat |
| Identification | Assignment schematic and comparison logic |
| Equation | Legible equation with progressive term highlighting and a symbol key |
| Model or method | Compact pipeline with the active stage highlighted |
| Results | Original exhibit or reproducible chart from verified values |
| Heterogeneity | Coefficient or subgroup comparison with available uncertainty |
| Mechanism | Diagram distinguishing hypothesized and tested paths |

Classify every visual as original evidence, reconstruction from reported values, conceptual schematic, or pedagogical simulation. Label schematics and simulations visibly. Record provenance for original and reconstructed exhibits.

Never fabricate data, precision, uncertainty bands, trajectories, or missing estimates. If digitizing a chart is useful and feasible, identify the values as approximate and document the extraction. Do not present approximate values as reported exact results.

Use image generation only for optional illustrative imagery, never for exact data charts, equations, or scientific diagrams. Use plotting or vector tools for precise visuals. Preserve axes, units, baselines, comparison groups, and uncertainty. Avoid decorative diagrams that imply unsupported causal paths.

Use progressive reveals only to explain a dependency, term, comparison, or stage. Use interactive controls for useful exploration, with assumptions and simulated quantities explicit. Ensure essential meaning also survives a static export.

## 7. Produce and verify the presentation

- Honor the requested format. Use the environment's presentation workflow for PPTX or Google Slides. Prefer editable source plus PDF where supported.
- Use Quarto/reveal.js for a requested browser-based academic deck when the toolchain is available. Do not assume the upstream repository's extensions or scripts are installed. Inspect official documentation if implementation behavior is uncertain.
- If the preferred renderer is unavailable, disclose that constraint and use a supported format or deliver verified content and source. Never label unrendered source as a completed, tested deck.
- Put evidence, key findings, implications, and necessary formal statements on slides. Use complete, clear explanations for findings and figure interpretations instead of slogan-like fragments. Put detailed narration, intuition, transitions, and anticipated caveats in bilingual notes. Keep caveats necessary to interpret a claim visible on the slide.
- Preserve exact provenance in the evidence index and speaker notes. Do not display internal claim IDs or locator strings such as C4–C5 · §3, pp.87–88 on audience slides. Retain concise human-readable author/year attribution where needed for borrowed exhibits and a formal references appendix. Verify bibliographic metadata rather than generating missing fields from memory.
- Apply the default blue theme unless the user specifies another palette. Preserve Avenir Next with portable fallbacks, single-line cover and closing titles, section/subsection numbering, and permanent per-slide navigation specified in references/user-requirements.md.
- Keep the title at the top. Vertically center the grouped body between title and footer, as in PowerPoint's Align Middle, without moving the title or navigation. Justify substantial prose paragraphs across the available width; leave tables, equations, narrow labels, and short callouts naturally aligned. Verify this in interactive HTML and the exported PDF. Use a single consistent page count including the appendix.
- Render and inspect every slide, including reveal states when used. Check clipping, overlap, readable figures, contrast, mathematical rendering, attribution, and appendix links. Revise or split crowded slides instead of shrinking everything.
- Verify all principal numerical claims and formulas against the ledger. Check that conclusions do not exceed the evidence.
- Inspect the final PDF separately when exported. Confirm slides with animations retain their full meaning and essential assets. Test offline operation before claiming a deck is offline-ready.
- Report verification actually performed and any unresolved limitations. Do not equate a successful render with visual or scientific correctness.

## Rendering workflow

Before creating presentation source, rendering, previewing, exporting PDF, or answering how to render, read [references/rendering.md](references/rendering.md). Use [assets/deck-template.qmd](assets/deck-template.qmd) as the built-in Quarto reveal.js starting point when that route is appropriate. Follow its source-authoring, local preview, speaker-view, PDF export, validation, and missing-tool procedures. Keep storyboard-only requests unrendered. Report separately what was authored, rendered, exported, and inspected.

## Deliverables and completion

Scale output to the requested mode:

- Read: source/coverage note, paper map, evidence ledger, technical explanation, and critical discussion.
- Storyboard: verified source/coverage note, narrative brief, slide table, visual specifications, and appendix plan.
- Present: requested rendered deck where supported, editable source, speaker notes, and a compact evidence index. Include PDF when requested or useful and feasible.
- End-to-end: combine the reading deliverables and presentation deliverables without repeating long content in chat.

Do not create empty deliverables or claim unsupported outputs. Reuse verified work within the session; revisit the paper only when additional detail, a changed version, or a contradiction requires it. End with a concise outcome, available artifacts, and material limitations.

## Example invocations

- "Use $paper-to-presentation to explain this paper in Chinese. Focus on identification and derive the main equations. Do not make slides yet."
- "Use $paper-to-presentation to prepare a detailed learning presentation. Explain the paper in Chinese, derive its equations step by step, and create blue English slides with English notes above Chinese notes, numbered titles, page counts, and clickable navigation."
- "Use $paper-to-presentation in end-to-end mode. Explain the paper in Chinese, then create a 12-minute English presentation with bilingual notes (English first). Keep full derivations in the appendix and make findings, implications, and limitations explicit."
- "Use $paper-to-presentation to produce only a storyboard for this paper, then wait for my feedback before rendering the deck."
- "Use $paper-to-presentation in end-to-end mode for this empirical paper. Explain the research design and each study in Chinese; then create a detailed blue HTML deck with English slides, English-first/Chinese-second notes, verified results, identification threats, implications, and boundaries. Use the empirical template and my reference slides for visual style only."

## Attribution

Adapted at the workflow level from Eric Luo's reading-papers and research-talk modules in https://github.com/ericluo04/claude-academic-workflow. This independently written skill adds a shared evidence ledger, bilingual output controls, multiple reading/presentation modes, visual provenance labels, and environment-aware artifact production. No upstream scripts, themes, fonts, or other assets are bundled. Consult the upstream license before copying any upstream implementation.
