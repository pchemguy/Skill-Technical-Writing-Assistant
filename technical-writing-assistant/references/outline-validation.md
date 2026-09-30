# Outline validation

## Scope and authority

Check a structured outline or map against explicit contextual criteria and identified source material. Separate structural validity, source fidelity, and coverage against requirements. Use on generated or existing artifacts. Do not claim factual correctness or universal completeness from a well-formed structure.

## Inputs and missing information

Use the artifact, working contract, governing sources, and requirements. If criteria are absent, derive and state defensible provisional criteria from the request; use [outline context exploration](outline-context-exploration.md) for consequential ambiguity. Do not silently invent a mandatory schema. Without source access, perform only supported internal checks and mark source fidelity or completeness not assessed.

## Procedure

1. Define the validation boundary: exact artifact/version, inspected sources, scope, and criteria. Distinguish required constraints from editorial preferences.
2. Check structural validity in the chosen representation: node references resolve; labels are distinguishable where needed; hierarchy or typed relationships are coherent; required fields exist; stated order and dependencies are consistent. Cycles are defects only when the relationship requires acyclicity.
3. Check source fidelity: trace claims, nodes, status labels, and relationships to inspected material. Identify omissions, contradictory representations, unsupported additions, and proposals presented as established facts.
4. Check coverage against identified requirements. Map each required item to a location or an explicit gap. Consider exclusions and unavailable sources; do not inflate optional improvements into requirements.
5. Check cross-view consistency when a tree, table, and diagram represent the same material. Names, boundaries, statuses, and relations should agree or explain their different perspectives.
6. Classify results per criterion as satisfied, failed, or not assessable, with source/location and reason. Use “not applicable” only for criteria genuinely outside scope, not missing evidence.
7. Recommend precise repairs. Recheck affected criteria after authorized changes; a title fix may require checking node notes and cross-references. Route conceptual recommendations to [outline review](outline-review.md) rather than mislabeling them validation failures.

## Outputs

For a simple artifact, return findings and a bounded conclusion. For a substantial one, use a criterion/requirement, location/source, result, and repair table. State what was checked, unresolved failures, and limits. “Complete against the supplied requirements” is narrower than “complete.” Do not claim unperformed automated checks.

## Examples and failure handling

- A capability map marks a module “tested,” but the project supplies only its declaration. Fail the status claim's source-fidelity check; implementation may exist elsewhere, so do not assert it is absent universally.
- A requirement mandates error handling and no node covers it. Report a coverage failure and proposed location, without inventing the policy.
- A two-way communication relationship can form a valid cycle; a strict prerequisite order containing a cycle requires repair. Apply the relationship's semantics.
- If half the source set is inaccessible, report internal validation and partial source assessment. Do not issue an unqualified completeness pass.

## Completion checks

All assessed criteria have a stated basis and outcome. Unavailable evidence is distinguished from failure, and optional preferences from requirements. Source-derived content and proposals are distinguishable. The conclusion reflects the actual validation boundary and remaining defects.
