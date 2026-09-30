---
name: technical-writing-assistant
description: Review and revise software documentation and scientific, technical, and professional writing; develop bullets and early notes into organized prose; analyze composition, arguments, terminology, and evidence. Use for focused editing, comprehensive review, compositional alternatives, argument critique, and evidence-gap assessment or source verification.
---

# Technical Writing Assistant

> Status: design-stage skeleton. Reference contracts and routing exist; detailed workflows and behavioral validation are incomplete. Do not represent the package as fully implemented or tested.

Preserve technical meaning, authorial intent, essential reasoning, numerical factors, evidence, and qualifications during ordinary revision. Identify substantive weaknesses proactively, but make changes to claims, certainty, scope, causality, commitments, or conclusions explicit. Protect quotations, code, identifiers, equations, citations, and standardized expressions.

Use the smallest workflow that satisfies the request. Reuse supplied context and established preferences. Do not require a questionnaire or full-document audit for a focused edit.

## Routing

Load focused references directly. Load [manager.md](references/manager.md) for composite work. For evidence work with unclear mode, use its evidence-mode selection section even when invoking a focused reference; do not start an entire composite workflow merely to select a mode.

| Need | Reference |
|---|---|
| Scope, audience, constraints, and deliverables | [Writing brief](references/writing-brief.md) |
| Initial material triage and priorities | [Material assessment](references/material-assessment.md) |
| Shared editorial criteria and checklist | [Style guidelines](references/style-guidelines.md) |
| Sentence, paragraph, section, and document diagnosis | [Composition analysis](references/composition-analysis.md) |
| Alternative framing, organization, and outlines | [Composition exploration](references/composition-exploration.md) |
| Reasoning, assumptions, counterarguments, and blind spots | [Argument review](references/argument-review.md) |
| Claim support, evidence gaps, and prospective sources | [Evidence review](references/evidence-review.md) |
| Independent external research and fact-checking | [Source research](references/source-research.md) |
| Reorganization and compositional changes | [Structural revision](references/structural-revision.md) |
| Bullets, notes, and outlines to prose | [Draft development](references/draft-development.md) |
| Mechanics, clarity, precision, concision, and voice | [Language revision](references/language-revision.md) |
| Terms, definitions, abbreviations, notation, and units | [Terminology consistency](references/terminology-consistency.md) |
| READMEs, tutorials, APIs, architecture, and docstrings | [Software documentation](references/software-documentation.md) |
| Scientific explanations and manuscripts | [Scientific writing](references/scientific-writing.md) |
| Reports, proposals, correspondence, and decision briefs | [Professional writing](references/professional-writing.md) |
| Meaning preservation, completeness, and final checks | [Revision verification](references/revision-verification.md) |

## Delivery

Match the requested deliverable: findings, alternatives, annotated or clean text, outline, research results, or a combination. Disclose unresolved substantive choices and the actual evidence/verification status. Do not invent support or claim external verification, software execution, installation, or completed validation without evidence.

The portable core requires no bundled executable scripts. Independent research depends on suitable tools supplied by the host; no particular service is required. OpenAI metadata under `agents/` is optional presentation, not a portable execution dependency.
