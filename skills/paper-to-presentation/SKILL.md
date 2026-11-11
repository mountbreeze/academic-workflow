---
name: paper-to-presentation
description: Read academic papers deeply and transform their arguments into evidence-grounded visual presentations. Use for paper explanation, equation walkthroughs, journal clubs, literature presentations, research talks, visual paper summaries, or requests to turn a paper into slides. Support reading-only, storyboard-only, presentation-only from verified notes, and end-to-end modes, especially for quantitative marketing, economics, and empirical social science.
---

# Paper to Presentation

## Operating defaults

- Select the requested mode: read, storyboard, present, or end-to-end. Do not produce a deck for a reading-only request.
- Write reading explanations in the user's conversation language. Default to English slides and speaker notes in the conversation language. Override either when requested. Keep this skill and its reusable templates in English.
- Preserve original mathematical notation and important English technical terms.
- For an unspecified presentation brief, state provisional defaults: a 12-minute graduate journal-club talk, 8–10 main slides plus a focused appendix, for an audience familiar with basic statistics. Use a different brief when available in the conversation.
- Ask only for missing information that materially prevents useful work. Continue source inspection and reading independently. Do not require approval between ordinary stages; pause after a storyboard only if the user requests a checkpoint.
- Use available tools rather than assuming a particular model, connector, absolute path, API key, or institutional integration. Do not install software, connect accounts, publish, or modify this skill merely to read a paper.
- For file deliverables, follow the current environment's storage and artifact instructions. Read the applicable PDF, document, presentation, or visualization guidance before creating those artifacts.

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

For a multi-study paper, create a study map linking each study to its role. For theory, distinguish assumptions, propositions, and proof strategy. For methodological work, explain the problem, pipeline, validation, and conditions of use. Do not force every paper into a causal empirical template.

## 3. Maintain an evidence ledger

Create a compact ledger shared by the reading notes and the deck:

| Claim ID | Claim and attribution | Evidence and verified values | Required assumptions | Source locator | Inspection status and limitations |
| --- | --- | --- | --- | --- | --- |
| C1 | [Authors' finding, interpretation, or analyst inference] | [Table, figure, equation, proof, or passage] | [Conditions needed] | [Version; section; printed/PDF page; exhibit] | [Verified, partial, or unresolved] |

Assign stable IDs to substantive claims and reuse them in the storyboard and notes. Include units, denominators, sample restrictions, model columns, uncertainty intervals, and significance information when relevant. Do not infer an exact p-value or confidence interval from significance stars alone.

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

For empirical work, identify assignment, treatment/exposure, comparison, outcome, estimand and target population, timing, inference unit, identification assumptions, and main threats. Explain how the reported evidence addresses each threat and what remains unresolved. Do not select an estimator merely because the paper's topic resembles a familiar design.

For predictive or structural work, explain the objective, estimation, validation, parameter interpretation, and counterfactual assumptions. For theory, separate intuition, formal statement, proof steps, and comparative statics.

End the reading with a few substantive limitations, transferable ideas, and unresolved questions. Relate them to the user's research only when there is a concrete connection; do not force relevance.

## 5. Design the visual argument

Use the verified reading as the content source. If existing notes are supplied, verify load-bearing claims against the paper before presenting them as established.

Record audience, purpose, duration including discussion, central takeaway, language, format, and available source assets. Distinguish learning material from a spoken research presentation. Attribute the paper to its authors and identify the user as presenter; label the presenter's critique and extensions.

Write a storyboard before slide bodies:

| Slide | Audience question | Assertion title | Primary exhibit | Claim IDs and source | Speaker notes and time |
| --- | --- | --- | --- | --- | --- |
| 1 | [Question] | [Evidence-bounded takeaway] | [Visual] | [C1; locator] | [Narrative and seconds] |

Read titles in order to check the argument. Prefer short assertion titles whose causal language matches the evidence. Use one primary intellectual task per slide. Adapt the number of slides to the actual time needed for complex exhibits rather than applying a fixed slides-per-minute rule.

Choose a structure appropriate to the contribution:

- Empirical: question, early answer, setting/data, design, principal results, mechanism or heterogeneity, strongest threat, contribution and discussion.
- Multi-study: shared question and claim, followed by a compact design–result–limitation arc per study, then synthesis.
- Theory/model: question, setup, assumptions, core result, intuition, comparative statics, implications and boundaries.
- Method/framework: problem, pipeline overview, stages with a recurring roadmap, validation, limitations and applications.

Build an appendix for technical derivations, full specifications, robustness, and anticipated questions. Keep the main conclusion visible at the end of the main narrative.

## 6. Translate evidence into visuals

| Explanatory task | Preferred visual |
| --- | --- |
| Motivation or gap | Benchmark-versus-unresolved-question comparison |
| Assignment or experiment | Group and measurement timeline |
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
- Put concise evidence and necessary formal statements on slides. Put explanation, intuition, transitions, and anticipated caveats in speaker notes. Keep caveats necessary to interpret a claim visible on the slide as well.
- Cite borrowed claims and exhibits on the relevant slide. Verify bibliographic metadata; do not generate missing fields from memory. Use an attribution line for reproduced or adapted exhibits.
- Render and inspect every slide, including reveal states when used. Check clipping, overlap, readable figures, contrast, mathematical rendering, attribution, and appendix links. Revise or split crowded slides instead of shrinking everything.
- Verify all principal numerical claims and formulas against the ledger. Check that conclusions do not exceed the evidence.
- Inspect the final PDF separately when exported. Confirm slides with animations retain their full meaning and essential assets. Test offline operation before claiming a deck is offline-ready.
- Report verification actually performed and any unresolved limitations. Do not equate a successful render with visual or scientific correctness.

## Deliverables and completion

Scale output to the requested mode:

- Read: source/coverage note, paper map, evidence ledger, technical explanation, and critical discussion.
- Storyboard: verified source/coverage note, narrative brief, slide table, visual specifications, and appendix plan.
- Present: requested rendered deck where supported, editable source, speaker notes, and a compact evidence index. Include PDF when requested or useful and feasible.
- End-to-end: combine the reading deliverables and presentation deliverables without repeating long content in chat.

Do not create empty deliverables or claim unsupported outputs. Reuse verified work within the session; revisit the paper only when additional detail, a changed version, or a contradiction requires it. End with a concise outcome, available artifacts, and material limitations.

## Example invocations

- "Use $paper-to-presentation to explain this paper in Chinese. Focus on identification and derive the main equations. Do not make slides yet."
- "Use $paper-to-presentation to turn this paper into a 12-minute journal-club presentation. Use English slides and Chinese speaker notes. Include a visual explanation of the design and an evidence-linked appendix."
- "Use $paper-to-presentation in end-to-end mode. Explain the paper in Chinese, then create an English visual presentation with English speaker notes. Label simulations and keep empirical results traceable to the paper."
- "Use $paper-to-presentation to produce only a storyboard for this paper, then wait for my feedback before rendering the deck."

## Attribution

Adapted at the workflow level from Eric Luo's reading-papers and research-talk modules in https://github.com/ericluo04/claude-academic-workflow. This independently written skill adds a shared evidence ledger, bilingual output controls, multiple reading/presentation modes, visual provenance labels, and environment-aware artifact production. No upstream scripts, themes, fonts, or other assets are bundled. Consult the upstream license before copying any upstream implementation.
