# Technical Writing Assistant: Capability Map

## Contents

- [Purpose and status](#purpose-and-status)
- [Governing principles](#governing-principles)
- [Package and routing model](#package-and-routing-model)
- [Capability decomposition](#capability-decomposition)
- [Structured outlines and maps](#structured-outlines-and-maps)
- [Composition analysis coverage](#composition-analysis-coverage)
- [Shared style policy](#shared-style-policy)
- [Module contracts and coupling](#module-contracts-and-coupling)
- [Manager decisions and evidence modes](#manager-decisions-and-evidence-modes)
- [Practical composite workflows](#practical-composite-workflows)
- [Implementation status and validation boundary](#implementation-status-and-validation-boundary)

## Purpose and status

Develop an editing-first writing assistant covering software documentation and broader scientific, technical, and professional writing. Its primary purpose is improving existing material. It also supports major transformations from early bullets, fragments, and brainstorming into organized, developed text.

In development and critical-review work, the assistant helps explore compositional options, identify prospective evidence and its intended use, critique or challenge arguments, and surface weaknesses, blind spots, unjustified assumptions, logical fallacies, and missing support. In review and revision, it improves clarity, structure, terminology, style, composition, and consistency while preserving technical meaning.

The assistant also generates, reviews, validates, and revises structured outlines and maps as standalone deliverables or foundations for developed text. It adapts the general workflows to the task context, including specialized representations whose requirements must first be explored.

This map records the agreed capability design and its rationale. The full project requirements and module order are recorded in [SPEC.md](SPEC.md) and [PLAN.md](PLAN.md). The accompanying package implements all named references with procedures, examples, failure handling, and completion criteria. Final package review and representative execution are in progress; implementation alone does not establish behavior across clients and models.

## Governing principles

The central distinction is between improving expression and reconsidering substance. During ordinary revision, preserve technical meaning and the author's position. During development or critical review, challenge that position when appropriate, identify alternatives, and propose substantive changes explicitly.

- Preserve technical meaning, authorial intent, and essential support during ordinary revision.
- Identify problems proactively and propose useful improvements. Make proposed changes to claims, assumptions, certainty, scope, causality, commitments, and conclusions explicit.
- Scale the work to the request. A focused edit remains focused; a substantial development task permits deeper examination of reasoning, evidence, and alternatives.
- Load only the references needed for the task. Support independent subworkflows and coordinated composite workflows.
- Never silently convert an editorial improvement into a substantive change. Explain its implications and distinguish it from ordinary wording revision.
- Do not manufacture coherence. A missing transition may reveal a missing argument; flag the gap rather than insert a connective that makes unsupported reasoning appear complete.
- Preserve essential reasoning, numerical factors, qualifications, and evidence when shortening text. Retaining only the headline conclusion is insufficient.
- Treat quotations, code, identifiers, equations, citations, and standardized expressions appropriately. Editorial rules must not silently alter protected material.

## Package and routing model

Use one standalone skill with a compact `SKILL.md`, focused references, and `manager.md` for coordination. The manager's filename is `manager.md`, replacing the earlier proposed `wra-manager.md`.

The entry point provides activation, essential safeguards, and direct routing. Focused requests load their relevant references directly without requiring the full manager workflow. Composite requests load `manager.md`, which selects the smallest sufficient workflow, sequences work, tracks decisions, and consolidates findings.

Define evidence modes in the manager. A directly invoked evidence workflow uses the relevant mode-selection section when needed without initiating a complete composite workflow. Shared guidance supplies editorial criteria; genre references supply contextual conventions. They are loaded only when useful.

The standalone package directory is `technical-writing-assistant/`; development documentation remains outside it under `docs/dev/`. The package uses ordinary text and Markdown and does not depend on a particular host, installation directory, connector, or vendor-specific API. Optional OpenAI presentation metadata is separate from the portable skill core.

## Capability decomposition

The following filenames are package boundaries, not a requirement to execute every module.

| Reference | Scope and outputs | Boundary |
|---|---|---|
| `manager.md` | Define task modes, select and coordinate workflows, resolve overlapping findings, retain decisions, and consolidate results. Include practical workflow recipes. | Coordinates substantive work; does not duplicate detailed editorial procedures. |
| `writing-brief.md` | Establish purpose, audience, genre, dialect, register, constraints, source authority, revision depth, and deliverables. Reuse supplied information and established preferences. | Defines the task; does not require a questionnaire before every edit. |
| `material-assessment.md` | Assess maturity, completeness, contradictions, missing context, and suitability for the requested work. Produce initial diagnosis and priorities. | Performs triage; detailed composition, argument, and evidence examinations belong to their respective modules. |
| `style-guidelines.md` | Maintain authoritative style guidance and the checklist derived from the supplied guidelines, including contextual qualifications. | Provides shared editorial criteria; does not prescribe document organization or establish factual correctness. |
| `composition-analysis.md` | Diagnose composition at sentence, paragraph, section, and document levels. Produce located findings, reader consequences, and proposed remedies. | Analyzes existing composition; does not automatically rewrite it or redesign its substantive argument. |
| `composition-exploration.md` | Develop alternative framing, organizing principles, outlines, emphasis, and explanatory or argumentative sequences. Explain trade-offs and recommend an approach. | Explores alternatives before substantial restructuring or drafting; does not manufacture support for the selected approach. |
| `outline-context-exploration.md` | Establish what an outline or map must represent, its purpose, audience, sources, organizing dimensions, relationships, detail, and success criteria. Propose alternatives when these are unclear. | Resolves contextual structural choices; reuses established information and does not require exploration for every task. |
| `outline-generation.md` | Generate a structure using agreed contextual criteria. Support hierarchies, tables, relationship maps, or combinations; distinguish source-derived content from proposed additions. | Does not invent requirements, unsupported relationships, or established project scope; does not automatically develop full prose. |
| `outline-review.md` | Critique coverage, grouping, boundaries, granularity, sequence, relationships, emphasis, and practical usefulness. Recommend repairs or alternative structures. | Evaluates conceptual and editorial quality; does not treat preferences as validation failures. |
| `outline-validation.md` | Check conformity to the agreed structural contract, fidelity to supplied sources, internal consistency, and coverage of identified requirements. Report defects and validation limits. | Claims completeness only relative to identified sources and criteria; structural validity does not establish factual correctness. |
| `argument-review.md` | Examine claims, premises, assumptions, inference, counterarguments, qualifications, contradictions, fallacies, and blind spots. Propose repairs and author decisions. | Assesses reasoning; empirical verification belongs to evidence work. Explain reasoning defects rather than merely attach fallacy labels. |
| `evidence-review.md` | Identify claims requiring support, assess supplied evidence, examine whether sources support the actual claims, and identify gaps and prospective evidence. | Owns the relationship between claims and support; delegates independent retrieval and verification when the evidence mode permits it. |
| `source-research.md` | Find and inspect external sources, fact-check claims, verify prospective references, compare conflicting evidence, and record attribution and verification limits. | Executes external research only in the research mode; does not silently revise the author's conclusions. |
| `structural-revision.md` | Change organization, grouping, hierarchy, paragraph boundaries, sequencing, headings, transitions, and placement of supporting material. | Changes arrangement and development of existing content. Missing substantive material is flagged or handed to drafting and evidence workflows. |
| `draft-development.md` | Transform bullets, notes, fragments, or an agreed outline into developed prose. Supply explanations and connective material within authorized scope; expose unresolved content needs. | Develops text without inventing facts, findings, citations, commitments, or an authorial position. |
| `language-revision.md` | Improve mechanics, clarity, precision, concision, register, collocations, sentence construction, pronoun references, and voice. | Preserves substantive meaning; meaning-changing edits become explicit proposals. |
| `terminology-consistency.md` | Reconcile terminology, definitions, abbreviations, notation, naming, units, and recurring expressions. Produce a terminology record when useful. | Checks consistency and usage; consistently repeated terminology is not automatically technically correct. |
| `software-documentation.md` | Apply conventions for READMEs, tutorials, procedures, API references, architecture documents, and docstrings. Check prerequisites, examples, interfaces, and alignment with supplied code. | Documents behavior supported by inspected material; does not implement software or claim unperformed execution checks. |
| `scientific-writing.md` | Apply conventions for scientific explanations, manuscripts, methods, results, discussions, abstracts, and related material. Check reporting clarity, uncertainty, and separation of observations from interpretation. | Provides genre guidance; does not invent methods, results, statistical support, or journal requirements. |
| `professional-writing.md` | Apply conventions for reports, proposals, technical correspondence, decision briefs, and other professional texts. Check purpose, audience needs, recommendations, actions, and commitments. | Provides genre guidance; does not invent organizational positions, promises, approvals, or commercial terms. |
| `revision-verification.md` | Compare the result with the brief and source material. Check meaning, completeness, evidence status, consistency, composition, and applicable style requirements. Report unresolved issues. | Verifies delivered work; does not imply independent factual verification when no research occurred. |

Separating `source-research.md` and `draft-development.md` makes two capabilities explicit: researching support and developing prose. This prevents evidence review and structural revision from becoming overly broad. Similarly, composition analysis diagnoses the existing text, composition exploration proposes alternatives, and structural revision implements authorized changes.

## Structured outlines and maps

Structured outline work is an explicit capability covering generation, review, validation, and revision. An outline or map may be the final deliverable; the workflow must not automatically turn it into prose. Users can enter at any stage, including reviewing or repairing an existing structure without regenerating it.

Specialization emerges from the task context rather than a predefined catalogue of cases. A skill capability map derived from project materials is one example of applying the general capability, not a limit on its scope or a required dedicated module. The agent facilitates contextual exploration when needed, defines the relevant representation and criteria, and adapts the general workflows accordingly. Do not require an `outline-profiles.md` catalogue or a separate workflow for every specialized map.

### Contextual exploration and working contract

Use the request, supplied materials, and established decisions first. When consequential choices remain unclear, explore alternatives and their trade-offs with the user. Establish a small task-specific working contract in ordinary prose or Markdown:

- What is represented, for what purpose, and for which audience.
- Which sources govern the content and what their authority and limitations are.
- Which kinds of elements and relationships matter.
- Which fields, hierarchy, or other representation serve the task.
- What belongs within scope and what is excluded.
- How completeness, consistency, and usefulness will be assessed.

These are prompts for judgment, not mandatory fields or a questionnaire. An ordinary document outline may need only purpose and section sequence; a more complex map may need responsibilities, boundaries, dependencies, and status. Resolve material uncertainty without adding unnecessary process to a clear request.

Adapt the representation to the relationships in the material. Do not force a hierarchy onto cross-cutting relationships, invent dependencies to fill a template, or imply exhaustive coverage when sources are incomplete. Use nested lists, tables, relationship maps, or combinations as appropriate; the capability is not tied to a rendering tool or format.

### Generation and review coverage

| Dimension | Questions and checks |
|---|---|
| Coverage | Are required topics represented? What is missing, excluded, or unnecessarily added? |
| Hierarchy and relationships | Are parent–child relationships meaningful where hierarchy is used? Are levels distinguishable and other relationships explicit and justified? |
| Granularity | Are nodes fragmented or overloaded? Is the decomposition sufficiently consistent for the task? |
| Boundaries | Do responsibilities or topics overlap? Is coverage duplicated or ownership unclear? |
| Sequence | Do prerequisites, dependencies, logical progression, and audience needs inform the order? |
| Node quality | Are titles informative, purposes clear, and intended content sufficiently explained? |
| Traceability | Can elements be related to supplied requirements and source materials? Are proposed additions distinguishable? |

For substantial work, nodes may include purpose, scope, exclusions, source references, dependencies, and unresolved questions. Keep simple outlines lightweight. Review should produce located findings, consequences, suggested remedies, and any substantive decisions required; it should not automatically rewrite the structure.

### Validation and source fidelity

Distinguish structural validity, source fidelity, and coverage against requirements. A well-formed outline can still omit essential material or misrepresent its sources. Define the criteria before judging conformity and distinguish validation failures from editorial recommendations. Report checks performed, unresolved issues, and limitations, including incomplete sources or unsupported completeness claims.

In a skill capability-map task, for example, inspect the available project materials and distinguish declared capabilities, procedures actually described in resources, proposed additions, and implementation or validation status established by evidence. Examine scope, boundaries, inputs, outputs, routing, dependencies, shared guidance, and composite workflows where relevant. Surface orphaned resources, routing gaps, overlapping responsibilities, or declared capabilities absent from the inspected package. Filenames alone do not establish implementation or successful behavior. These criteria illustrate contextual adaptation rather than define a mandatory schema for other maps.

Apply the existing evidence modes when factual or external verification is involved. Reading supplied project material and validating its representation do not by themselves constitute independent external fact-checking.

### Boundaries and coordination

`composition-exploration.md` examines how a text could be organized and developed. `outline-context-exploration.md` determines what a structured representation must capture. They may cooperate when the outline will become prose, without duplicating their procedures. `writing-brief.md` supplies existing task context; outline exploration adds only representation-specific decisions.

`outline-review.md` critiques the structure's conceptual and editorial quality. `outline-validation.md` checks explicit criteria and sources. `revision-verification.md` checks the final deliverable against the overall brief and original material, using relevant outline findings rather than repeating every specialized check. Authorized repairs proceed through the applicable outline workflows, revisiting context or generation only when findings justify it.

## Composition analysis coverage

Detailed compositional analysis examines small, fragmented, underdeveloped, or overloaded sentences, paragraphs, and sections. It considers whether to combine, split, expand, trim, or relocate material based on its function and reader consequences.

| Level | Coverage |
|---|---|
| Sentence | Fragmentation, overload, completeness, information order, emphasis, ambiguous references, excessive nesting, interruptions, and logical connections. |
| Paragraph | A coherent controlling idea; sound topic sentences accurately reflecting contents; adequate development; size and density; sentence sequence; transitions; closure. |
| Section | Clear purpose, meaningful boundaries, hierarchy, grouping, proportion, heading accuracy, internal progression, and transitions between sections. |
| Document | Overall trajectory, continuity, prerequisites, distribution of material, redundancy, balance, openings and conclusions, navigation, and integration of examples, lists, tables, figures, equations, and quotations. |

Across these levels, examine logical and semantic flow: missing steps, contradictions, scope shifts, topic drift, unexplained introductions, abrupt reappearances, and the burden placed on readers.

| Dimension | Diagnostic questions |
|---|---|
| Unit size and load | Is a unit fragmented, underdeveloped, or overloaded? Would combining, splitting, expanding, or relocating improve it? |
| Paragraph focus | Does the paragraph have a controlling idea? Are competing topics, digressions, or misplaced content present? |
| Topic sentences | Does the topic sentence accurately reflect content, scope, and emphasis? Does the paragraph develop the announced idea? |
| Internal development | Are assertions sufficiently explained, supported, exemplified, qualified, or interpreted? Are there unsupported jumps or premature conclusions? |
| Transitions | Are relationships between sentences, paragraphs, and sections clear and accurate? Does a connective express a real relationship? |
| Logical and semantic progression | Are reasoning steps missing? Are there contradictions, ambiguous relationships, topic drift, or meaning and scope changes? |
| Information order | Do definitions, context, assumptions, and prerequisites appear before readers need them? Does familiar information prepare for new information? |
| Hierarchy and grouping | Are major and subordinate ideas distinguishable? Is related material grouped? Do section boundaries reflect meaningful divisions? |
| Emphasis and proportion | Do important ideas receive appropriate prominence and development? Are central points buried or minor details dominant? Are qualifications near their claims? |
| Continuity and reference | Can readers trace concepts, entities, terminology, and pronouns? Are introductions or reappearances unexplained? |
| Redundancy and distribution | Are explanations repeated, sections overlapping, or treatment scattered? Does useful repetition support orientation? |
| Headings and signposting | Do headings describe their sections accurately? Do previews, summaries, and cross-references help navigation? |
| Opening and closure | Do openings establish purpose and context? Do endings deliver the promised result without unsupported new conclusions? |
| Reader burden | Are nesting, interruptions, parenthetical material, distant dependencies, or unnecessary retention demands excessive? |
| Document trajectory | Does the sequence serve the purpose and genre: explanation, argument, procedure, research report, or decision brief? |
| Supporting material | Are lists, examples, tables, figures, equations, and quotations introduced, appropriately placed, and connected to the discussion? |

Sound topic sentences in each expository paragraph are a strong default. Assess accuracy as well as presence: a polished topic sentence does not repair a paragraph that develops a different idea. A justified exception, such as a brief transitional paragraph, must serve the composition rather than excuse an unfocused paragraph.

Length is a signal to investigate, not proof of a defect. A grammatically complete sentence can be conceptually fragmented; a long paragraph can remain coherent; a short section can be appropriate.

Each actionable finding identifies its location and problem, the reader consequence, a proposed remedy, and any meaning implications or author decision. Distinguish cosmetic awkwardness from a structural defect or substantive gap.

## Shared style policy

The supplied Writing Style Guidelines for Technical and Business Texts form the basis of `style-guidelines.md`. Preserve their coverage while applying the contextual qualifications below. The reference owns editorial criteria; focused workflows apply the relevant sections without duplicating them.

### Mechanics and grammar

Use accurate and consistent spelling, grammar, and punctuation in the selected dialect. Follow standard capitalization and avoid excessive uppercase for emphasis. Avoid contractions by default unless the requested voice, genre, or context warrants them.

### Vocabulary and word choice

Use precise, professional vocabulary and appropriate industry terminology. Avoid colloquial, vulgar, or unnecessarily spoken phrasing unless the context requires it; do not replace clear language with ornate formality. Match audience knowledge and explain unfamiliar jargon.

Maintain consistent technical terms. Expand unfamiliar abbreviations at first relevant use, normally giving the full term followed by the abbreviation in parentheses; consider independently read sections and audience familiarity. Use abbreviations consistently, avoid unnecessary or uncommon abbreviations, and provide a glossary when useful.

Check commonly confused words and natural collocations, including verb–noun, adjective–noun, noun–noun, preposition–noun, and adverb–verb combinations. Preserve specialized phrasing recognized in the field; improve vague or unnatural combinations where a clearer conventional expression exists.

Avoid redundant repetition, especially consecutive repetition, while retaining repetition that clarifies concepts, sustains orientation, or emphasizes a point. Vary pronouns, wording, and sentence structures only when references remain unambiguous. Stable terminology for the same technical concept takes precedence over synonym variation.

### Lists and series

Maintain grammatical and logical parallelism in lists, coordinated and correlative constructions, comparisons, infinitive phrases, gerund phrases, verb tenses, and clauses. Ensure items fit the lead-in and do not mix unrelated categories such as actions and descriptions. Group related items and use hierarchy when it improves clarity. Move genuinely common wording into the lead-in without losing qualifications. Use consistent grammar and punctuation across items.

### Sentence structure

Use complete sentences in continuous prose. Permit purposeful fragments in headings, labels, tables, and concise list items. Attach participles, infinitives, and other modifiers to the appropriate subject; avoid dangling or ambiguous constructions.

Remove unnecessary words and redundancy. Use an effective mix of simple, compound, and complex sentences. The supplied examples of short sentences at 5–10 words and longer sentences at 20–30 words are diagnostic guidance, not quotas. Avoid monotonous sequences and complexity that burdens comprehension; do not force variation where precision calls for repetition.

### Paragraph structure

Center each paragraph on one controlling idea. Prefer a sound topic sentence that accurately represents and introduces its contents, and ensure subsequent sentences develop that idea. The supplied range of three sentences to half a page is a heuristic, not a requirement to pad or arbitrarily split text.

Use purposeful transitions and appropriate paragraph boundaries. In long passages, use meaningful headings and subheadings to organize content; a heading does not cure an overloaded paragraph. A clear short paragraph should not be expanded merely to meet a target.

### Coherence and flow

Arrange ideas in a logical, audience-appropriate sequence. Make relationships between sentences, paragraphs, and sections clear, using linking words such as however, therefore, and in addition when they accurately express those relationships. Use bridging or brief recapitulation when it helps connect ideas, without repeating every preceding point.

Use clear headings and subheadings to signal meaningful topic shifts. Do not force a transition phrase into every paragraph or imply causation, contrast, or inference unsupported by the content.

### Clarity and precision

Prefer active voice when it clarifies agency. Retain passive voice when the actor is unknown, irrelevant, or appropriately secondary. Use precise nouns, verbs, adjectives, and adverbs. Ensure pronoun references are clear; accompany this, that, these, or those with a specific noun when helpful.

Avoid excessive synonym variation that blurs concepts. Prefer direct, positive, action-oriented instructions while preserving necessary prohibitions, exceptions, safety constraints, and precise requirements. Check vague or unnatural word combinations without erasing established technical usage.

### Verification checklist

- [ ] Mechanics: spelling, punctuation, grammar, capitalization, dialect, and contractions are appropriate and consistent.
- [ ] Vocabulary: register is suitable, wording precise, jargon explained as needed, and terminology stable.
- [ ] Abbreviations: introduction, reuse, and glossary treatment suit the document and audience.
- [ ] Lists and series: parallel structure, logical categories, lead-ins, and punctuation are consistent.
- [ ] Sentences: complete where required, concise, appropriately varied, and free of dangling or ambiguous modifiers.
- [ ] Paragraphs: focused, adequately developed, with sound topic sentences and purposeful boundaries.
- [ ] Coherence: logical and semantic progression, accurate transitions, appropriate information order, and useful headings.
- [ ] Precision: clear references, specific wording, and no misleading synonym variation.
- [ ] Voice and instructions: active voice and direct action where useful, with justified passive constructions and necessary negatives retained.
- [ ] Collocations: natural recognized usage, including appropriate specialized expressions.

Apply only relevant checks. Style compliance does not establish factual correctness.

## Module contracts and coupling

Every executable module defines activation conditions and exclusions, necessary inputs and missing-input handling, procedure and authority to change material, outputs and unresolved decisions, completion checks, and optional handoffs.

Shared guidance references provide applicable criteria rather than pretending to be independent transformation workflows. Genre guidance can be used independently for a focused review or alongside another module.

Use ordinary text or Markdown for handoffs. Structured issue, claim, or terminology registers can support substantial work but must not become administrative prerequisites for small edits. Each finding should carry enough context to be understood without reconstructing the entire workflow.

These boundaries separate editorial decisions. Structural revision remains usable without argument review. Argument review produces useful findings without rewriting. A parallelism check must not trigger a full argument audit, while developing an early scientific argument can warrant deeper examination of assumptions, evidence, counterarguments, and compositional alternatives.

## Manager decisions and evidence modes

The assistant should be generally proactive in identifying problems, proposing improvements, and surfacing decisions. Its authority to research externally or change substantive claims remains explicit.

| Decision | Options or considerations |
|---|---|
| Task objective | Review, revise, develop, explore alternatives, generate or assess structured outlines and maps, or a combination. |
| Revision authority | Wording changes; structural changes; substantive proposals; substantive changes already authorized by the user. |
| Evidence mode | External research and verification, or review without external research. |
| Review coverage | Focused dimensions or broader editorial examination. |
| Genre and audience | Applicable conventions, reader knowledge, purpose, and register. |
| Deliverables | Findings, annotated text, clean revision, alternatives, structured outline or map, validation findings, research results, or a combination. |
| Structured representation | Purpose, governing sources, elements and relationships, granularity, scope, representation, and review or validation criteria established from context. |

### External research and verification

Independently research and inspect sources, fact-check relevant claims, assess evidential support, and report contradictions and uncertainty. External research requires suitable host-provided tools. If they are unavailable, report the limitation and offer the non-research mode rather than claim verification or silently change the agreed mode.

### Review without external research

Use supplied material and information available from model training to identify evidence gaps, questionable claims, suitable evidence types, prospective sources, and verification steps. Conduct no independent external research. Distinguish observations grounded in supplied material from suggestions based on model knowledge. Remembered facts and prospective sources are not independently verified; do not invent uncertain bibliographic details.

Assessing supplied evidence can occur within either mode and does not require a separate third mode. Distinguish inspected supplied material from externally verified evidence, uninspected supplied references, inference, and proposed support. A prospective source must never be presented as verified support merely because it appears promising.

### Selection and persistence

At task intake, when the prompt does not clearly establish evidence preference and no applicable choice has already been established, ask a clarifying question: "Should I independently research and verify sources, or review the supplied material and identify evidence gaps and prospective sources without external research?"

Retain the answer within the task unless the user changes it. While awaiting an answer, continue organization, language, and internal-reasoning work that does not depend on external research. For a strictly focused task without an evidence component, do not inflate its scope; apply mode selection before evidence work becomes relevant.

The manager owns mode definitions and selection. Evidence review works within the selected mode; source research executes external verification only when permitted. The entry point ensures direct evidence-workflow invocation follows the same rule, using the relevant manager section without starting the entire composite workflow.

## Practical composite workflows

These are adaptable recipes, not mandatory pipelines. Select an entry point from the request and supplied material. Honor explicit instructions about whether the user wants diagnosis, alternatives, rewritten text, or research. Use the brief only to resolve material uncertainties.

| Workflow | Typical sequence | Practical result |
|---|---|---|
| Focused language edit | Brief as needed → language revision → relevant terminology checks → verification | Revised passage with substantive uncertainties preserved or flagged. |
| Composition audit | Composition analysis → optional composition alternatives | Located findings and prioritized recommendations; rewritten text only when requested. |
| Structural revision | Composition analysis → exploration if needed → structural revision → verification | Reorganized text with clearer paragraph and section purposes and accurate transitions. |
| Comprehensive editorial review | Assessment → relevant genre guidance → composition, argument, evidence, and consistency reviews → consolidation | Prioritized findings separating editorial defects, substantive weaknesses, and evidence needs. |
| Full revision of an existing draft | Assessment → selected reviews → structural revision → language revision → terminology reconciliation → verification | Revised document plus significant changes and unresolved questions. |
| Bullets or brainstorming to developed text | Brief → assessment → composition exploration → argument and evidence review → draft development → revision → verification | Organized prose grounded in supplied ideas, with missing support and assumptions visible. |
| Argument strengthening | Argument review → evidence review → external research if selected → composition exploration → authorized revision → verification | Stronger argument, or an explanation of why available support cannot sustain the proposed conclusion. |
| Fact-checking and evidence repair | Evidence mode selection → claim identification → evidence assessment → source research when permitted → proposed corrections → verification | Claim-by-claim account of support, contradictions, gaps, and appropriate wording. In non-research mode, report a gap review rather than completed fact-checking. |
| Audience or genre transformation | New brief → applicable genre guidance → composition analysis and exploration → structural revision or development → language revision → verification | Text adapted to new readership and purpose while retaining essential meaning and qualifications. |
| Concision and executive-summary development | Identify indispensable content → select emphasis and structure → compress or develop summary → verify against source | Shorter text retaining reasoning and qualifications necessary to understand its conclusions. |
| Software documentation review | Software guidance → inspect supplied implementation and documentation → composition and consistency review → revision → verification | Clearer documentation with discrepancies and unperformed behavior checks identified. |
| Scientific manuscript revision | Scientific guidance → composition, argument, and evidence review → structural and language revision → verification | Better reporting and interpretation without unsupported methods, results, or certainty. |
| Generate a structured outline or map | Brief and source assessment as needed → explore unresolved structural choices → establish contextual criteria → generation → review → validation | A context-appropriate standalone structure with proposed additions and unresolved gaps visible. |
| Review an existing outline or map | Identify purpose, sources, and criteria → context exploration if needed → review → validation → prioritized findings | Conceptual recommendations distinguished from source or structural validation failures; no regeneration unless requested. |
| Repair an outline or map | Review and validation → authorized revision through applicable outline workflows → repeat affected checks | A repaired structure with significant changes and unresolved issues recorded. |
| Derive a specialized map from source materials | Inspect materials → explore needed elements and relationships → contextual contract → generation → review → source and coverage validation | A specialized map adapted to its context, such as a skill capability map, with source-derived content, proposals, and status distinguished. |
| Outline to developed text | Review and validate the outline as needed → argument and evidence work where relevant → draft development → revision → verification | Developed prose grounded in the outline and sources, with missing support and qualifications retained. |

The manager revisits earlier stages when findings justify it. An unsupported conclusion may require a narrower argument; a paragraph split may expose a missing explanation; external research may require changing the outline. Consolidate duplicate findings and resolve disagreements between workflows before presenting recommendations.

Do not make every handoff an approval gate. Ordinary work proceeds within the user's authorized scope. Seek an author decision when a substantive choice is unresolved, not merely because the next module is ready to run.

## Implementation status and validation boundary

The package implements all 21 named references, including the four outline workflows, and directly routes to each from SKILL.md. The manager implements both evidence modes and all 17 composite recipes. The shared style guidance retains the supplied coverage and contextual qualifications; detailed composition and outline procedures apply the boundaries above.

Structural validation and representative task execution assess different properties. Package checks demonstrate format and resource integrity; sample outputs can reveal behavior on the sampled tasks. Neither establishes universal writing quality, successful live research, installation, or behavior across hosts and models. Final full review is in progress. Subsequent work should extend evaluation from real use and repair observed weaknesses without replacing contextual judgment with a fixed profile catalogue.
