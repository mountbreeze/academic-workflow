# Rendering a Paper Presentation

## Contents
1. Select a route
2. Build the source from the approved storyboard
3. Render and preview with Quarto
4. Export a PDF
5. Validate and deliver
6. Recover from missing tools

## 1. Select a route

Honor the requested format. For an academic browser presentation, default to Quarto reveal.js when available. For PPTX or Google Slides, use the environment's corresponding presentation workflow and its renderer. Do not claim that a reveal.js HTML file is an editable PowerPoint file.

Distinguish three stages:
- Storyboard: slide plan and notes, with no rendered deck.
- Source: an authored .qmd and its local assets.
- Rendered presentation: generated HTML or another requested presentation artifact, inspected after rendering.

A request for instructions or for this skill to gain rendering support does not by itself authorize turning a previously paused storyboard into a full deck. Provide the instructions and update the workflow. When the user asks to build the deck, complete source authoring and rendering autonomously where tools permit.

## 2. Build the source from the approved storyboard

Copy assets/deck-template.qmd from this skill into a new presentation project as deck.qmd. This uses Quarto's built-in revealjs format, with no upstream custom extension required.

Create the actual main slides and appendix from the approved plan. Replace all instructional content in the template. Preserve the main-slide timing budget. Include English slide text and the requested language of speaker notes inside each slide's notes div.

Place original or reproducible exhibits in assets/. Keep a compact evidence-index.md linking slide numbers to claim IDs, original exhibit numbers, printed and PDF pages, and visual provenance. Preserve chart-generation code and exact inputs when charts are reconstructed.

Use Markdown headings beginning with ## for slides. Add stable heading IDs for appendix navigation. Add a source footer to every substantive slide. Keep citations short but identify the paper, page/exhibit, and claim IDs. A verified .bib file is optional for a single-paper talk; if used, configure bibliography and validate its metadata.

Keep notes inside:
```markdown
::: {.notes}
Write the speaker's actual narration here.
:::
```

Keep a separate speaker-notes.md in the requested language as a fallback. Notes embedded in HTML can be read by anyone who receives the source or HTML, even though they are absent from the audience slide view.

Use local figures and static exports of essential interactive exhibits. Do not rely on an online widget for the only representation of a result. Use compatible LaTeX math in the default KaTeX route. For advanced MathJax-only macros, select MathJax deliberately, document the dependency, and test offline behavior separately.

## 3. Render and preview with Quarto

Check the environment first:
```bash
quarto --version
quarto check
```

Install Quarto from its official installer only if authorized and needed:
https://quarto.org/docs/get-started/

In the directory containing deck.qmd, run:
```bash
quarto render deck.qmd --to revealjs
quarto preview deck.qmd --to revealjs
```

The render command creates deck.html. Preview serves the presentation locally and refreshes after edits. Open the preview URL printed by Quarto. Press S to open speaker view and allow its popup if prompted. Use the local preview for rehearsal because browser security can restrict speaker view under file URLs.

The template requests embedded resources and self-contained math. Rendering can still require a network to fetch dependencies. Embedding is a configuration request, not proof that every dependency or presenter feature works offline. Test the actual delivered HTML with the network disabled before labeling it offline-ready.

Do not render a reveal.js presentation with --to pdf and assume equivalent slides. That selects another output route rather than exporting the rendered slide layout.

## 4. Export a PDF

Use the rendered reveal.js print view in Chrome or Chromium:
1. Open Print to PDF from the presentation menu, or add ?print-pdf to the deck URL. Use &print-pdf if a query string already exists, before any # fragment.
2. Wait for fonts, figures, and math to finish loading.
3. Open the browser print dialog.
4. Select Save as PDF, landscape, no margins, and background graphics.
5. Save deck.pdf and inspect it separately.

The template sets pdf-separate-fragments: false so a handout normally shows the final state of each slide. Verify this in the exported file. Overlaid exhibits or mutually exclusive animation states can collide in print; author static alternatives where needed.

Keep Chinese notes in the separate notes file by default. Do not assume that an audience PDF includes presenter notes. If the user requests a notes PDF, configure and inspect that version separately using the installed Quarto version's documented options.

Use a supported automated browser/export route if one is already available, but inspect the generated PDF and record the actual tool/version. Do not invent an automatic export command or silently install a new dependency.

## 5. Validate and deliver

After each substantive edit, render and inspect:
- Every main and appendix slide at presentation size.
- All reveal states used to explain reasoning.
- Formula rendering and symbol definitions.
- Missing images, overlap, clipping, contrast, and small source labels.
- Numerical values, units, uncertainty, axes, and claim IDs against the evidence index.
- The 12-minute narration budget or the user's specified duration.
- Speaker-view notes, appendix navigation, and essential offline behavior when requested.
- The final PDF, including complete exhibit states and appendix pages.

Do not report an automated fit, staging, or offline gate as passed unless the relevant tool was actually run. No custom validation scripts are bundled with this skill. Use available browser inspection tools or manual review and report the scope precisely.

Deliver the inspected HTML, editable .qmd, required local assets if not embedded, separate speaker notes, evidence index, and PDF when successfully exported. Preserve the project in the environment's required durable storage. Do not publish to GitHub Pages or upload the paper itself merely because the skill is hosted on GitHub.

## 6. Recover from missing tools

If Quarto is absent or execution is blocked:
- Continue preparing verified source and figures when possible.
- State that rendering has not been completed.
- Offer the documented local commands above, or use the user's requested supported presentation renderer.
- Never describe a storyboard or unrendered .qmd as a completed presentation.

## Official references

- https://quarto.org/docs/presentations/revealjs/
- https://quarto.org/docs/presentations/revealjs/presenting.html
- https://quarto.org/docs/reference/formats/presentations/revealjs
- https://revealjs.com/pdf-export/
