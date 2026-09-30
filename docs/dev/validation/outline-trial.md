# Task 1 — Decision ownership and evidence map

Scope: supplied facts only. This map groups authority, evidence flow, and shared dependencies; row order does not imply a procedure.

| Entity | Supplied role | Authority or ownership boundary | Relationships |
|---|---|---|---|
| Department A | Approves release | Release approval authority | Receives measurement reports from B |
| Team B | Supplies measurement reports | No other authority specified | Sends reports to A and C; shares D with C for instrument calibration |
| Team C | Checks specifications | Has no release authority | Receives measurement reports from B; shares D with B for instrument calibration |
| Team D | Instrument calibration | Shared by B and C; exclusive ownership is not established | Shared calibration dependency of B and C |
| Calibration-exception approval | Approver not documented | **Ownership gap** | Do not assign approval to A, B, C, or D without further evidence |

Evidence flow: **B → A** and **B → C**, both carrying measurement reports. Shared dependency: **B ↔ D ↔ C**, where the links denote shared use for instrument calibration, not reporting or approval.

Check against supplied facts: all four entities, release authority, report recipients, specification checking, C's authority limit, shared calibration dependency, and the undocumented exception approver are represented. No source establishes additional authority or a procedural sequence.

# Task 2 — Review and validation of the supplied map

Boundary: the exact supplied map, assessed against the same supplied facts and the stated ownership/authority and coverage criterion. The map is reviewed below without being regenerated.

**Conclusion: fails source fidelity and relationship coverage.** Its entity labels are distinguishable, but the entries conceal evidence recipients and the shared dependency, and assign unsupported or contradictory authority.

| Criterion / location | Result | Finding and necessary repair |
|---|---|---|
| A: release approval | Satisfied | Matches A's supplied release approval role. |
| B: measurement reports | Satisfied for role; failed for recipient coverage | Report provision is represented, but recipients A and C are absent. Add both recipient relationships. |
| C: release approval | Failed | Contradicts the explicit fact that C has no release authority. Remove this assignment and show the authority limit. |
| C: specifications | Satisfied for topic; needs precision for responsibility coverage | The label names the topic but does not explicitly identify specification checking. State that C checks specifications. |
| D: owned exclusively by B | Failed | Contradicts D being shared by B and C. Remove exclusive ownership and represent the shared calibration dependency of both teams. |
| D: calibration | Satisfied for responsibility | Matches instrument calibration; specify “instrument calibration” for fidelity to the source wording. |
| D: calibration-exception approval | Failed | The approver is not documented. Remove D's approval assignment and mark the responsibility as undocumented. The source gap is not evidence that D lacks this authority in reality. |

Necessary repairs take priority over presentation changes because the current map would misdirect release and exception decisions and obscure C's dependence on D. Showing recipient and shared-dependency links explicitly would make the map useful for the requested ownership-gap assessment; no procedural ordering is needed.

Validation status: the supplied map was manually checked against all supplied responsibilities, authority boundaries, report recipients, shared calibration relationships, and the documented gap. The proposed repairs have not been applied or revalidated. No external verification was performed.

# Reference-loading record

- Read `SKILL.md` as the entry point; selected focused outline/map procedures and preserved structure-only and review-only boundaries.
- Read `references/outline-context-exploration.md` to derive the working scope from the user's purpose: authority, evidence recipients, shared dependencies, and visible gaps. The prompt was clear enough to choose a table and explicit relationship notation without questions or a fixed profile.
- Read `references/outline-generation.md` for Task 1: use supplied elements, show missing authority, avoid invented dependencies and procedural ordering.
- Read `references/outline-review.md` for Task 2: located findings, consequences, and remedies without replacing the existing map.
- Read `references/outline-validation.md` for source fidelity and requirement coverage: bounded assessment, criterion outcomes, and explicit status of unapplied repairs.
- No external research, repository edits, or unrequested prose report.
