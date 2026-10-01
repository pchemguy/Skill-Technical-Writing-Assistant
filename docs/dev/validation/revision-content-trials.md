# Revision content workflow trials

Snapshot note: initial cases ran during migration around commits `4558f1e`–`a12f50d`; the resource-read list preserves the then-existing `outline-validation.md`. Supplemental cases ran after `a8ae780` against the merged review route. These are intermediate campaign snapshots, not an inventory of the final package.

Date: 2026-10-01. These are independent exercises performed against the current repository skill, not an external model benchmark. Each response below is the actual output produced for its recorded prompt. No correctness oracle or expected-answer scoring was supplied. No independent research, example execution, software modification, or commits were performed.

## Resources read

Entry point: `technical-writing-assistant/SKILL.md`.

Focused references read: `references/outline-review.md`, `references/outline-validation.md`, `references/composition-analysis.md`, `references/draft-development.md`, `references/argument-review.md`, `references/revision-check.md`, `references/software-documentation.md`, and `references/manager.md`. The first batched reference read was truncated; draft-development, argument-review, revision-check, and software-documentation were subsequently read in full. The other named references were visible in full in that batch. No other runtime references were loaded.

All paths above are relative to the repository's `technical-writing-assistant/` directory except the entry point, which is relative to the repository. Each exercise uses only its own recorded prompt and source, without borrowing unavailable context from another exercise.

## 1a. Evaluative-only outline review

### Raw prompt

Review this outline evaluatively only; give findings, without rewriting it or adding a criterion-by-criterion validation report. Purpose: help a writer prepare a technical report. Outline: Methods > install; Results > 12 devices dry-condition result; Reliability > installation; Shared communication > A -> B -> A. Criteria: include error handling; no ungrounded status. Supplied source: "12 devices tested only under dry conditions; no humidity test; implementation declared only; two-way A/B communication". No external research.

### Raw response

The outline has a useful Methods/Results distinction, but its installation material needs clearer boundaries.

- **Reliability > installation:** The heading promises reliability content while the note describes installation. Readers could mistake setup instructions for evidence of reliable operation. Move that material under Methods, or retitle the branch if it serves a separate installation purpose. If reliability discussion is intended, describe the dry-only test boundary and absence of humidity testing rather than inventing reliability results.
- **Methods > install and Reliability > installation:** These overlap as written. Consolidate them or specify the distinct work each branch performs so the writer does not repeat setup material.
- **Error handling:** The required topic has no visible place. Add an error-handling topic where readers would use it, such as under Methods or in a separate operational section. Its policy and details are not supplied and must remain content needs.
- **Results > 12 devices dry-condition result:** Preserve both the count and dry-condition restriction when developing this branch. Keep the absence of humidity testing nearby so readers understand the result's limits.
- **Shared communication > A -> B -> A:** The cycle is appropriate for the supplied two-way communication relationship. A clearer label such as “Two-way communication between A and B” is optional; the cycle itself needs no repair.

The outline contains no explicit implementation or testing status label that needs removal. When developed, it should distinguish declared implementation from demonstrated implementation. This is an editorial review of the supplied outline, not independent verification of the source claims.

## 1b. Validation-only outline review

### Raw prompt

Validate only this outline against the supplied criteria and source; do not add design alternatives or a comprehensive composition critique. Outline: Methods > install; Results > 12 devices dry-condition result; Reliability > installation; Shared communication > A -> B -> A. Criteria: include error handling; no ungrounded status. Supplied source: "12 devices tested only under dry conditions; no humidity test; implementation declared only; two-way A/B communication". No external research.

### Raw response

I checked the supplied outline against its two explicit requirements and the supplied source. Structural checks are limited to the listed branches and communication relation.

| Criterion | Outcome | Basis and necessary repair |
|---|---|---|
| Include error handling | Failed | No branch or note covers error handling. Add a location for it; the source does not supply an error policy. |
| No ungrounded status | Satisfied in this outline | No node claims implemented, validated, or tested status beyond the supplied dry-condition test note. This does not establish implementation status; the source provides only a declaration. |
| Results fidelity | Satisfied for the stated result | “12 devices dry-condition result” preserves the supplied count and condition. It does not claim humidity testing. The absence of humidity testing is not represented explicitly. |
| Communication fidelity and cycle validity | Satisfied | A -> B -> A expresses the supplied two-way communication. Communication is not a prerequisite relation requiring acyclicity. |
| Source support for installation content | Not assessable | The supplied source gives no installation procedure or details. The outline names a topic without asserting a particular procedure. |
| Cross-view consistency | Not applicable | Only one outline view is supplied. |

The outline fails the supplied error-handling requirement. Its source fidelity has the installation limit above; no independent verification or automated validation was performed. The Reliability heading's usefulness is an editorial question outside this validation-only request.

## 1c. Comprehensive outline review

### Raw prompt

Comprehensively review this outline, including evaluative and validation activities; give findings without rewriting it. Purpose: help a writer prepare a technical report. Outline: Methods > install; Results > 12 devices dry-condition result; Reliability > installation; Shared communication > A -> B -> A. Criteria: include error handling; no ungrounded status. Supplied source: "12 devices tested only under dry conditions; no humidity test; implementation declared only; two-way A/B communication". No external research.

### Raw response

The outline needs an error-handling location and a clearer distinction between installation and reliability. Methods and Results are suitable headings for their stated content.

| Finding | Reader consequence and remedy | Assessment basis |
|---|---|---|
| No error-handling topic | Readers and writers cannot locate the required material. Add a topic under Methods or another relevant operational location; obtain its details rather than invent policy. | Explicit requirement: failed. |
| Reliability contains installation | The heading promises a different subject and duplicates Methods > install. Consolidate setup material or establish distinct boundaries. Develop reliability discussion only from supported evidence and stated limits. | Editorial mismatch; no supplied rule makes the heading itself a validation failure. |
| Dry-condition result needs its boundary retained | Keep “12 devices” and “dry conditions” together, and consider making “no humidity test” explicit nearby. Otherwise developed prose could invite a broader reading than the source supports. | Stated result fidelity: satisfied. Explicit humidity-limit signposting is an editorial recommendation, not a new requirement. |
| No implementation-status evidence beyond a declaration | Do not develop the outline into an assertion of demonstrated implementation. | No ungrounded status: satisfied for the current outline, which makes no such status claim. Actual implementation status is not established. |
| A -> B -> A is a communication cycle | It represents the supplied two-way relationship. A plain two-way label could improve readability if needed. | Structural and source-fidelity check: satisfied; acyclicity is not required. |
| Installation details unavailable | The topic can remain, but its procedure cannot be assessed from this source. | Source support for installation content: not assessable. |

This review covers the supplied outline and source only. It identifies one explicit requirement failure and the editorial issues above; it does not verify the underlying test or implementation claims. No rewritten outline or automated check was produced.

## 2. Standalone-context composition audit

### Raw prompt

Audit composition only, without rewriting or research. Standalone instructions: "Use the supplied guidelines. As agreed earlier, use the approach in the prior revision. The previous revision demonstrated safety." No referenced context is supplied. Contrast these with the currently supplied draft "Step 1: inspect input. Step 2: repeat Step 1" and the supplied comparison "Revision a: may improve. Revision b: improves".

### Raw response

The standalone instructions depend on references that their reader cannot resolve.

- **“Use the supplied guidelines”:** No guidelines are available here. The operative criteria are missing. Supply an identifiable accessible reference or state the necessary guidelines directly.
- **“As agreed earlier, use the approach in the prior revision”:** Neither the agreement nor the revision is supplied. The reader cannot determine which approach to use. State the approach from available material, or identify the missing decision; do not invent it.
- **“The previous revision demonstrated safety”:** The revision and its supporting account are unavailable. This sentence introduces a conclusion without accessible context or explanation. Identify the necessary source and summarize its relevant support if supplied. This composition audit cannot establish whether safety was demonstrated.

The other examples have available referents and therefore different issues:

- **“Step 2: repeat Step 1”:** Step 1 is present and identifiable. The cross-reference is valid. The procedure may still need a reason for repetition or a stopping condition, depending on its purpose, but its referent is not missing.
- **“Revision a: may improve. Revision b: improves”:** Both versions are supplied, so the comparison is available. The change increases certainty from possibility to assertion. That is a substantive difference to expose, rather than a broken contextual reference or a cosmetic wording improvement.

These findings concern only the supplied passages. Document-wide progression and the missing guidelines, agreement, revision, and safety evidence were not assessed.

## 3. Clean development from notes

### Raw prompt

Develop a clean draft from these notes without research: "Central position recommend system A, comparative benefit not demonstrated; secondary blue casing possible/unconfirmed; 12 units operated only dry conditions". Preserve the central position and qualifications.

### Raw response

I recommend system A, although its comparative benefit has not been demonstrated. Twelve units operated only under dry conditions, so these observations do not establish performance under other conditions.

The possible blue casing was omitted as a secondary, unconfirmed detail. The recommendation remains an authorial position; the notes do not supply a demonstrated comparative rationale. No external research was performed.

## 4. Deductive and provisional argument critique

### Raw prompt

Critique and compare these arguments without external research or rewriting: (A) "All tested units met X; this unit was tested; therefore met X". (B) "Pilot pattern suggests A may help under tested condition; further evidence needed."

### Raw response

**Argument A** is deductively valid if “tested units” and “was tested” refer to the same test population, and X has the same meaning throughout. Under those premises, the conclusion follows. The passage does not establish that the premises are true; empirical support would be a separate question. Clarify the test scope if it could be read differently.

**Argument B** makes a provisional inference rather than claiming a necessary conclusion. “Suggests,” “may,” the tested-condition boundary, and “further evidence needed” calibrate its certainty. The supplied passage does not describe the pilot pattern, comparator, sample, or possible alternative explanations, so its support strength cannot be assessed. Provide those details to make the inference inspectable without strengthening its certainty prematurely.

A should be assessed for entailment from its premises; B for evidential strength and calibrated scope. B's failure to entail its conclusion is not by itself a reasoning defect. Neither argument's empirical premises were independently verified.

## 5. Comparison-only revision check

### Raw prompt

Compare only; do not repair or research. Source: "12 of 20 samples improved under A. 2 kg × 0.4 × F. Q4 launch possible, budget not agreed. Figure 1 supports claim X." Revised: "Samples improved. 2 kg × F. We will launch Q4. Figure 1 supports claim Y. Use the approach from the earlier revision."

### Raw response

The revision loses essential qualifications and introduces claims and an instruction that the supplied source does not establish.

| Changed passage | Comparison finding |
|---|---|
| “Samples improved” | Removes 12 of 20 and condition A. The remaining wording can imply improvement across the samples generally rather than the bounded result. |
| “2 kg × F” | Drops the material factor 0.4. The expression no longer preserves the source calculation. |
| “We will launch Q4” | Changes possibility into a commitment and omits that the budget is not agreed. No authorization for that substantive change is supplied. |
| “Figure 1 supports claim Y” | Reassigns the source's figure association from X to Y. The supplied source establishes only the stated association with X; the actual figure was not supplied or inspected. |
| “Use the approach from the earlier revision” | Adds an instruction dependent on an unidentified, unavailable revision. Neither its approach nor authority is available in the comparison. |

This is a comparison of the two supplied passages only. I have not repaired the revision, independently verified the source claims, recalculated F, or inspected Figure 1 or any earlier revision.

## 6. Docstring maintenance

### Raw prompt

Revise documentation only after the signature changed from run(items) to run(items, timeout=None). Do not execute examples or change software. Both supplied implementations return len(items) and contain no explicit raises. The first project declares NumPy docstring style; the second has no declared or established convention. Do not invent timeout behavior or types.

First snippet, NumPy project:

```python
def run(items, timeout=None):
    """Return the number of items.

    Parameters
    ----------
    items : object
        Collection to count.

    Returns
    -------
    int
        Number of items.
    """
    return len(items)
```

Second snippet, no convention:

```python
def run(items, timeout=None):
    """Return the number of items."""
    return len(items)
```

### Raw response

For the NumPy project, preserve its declared convention:

```python
"""Return the number of items.

Parameters
----------
items : object
    Object supporting len().
timeout : object, optional
    Accepted but unused. Defaults to None.

Returns
-------
int
    Number of items.
"""
```

With no declared or established convention, use Google style:

```python
"""Return the number of items.

Args:
    items: Object supporting len().
    timeout: Accepted but unused. Defaults to None.

Returns:
    The number of items as an integer.
"""
```

These replacements document the supplied signature and body by static inspection. No timeout units, validation, cancellation behavior, or parameter type restriction are established by that body. I added no Raises section: the snippets contain no explicit raises and do not establish a specific exception contract. This does not claim that calls to len() cannot raise. No implementation was changed or executed.

## 7. Short warning and transition composition review

### Raw prompt

Review composition only, without rewriting or research. Warning: "Do not open the pressurized chamber." Transition: "The next section explains calibration."

### Raw response

Both sentences perform clear, distinct jobs. The warning is a complete, direct prohibition with one controlling idea. Its brevity does not require additional development for this composition-only review. The transition clearly previews the next topic and can stand alone as a signpost.

No local composition defect is apparent. Whether calibration actually follows, and whether the transition belongs at this location, requires the surrounding sections. I have not assessed the warning's technical adequacy or verified chamber safety.

## Exercise limitations

These trials are self-produced workflow outputs, not independent ratings or repeated model runs. The source snippets and outline are deliberately small; findings do not establish full-document completeness, empirical truth, or runtime behavior. The Python snippets in case 6 were included explicitly in that case's recorded prompt to make the supplied-code boundary inspectable. The single saved artifact is this development validation record; runtime skill files were not edited.

## Supplemental exercises

The following exercises were appended after the initial record. Prior raw prompts and responses above were not altered. The current entry point was read again; it now routes validation through `references/outline-review.md`. An attempted read of the earlier `references/outline-validation.md` failed because that file was no longer present. No absent procedure was treated as inspected for these exercises.

Resources read for this supplement: current `SKILL.md`, `references/outline-review.md`, `references/revision-check.md`, `references/composition-analysis.md`, `references/manager.md`, `references/scientific-writing.md`, `references/language-revision.md`, `references/evidence-review.md`, and `references/style-guidelines.md`. A batched read truncated part of manager/scientific-writing; both were subsequently read in full. Other named supplemental resources were visible in full. Paths are relative to `technical-writing-assistant/`.

## 8. Validation-only with quantity mismatch and unavailable citation

### Raw prompt

Validate only; do not rewrite, add design alternatives, or research. Artifact states "cost fell 40%". Supplied excerpt states "time decreased 40%". A second citation is supplied but its contents are unavailable. Explicit criterion: "supplied contents must include comparative cost measurements".

### Raw response

The supplied contents do not meet the explicit comparative-cost requirement.

| Dimension | Finding |
|---|---|
| Criterion outcome | **Failed:** the available supplied contents report time, not comparative cost measurements. A citation whose contents are unavailable does not supply inspectable measurements. |
| Inspected source-to-claim relationship | The excerpt **does not address** “cost fell 40%.” Its 40% value measures time. It does not establish the same percentage for cost, and it does not by itself contradict a separate cost result. |
| Second citation | Contents unavailable and uninspected; its support for the cost claim is **not assessed**. |
| Overall cost claim | Unresolved within the supplied material. Lack of supplied support does not establish that the claim is false. |

Supply comparative cost measurements to satisfy the criterion, or explicitly revise the claim and requirement with appropriate authority. I have assessed only the supplied contents and their relationship to the artifact; no independent verification, citation retrieval, or artifact change was performed.

### Action limits

Validation findings only. No revised text or external source acquisition.

## 9a. Revision check against source notes

### Raw prompt

Check the revision against the notes, without research or rewriting. Notes: "possible Q4 launch, budget not agreed". Draft: "will launch Q4".

### Raw response

The draft does not preserve the notes' planning status. “Will launch Q4” changes a possible launch into a commitment and drops the unresolved budget. No authorization for either substantive change is supplied.

Preserve the possibility and budget qualification, or obtain an explicit decision supporting the commitment. Source notes are sufficient for this comparison; an earlier prose draft is not required. I compared only the supplied notes and draft, without verifying launch feasibility or changing the text.

### Action limits

Comparison only; no repair, research, or scheduling action.

## 9b. Findings-only composition review with no revised artifact

### Raw prompt

Perform a separate findings-only composition review. Input: a coherent setup paragraph, no revised artifact. No external research. The paragraph itself is not supplied; this description is the complete input.

### Raw response

No paragraph text is available to inspect. Its description as “coherent” does not establish the actual topic sentence, progression, references, or adequacy of development, so I cannot report located composition findings from it.

Provide the paragraph for a composition review. No revised artifact is required for that findings-only task, and there is no revision comparison to perform here. This response is limited to the missing-input finding; it does not certify the unseen paragraph's composition.

### Action limits

No paragraph was invented or rewritten. No revision-check workflow was applied to an absent revision.

## 9c. Supplied revision with unavailable source

### Raw prompt

Check the quality and fidelity of this supplied revised paragraph: "12 devices improved". The source is unavailable. No research or rewriting.

### Raw response

The sentence is grammatically complete and preserves an explicit count. Locally, “improved” leaves the outcome and comparison baseline unspecified, so a reader cannot tell what changed or what it was compared with. Clarify those details from available source material rather than inventing them.

Source fidelity is **not assessable**: the source is unavailable. I cannot establish whether the count, condition, population, certainty, or qualifications were preserved, or whether essential information was omitted. The local quality observation is not a fidelity pass or empirical verification. No revision was made.

### Action limits

Internal quality inspection only where supported; source comparisons unavailable and reported as such.

## 10. Comprehensive revision of an already coherent paragraph

### Raw prompt

Comprehensively revise this already coherent text without research. Purpose: technical-report paragraph. Give clean wording and preserve numbers and qualifications: "A 12-device pilot showed lower losses only under dry conditions. Performance in humid conditions was not tested."

### Raw response

A 12-device pilot showed lower losses only under dry conditions. Performance in humid conditions was not tested.

The wording and structure were retained because the paragraph already connects the bounded result to its testing limitation clearly. The count, dry-condition restriction, and absence of humidity testing are preserved. The comparison behind “lower losses” is not specified in the supplied excerpt; identify its baseline elsewhere in the report if it is not already clear. No comparator, significance claim, mechanism, or broader performance result was added. This was an editorial assessment of the supplied paragraph, without external research or analytical validation.

### Action limits

No forced reorganization or new substantive content. Clean text delivered unchanged after the relevant composition, language, reporting, support-boundary, and fidelity checks.

## 11. Warning contrasted with an ordinary expository paragraph

### Raw prompt

Review composition only without research or rewriting. Warning: "Do not open the pressurized chamber." Ordinary expository paragraph: "Calibration is simple. It requires six dependent preparation operations, two prerequisite measurements, and specialist authorization."

### Raw response

The warning is a coherent, direct prohibition. Its one-sentence form serves its purpose; no added topic sentence or padding is needed for composition alone.

The expository paragraph has a topic/content mismatch. “Calibration is simple” announces ease, but the next sentence describes several dependencies, prerequisite measurements, and authorization. Readers receive a complexity and access account rather than an explanation of the asserted simplicity. The listed requirements do not conclusively prove that calibration is difficult, but this paragraph does not explain why “simple” is the appropriate framing.

Revise the topic sentence to introduce the actual prerequisites, or supply the basis for calling calibration simple if that position is intended and supported. That choice affects the paragraph's substantive framing and should remain explicit. The paragraph's short length is not the defect; its announced idea and development are misaligned.

This review covers the two supplied passages only. It does not assess technical safety, verify the calibration requirements, or review unseen procedures or surrounding sections.

### Action limits

Located composition diagnosis and remedies only; no automatic rewrite or technical verification.

## Supplemental limitations

No expected outputs, correctness oracle, or scoring were included. Supplemental responses are actual self-produced workflow exercises, with no independent assessor or model execution. Resource-file reads served to inspect the current skill procedures, not to research the claims in the exercise prompts. No runtime files, prior raw trial outputs, software, or examples were changed or executed, and no commits were made.
