# Workflow manager

> Status: manager skeleton. Task decisions, evidence modes, and workflow recipes are defined; detailed orchestration procedures and behavioral acceptance cases remain to be implemented.

## Contents

- [Scope and boundary](#scope-and-boundary)
- [Task decisions](#task-decisions)
- [Evidence modes and selection](#evidence-modes-and-selection)
- [Composite workflow recipes](#composite-workflow-recipes)
- [Coordination and outputs](#coordination-and-outputs)
- [Completion checks](#completion-checks)
- [Implementation work remaining](#implementation-work-remaining)

## Scope and boundary

Select and coordinate the smallest sufficient workflow. Retain task decisions, resolve overlapping findings, and consolidate results. Do not duplicate the focused procedures or load every reference by default. Focused workflows remain independently executable.

## Task decisions

| Decision | Considerations |
|---|---|
| Objective | Review, revise, develop, explore alternatives, or a combination. |
| Revision authority | Wording changes, structural changes, substantive proposals, or substantive changes already authorized. |
| Evidence mode | External research and verification, or review without external research. |
| Coverage | Focused dimensions or broader editorial examination. |
| Genre and audience | Applicable conventions, reader knowledge, purpose, and register. |
| Deliverables | Findings, annotated text, clean revision, alternatives, outline, research results, or a combination. |

Use [writing-brief.md](writing-brief.md) only to resolve material uncertainties. Reuse the request and established preferences; do not ask the same questions again.

## Evidence modes and selection

### External research and verification

Independently research and inspect sources, fact-check relevant claims, assess evidential support, and report contradictions and uncertainty. Delegate execution to [source-research.md](source-research.md) and claim/support assessment to [evidence-review.md](evidence-review.md).

Use suitable host-provided tools. If unavailable, disclose the limitation and offer review without external research. Do not claim verification or silently substitute a different mode.

### Review without external research

Use supplied material and model knowledge to identify evidence gaps, questionable claims, suitable evidence types, prospective sources, and verification steps. Conduct no independent external research.

Distinguish observations grounded in inspected supplied material from suggestions based on model knowledge. Remembered facts and prospective sources are not independently verified. Do not invent uncertain bibliographic details.

Assessment of supplied evidence is available in both modes; it is not a third mode. Separate inspected supplied material, uninspected supplied references, externally verified evidence, inference, and proposed support.

### Selection and persistence

At task intake, if the prompt does not clearly establish evidence preference and no applicable choice is established, ask:

> Should I independently research and verify sources, or review the supplied material and identify evidence gaps and prospective sources without external research?

Retain the selected mode within the task unless the user changes it. Continue independent organization, language, or internal-reasoning work while awaiting the answer. For a strictly focused task without evidence work, preserve its scope; resolve the mode before evidence work becomes relevant.

A directly invoked evidence workflow uses this section without initiating the full manager workflow.

## Composite workflow recipes

Adapt these recipes to the request. Each named step routes to its corresponding focused reference. Shared [style-guidelines.md](style-guidelines.md) and applicable genre guidance supply criteria, not mandatory extra stages.

| Workflow | Typical sequence | Result |
|---|---|---|
| Focused language edit | Brief as needed → language revision → relevant terminology checks → verification | Revised passage with substantive uncertainties flagged or preserved. |
| Composition audit | Composition analysis → optional exploration | Located findings and priorities; rewrite only when requested. |
| Structural revision | Composition analysis → exploration if needed → structural revision → verification | Reorganized text with clear purposes and accurate transitions. |
| Comprehensive editorial review | Assessment → genre guidance → composition, argument, evidence, and consistency reviews → consolidation | Prioritized editorial, substantive, and evidence findings. |
| Full draft revision | Assessment → selected reviews → structural revision → language revision → terminology reconciliation → verification | Revised document, significant changes, and unresolved questions. |
| Bullets or brainstorming to prose | Brief → assessment → composition exploration → argument and evidence review → draft development → revision → verification | Developed text grounded in supplied ideas; support gaps remain visible. |
| Argument strengthening | Argument review → evidence review → research if selected → composition exploration → authorized revision → verification | Stronger argument, or a clear account of insufficient support. |
| Fact-checking and evidence repair | Mode selection → claim identification → evidence review → research when permitted → proposed corrections → verification | Claim-linked support, contradictions, gaps, and wording. Without research, label the result a gap review, not completed fact-checking. |
| Audience or genre transformation | New brief → genre guidance → composition analysis/exploration → structural revision or development → language revision → verification | Adapted text retaining essential meaning and qualifications. |
| Concision or executive summary | Identify indispensable content → select emphasis/structure → compress or develop summary → verify against source | Shorter text preserving essential reasoning, numerical factors, and qualifications. |
| Software documentation review | Software guidance → inspect supplied code/docs → composition and consistency review → revision → verification | Clearer docs, discrepancies, and unperformed behavior checks. |
| Scientific manuscript revision | Scientific guidance → composition, argument, and evidence review → structural and language revision → verification | Clearer reporting without unsupported results or certainty. |

## Coordination and outputs

Use ordinary text or Markdown handoffs; structured issue, claim, or terminology registers are optional for substantial work. Consolidate duplicate findings and reconcile conflicting recommendations.

Iterate when findings justify it: narrow an unsupported conclusion, supply an authorized missing explanation, or reconsider an outline after research. Do not make every handoff an approval gate. Ask for an author decision when a substantive choice is unresolved; otherwise continue within authorized scope.

Respect requests for diagnosis without rewriting. Keep substantive changes visible. Produce the requested deliverable, significant changes when relevant, unresolved decisions, and the actual evidence status.

## Completion checks

Confirm that the selected work fits scope; essential meaning and support survive; findings do not contradict one another; and verification claims match work actually performed. Use [revision-verification.md](revision-verification.md) for final comparison.

## Implementation work remaining

Develop detailed selection and iteration procedures, examples of focused and composite execution, missing-tool handling, and positive/negative acceptance cases. This scaffold is not an end-to-end validated manager.
