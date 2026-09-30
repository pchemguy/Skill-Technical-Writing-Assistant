# Technical Writing Assistant

A modular agent skill for scientific, technical, software, and professional writing. Its primary use is reviewing and revising existing material for clarity, structure, terminology, style, composition, and consistency while preserving technical meaning and authorial intent.

The planned skill also supports transforming bullets and early brainstorming into developed text, exploring compositional alternatives, challenging arguments and assumptions, and identifying evidence needs. Evidence work has two modes: independent external research and verification, or review using supplied material and model knowledge without external research.

## Status

**Design and skeleton stage.** The capability decomposition and composite workflows are documented. The standalone skill contains an entry point, 17 reference scaffolds, and optional OpenAI presentation metadata. Reference files establish scope and contracts; detailed procedures, behavioral acceptance cases, and end-to-end validation remain future work. This is not a fully implemented or behaviorally validated writing assistant.

## Project contents

- [Capability map](docs/dev/CAPABILITY_MAP.md): design rationale, scope, boundaries, style policy, evidence modes, and practical composite workflows.
- [Skill entry point](technical-writing-assistant/SKILL.md): invocation guidance and direct reference routing.
- [Workflow manager](technical-writing-assistant/references/manager.md): evidence-mode selection and composite workflow scaffolding.
- [Focused references](technical-writing-assistant/references/): independently loadable workflow contracts and shared editorial guidance.

The standalone package is `technical-writing-assistant/`. Its core uses Markdown and standard Agent Skills frontmatter; `agents/openai.yaml` is optional client-specific presentation metadata. The repository does not install the skill into any client. External research requires suitable tools supplied by the host; no particular connector is required.
