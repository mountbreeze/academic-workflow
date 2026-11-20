# Empirical papers: reading and presentation guide

Read this reference for experiments, quasi-experiments, observational studies, surveys, scale development, predictive studies, and papers combining several designs. Use only the sections that fit the actual paper. A reported regression is not, by itself, a causal design.

## 1. Classify the evidence before explaining it

Identify the paper's main inferential task: causal estimation, descriptive association, prediction, measurement/construct validation, mechanism probing, or a combination. Name each study's task separately. Do not let an experiment in one study confer causal interpretation on an observational result in another.

Create a compact study map before deep explanation:

| Study | Question and role | Setting, units, period, sample | Exposure/assignment and comparison | Outcome and timing | Estimand or target | Main exhibit | Principal limitation |
| --- | --- | --- | --- | --- | --- | --- | --- |

For a single-study paper, use the same fields without forcing a multi-study table. Track recruitment and exclusions, missing data, attrition, treatment uptake, and whether the analyzed sample differs from the target population. Distinguish randomization unit, observation unit, treatment unit, and inference or clustering unit. Check whether subgroup and mechanism analyses were planned, exploratory, or unclear.

## 2. Teach the design in Chinese

Begin with the practical comparison the authors want, then show the observed comparison they actually make. For each central estimate:

1. Define treatment/exposure, comparison condition, outcome, measurement window, units, and target population. State what a zero or reference category means.
2. Explain assignment or selection into exposure and the timing of measurement. Use a group/time diagram when it helps.
3. Name the estimand if defined (for example ATE, ATT, intent-to-treat, treatment-on-the-treated, a regression contrast, forecast accuracy, or construct validity). If the paper does not define a formal causal estimand, describe the comparison without inventing one.
4. Explain identification or validity assumptions in ordinary language and connect each to this setting. Discuss plausible threats rather than reciting a generic checklist.
5. Map each diagnostic, robustness check, placebo, balance test, sensitivity analysis, or triangulating study to the specific threat it addresses. Say what remains unresolved. A balance table, insignificant pretrend, or good predictive fit cannot prove the full identifying assumptions.
6. State the strength of the resulting claim: randomized causal effect, design-dependent causal estimate, association, prediction, or measurement claim.

Do not automatically prescribe difference-in-differences, instruments, matching, mediation, or other methods. Explain the design the authors actually used. For multi-study work, describe what each study adds and whether the studies use comparable samples, treatments, outcomes, and estimands.

## 3. Decode specifications and numbers

For each load-bearing equation or model, reproduce the paper's notation faithfully and define indices, time, variables, controls, fixed effects, link function, baseline, interactions, and error term. Explain why each term is present. Show the minimum algebra needed to interpret a coefficient, marginal effect, predicted difference, or hypothesis test. Distinguish an equation printed in the paper from an explanatory rewrite or supplemental derivation.

Be precise about:
- Level versus change, percentage versus percentage points, relative versus absolute risk, odds versus probability, log points versus percentage changes, and local versus finite changes.
- Conditional effects under interactions, nonlinear models, and transformations; do not interpret an interaction coefficient alone as the total subgroup effect.
- The actual reference group and model column used. Report uncertainty as given; do not infer exact p-values or confidence intervals from stars.
- Whether a numerical headline is a raw contrast, regression-adjusted estimate, model prediction, subgroup contrast, decomposition, or simulation. Reconstruct calculations only when the paper provides sufficient inputs; show denominators and rounding.
- Whether multiple outcomes, subgroups, model variants, or studies invite selective emphasis. Show the principal result in context rather than selecting the largest estimate.

If a table is too dense for a slide, reproduce only verified rows/columns with a clear label and source, or show the original exhibit at readable size. Keep a link to the full exhibit in notes or the evidence index.

## 4. Build an evidence-bounded narrative

For each principal finding, record: the question, exact exhibit and column/panel, estimate or comparison, outcome scale and baseline, uncertainty, sample, interpretation, and caveat. Distinguish a statistically detectable result from practical importance. Give null or mixed findings enough visibility to qualify the headline.

Separate:
- Main effects from heterogeneity and mechanisms.
- Observed mediator patterns from an identified causal mediation effect.
- Within-sample evidence from external validity and transport to another population, platform, time, or intervention.
- Authors' claims from the presenter's interpretation and suggested applications.

Use this empirical slide arc when it fits: question and early answer; setting and study map; sample and measurement; assignment/comparison and estimand; key specification or identification logic; one or more principal result exhibits; mechanism or heterogeneity; most consequential threat and evidence addressing it; synthesis across studies; theoretical and managerial implications; scope and open questions. A scale-development or predictive paper should instead foreground construct definition, validation or prediction target, data splits, comparison benchmarks, and use conditions. Keep a detailed learning deck spacious, splitting dense results across pages.

Prefer timelines, group/comparison diagrams, annotated original exhibits, reproducible effect plots, and small tables with one highlighted comparison. Show an audience-visible sentence interpreting each major result. Label conceptual diagrams and reconstructed charts. Preserve axes, units, baselines, uncertainty, and source attribution; never invent missing values.

## 5. Completion check

Before delivery, verify that a reader can answer: What was compared? Who or what was measured, and when? What is the estimand or claim type? Which exhibit supports each headline? How large is the effect on its correct scale? What assumptions carry the inference? Which threat matters most? What can a manager or researcher reasonably do with the finding, and where might it fail?

Use the shared evidence ledger, bilingual notes, numbered slide titles, page count, permanent navigation, visual review, and renderer-specific checks in SKILL.md and user-requirements.md. Do not copy values or conclusions from a visual reference deck into an unrelated paper.
