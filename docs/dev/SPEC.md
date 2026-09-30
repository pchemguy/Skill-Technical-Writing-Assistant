# Technical Writing Assistant specification

## Purpose and authority

Implement the complete standalone `technical-writing-assistant` skill described in [CAPABILITY_MAP.md](CAPABILITY_MAP.md). The map governs capability boundaries, style policy, evidence modes, and contextual outline adaptation. The skill covers software documentation and scientific, technical, and professional writing, with an editing-first orientation and support for development from early material.

## Required behavior

- Preserve meaning, authorial position, essential reasoning, numerical factors, qualifications, and protected material during ordinary revision. Present substantive changes explicitly.
- Execute focused modules independently and composite workflows through the manager. Load only relevant resources; handoffs do not create routine approval gates.
- Implement all 21 references in the map with usable procedures, inputs, missing-information handling, outputs, completion checks, and examples or observable acceptance criteria.
- Retain exactly two evidence modes. Ask when evidence work is relevant and the mode is unresolved; reuse existing decisions. Without research, do not independently retrieve sources or treat model knowledge as verified.
- Diagnose composition across sentence, paragraph, section, and document levels. Prefer sound topic sentences; treat length heuristics as signals, not quotas.
- Generate, review, validate, and repair outlines/maps using contextual criteria, without a closed catalogue of specialized cases or mandatory schema.
- Apply software, scientific, and professional genre guidance without inventing behavior, results, requirements, or commitments.
- Deliver the requested artifact and material unresolved issues. Distinguish source inspection, external verification, software execution, and editorial checking.

## Package and portability

Use required Agent Skills frontmatter and relative Markdown references. All references are directly discoverable from SKILL.md. The core consists of instructions; it requires no executable code or specific service. External research and file-format operations use host facilities when available. OpenAI metadata is optional client presentation, separate from portable behavior. Do not claim installation or client execution from package validation.

## Acceptance and review

Check naming, frontmatter, contained links and anchors, resource inventory, presentation metadata, and absence of implementation scaffolds. Review every capability against the map. Exercise realistic focused, composite, outline, and negative tasks through fresh agent sessions where available; preserve raw outputs and assess them against explicit criteria. These samples do not establish reliability across all models, clients, or external sources.
