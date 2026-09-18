---
name: write-agents-md
description: Write or review repository-level AGENTS.md and coding-agent instructions, not personal or global rules.
---

# Write AGENTS.md

Write repository-level instructions that help an agent make correct decisions in that repository. This skill does not apply to personal or global agent rules.
An instruction file is not a repository encyclopedia, a second README, or a record of previous sessions.

## Establish scope and evidence

- Start with the user's requested scope and the instructions already available in context. Read the target file before editing; reuse prior research that remains applicable.
- Inspect code, configuration, CI, or documentation to resolve specific uncertainties about a proposed instruction. Do not inventory the repository merely to populate sections.
- Distinguish current implementation facts from intended policy. Verify facts against their owning source; preserve explicit user and project requirements even when code does not enforce them. Report material conflicts rather than silently choosing a new policy.
- Treat global instructions as inherited constraints; this skill covers only repository and in-repository directory scopes. Do not repeat inherited guidance without a local reason, and do not assume every agent tool discovers or combines instruction files the same way.
- Keep changes within the requested files. Adding nested instruction files, tool-specific mirrors, symlinks, or new reference documents is a separate scope decision, not routine setup.

## Select content by its effect

Keep information that changes a likely agent decision, prevents a recurring mistake, or records an explicit working agreement.
Typical candidates are non-obvious ownership boundaries, project-specific conventions, unusual setup constraints, and change-specific verification requirements.
They are candidates, not mandatory sections.

- State when a rule applies and what the agent should do. Add a short reason when it helps distinguish the rule from a plausible but wrong alternative.
- Use precise instructions rather than slogans such as "follow best practices" or "keep documentation updated." Avoid turning a narrow incident into an unconditional rule.
- Preserve the user's intended strength and scope. Do not weaken a required workflow into a suggestion, or promote an observed implementation detail into a permanent requirement.
- Prefer durable guidance. Omit session summaries, completed work, temporary test results, dependency inventories, and speculative warnings.
- Do not restate standard language conventions, mechanically enforced formatting rules, obvious directory structure, or ordinary tool usage unless the repository has a meaningful exception.
- Follow the repository's language and terminology. Examples or upstream templates are not evidence that this project uses their technologies, policies, or workflows.

## Reference existing knowledge

Give a specific repository-relative path and explain when it is relevant when an existing document or configuration already owns the details.
Inline a critical rule when it must be visible before an agent acts; link to longer procedures, API contracts, or design rationale instead of copying them.

Do not replace duplicated content with an exhaustive link directory.
A reference earns its place by answering a likely question or directing a concrete kind of work.
Keep stable architectural intent distinct from a snapshot of files, symbols, or dependencies.

## Describe workflows, not command catalogs

Do not create a commands section, command table, or build/test/lint checklist by default.
If task runners, CI, or development documentation already explain a workflow, point to the relevant entry rather than maintaining another catalog.

Include an exact command when its spelling resolves a real ambiguity, when an unusual invocation is easy to get wrong, or when the user explicitly requests it.
Include the working directory, environment, order, or prerequisites only when they affect correct execution.
For verification, capture the relationship between a kind of change and the checks it requires; a list of available checks alone does not express that relationship.

Use the smallest verification scope that actually covers the affected contract.
Retain project-wide or end-to-end requirements when the project needs them; do not mechanically replace them with file-scoped checks.
Verify command availability and semantics from repository evidence rather than inventing convenient variants.

## Edit and validate

Choose headings and prose, lists, or tables to fit the retained content.
There are no required sections, preferred section order, line quotas, or mandatory table formats.
Concision means removing unnecessary information, not compressing important reasoning into cryptic fragments.

When revising an existing file, preserve useful guidance and explicitly requested policies.
Remove repetition and stale facts, but do not delete an agreement merely because it is unusual or absent from a template.
Prefer focused edits unless a rewrite is needed to fix the organization.
Do not modify product documentation or executable configuration just to make the instruction file look consistent.

Before delivery, verify changed factual claims and references, and check for contradictions with applicable instructions.
Run a command only when its result resolves uncertainty about the instructions; a prose edit does not justify running the entire project workflow.
Review whether the result helps an agent choose the right action without recreating a manual or command inventory.
Report substantive changes and unresolved policy questions briefly; keep that explanation out of the instruction file.
