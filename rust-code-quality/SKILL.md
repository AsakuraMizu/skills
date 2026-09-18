---
name: rust-code-quality
description: Implement, refactor, or review Rust code and concrete Rust APIs. Also use for rustdoc and crate API documentation.
---

# Rust Code Quality

## Scope

Write Rust code that is easy to understand, maintain, and verify. Fix real problems without adding abstractions, copies, or complexity merely to satisfy a rule.

Work from the concrete code, API contract, or documentation being changed or reviewed.

Do not treat conventions from another project or specialized domain as universal Rust rules. The current repository's established conventions take precedence.

## Reference guide

Select references by the question being addressed:

- Structure, naming, visibility, or abstraction decisions: `references/maintainability.md`
- Types, traits, ownership, lifetimes, or public APIs: `references/api-and-types.md`
- Error handling, arithmetic, state transitions, or boundary semantics: `references/correctness.md`
- `unsafe`, pointers, FFI, layout, or untrusted input: `references/safety.md`
- Locks, atomics, threads, asynchronous tasks, or cancellation: `references/concurrency.md`
- Allocations, copies, hot paths, or measured performance issues: `references/performance.md`
- Regression risks, test design, or verification scope: `references/testing.md`
- Source comments, rustdoc, or crate/API documentation: `references/documentation.md`

## Using the guidance

Apply relevant guidance already present in the active conversation, including equivalent repository or system instructions. Follow-up turns do not require reloading it.

Read only references whose needed guidance is missing. Reload a previously read file only when it has changed or the necessary details are no longer available in context.

Use these guidelines to judge the actual contract, not as a fixed sequence of steps. Rust's language and memory-safety requirements remain binding.