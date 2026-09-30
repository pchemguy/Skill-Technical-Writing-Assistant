# Forward task inputs

These tasks were given to fresh agent sessions with the package path, instructions to read SKILL.md and applicable references, and offline/no-repository-edit constraints. Each group wrote its actual responses and reference-loading record to a temporary file. The preserved outputs below are raw task artifacts, not ideal-answer fixtures or automated assertions. The reviewer evaluated them against the user requests and specification after execution. No live source research or supplied-code execution was requested in these trials.

## Professional group

[Actual responses](professional-trial.md).

1. “Shorten this decision memo for managers, keeping its reasoning and conditions: The rated package weighs 2 kg, of which 40% is active material. We estimate capacity using 2 kg × 0.4 × factor F, where F is provisional and has not been independently verified. A pilot involving 12 devices showed lower losses only under dry conditions. We recommend another pilot before committing to procurement. A June delivery is possible if testing passes; it is not approved or guaranteed.”
2. “Develop these planning bullets into a short professional project update: two prototypes tested; one failed in humid conditions; cause unknown; maybe redesign sealing; cost not estimated; launch date not approved. Preserve current uncertainty and do not add commitments.”
3. “Check only parallelism in this list and return the corrected sentence: The team is responsible for calibration, validating sensors, and to record readings.”

## Outline group

[Actual responses](outline-trial.md).

1. “Create a map showing who owns decisions and who provides evidence in this unfamiliar process. Use supplied facts only, and show gaps: Department A approves release. Team B supplies measurement reports to A and to Team C. Team C checks specifications but has no release authority. Team D is shared by B and C for instrument calibration. Responsibility for approving calibration exceptions is not documented. I want to spot ownership gaps and shared dependencies, not a procedural timeline.”
2. “Review and validate this existing map without regenerating it. Source facts are the same as Task 1. Map: A: release approval; B: measurement reports; C: release approval and specifications; D: owned exclusively by B, calibration and calibration-exception approval. Criterion: ownership and authority must match the supplied facts; all supplied responsibilities and recipient relationships must be represented.”

## Science/evidence group

[Actual responses](science-trial.md).

1. “Review and revise this scientific abstract using only supplied material, with no external research. Abstract: In 12 specimens, the treatment proved a significant improvement and is safe for all applications. Results supplied: treated mean 8.2, comparator mean 7.8; no variance, statistical tests, or adverse-event data supplied; measurements were made only at 20 °C. Preserve numbers and identify reporting gaps.”
2. “Assess evidence without external research. Claim: process cuts costs by 40%. Supplied source excerpt: median processing time was 40% lower in the trial. Additional reference is https://example.invalid/report, whose contents are not provided.”
3. “Review whether this conclusion is supported: Error rates fell after training, therefore training caused the decrease. No sources are provided. I have not selected whether you should independently research this.” For this separate task, return the next response rather than assume a user answer or research.

## Software/composition group

[Actual responses](software-trial.md).

1. “Review and revise these docs and Python docstring against the supplied code, using only supplied material. Docs: process_batch(items, batch_id) always commits atomically and returns an integer. All examples have been executed successfully. Code: async def process_batch(batch_id: str, batch_items: list[int]) -> None: await sink.begin_batch(batch_id); await sink.consume_results(batch_id, batch_items); await sink.finalize_batch(batch_id). No other implementation or test evidence is supplied. Docstring: Process batch. Args: items: Input data. Returns: int: Result ID. Use Google-style Python docstrings. Do not execute or change software.”
2. “Audit this composition without rewriting; offer organizing alternatives only if useful. Audience: engineers deciding whether to adopt a pilot method. Draft: Reliability is the main benefit. Installation takes two hours. The bracket is blue. Therefore the method is reliable. A ten-device pilot ran at 20 °C. The conclusion is that everyone should adopt it. Failures under humidity were not evaluated. Costs are unknown. Give located findings and priorities.”
3. “Independently verify this externally supplied claim: Version 9 supports protocol Z. For this task the host has no research or retrieval tools, and no source contents are supplied. Produce the next response rather than pretending to have checked sources.”

## Structural negative checks

On temporary repository copies, an added link to a nonexistent capability-map anchor was rejected with a missing-anchor error. Removing the routed outline-review reference was rejected with routing-mismatch and missing-target errors. The original repository was not mutated for these checks. They test integrity-check behavior, not writing quality.
