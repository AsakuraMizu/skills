# Testing

Tests should prove behavior, boundaries, and regression risks, not merely increase line coverage.

## `test-observable-behavior`

Prefer testing behavior through public APIs, user-visible output, or an external contract. Do not widen visibility merely to test private implementation details. Name tests after the behavior, scenario, or specification concept they verify.

## `regression-test-for-bug-fix`

Use existing regression coverage when it already detects the bug. Otherwise, add or adapt a minimal test that exercises the triggering input, state transition, interleaving, or resource lifetime and fails before the fix. When the failure cannot be reproduced reliably in a test, explain the limitation and use another repeatable verification method. Do not add a second test for behavior already protected by the same regression coverage.

## `boundary-and-error-cases`

Choose boundary and error cases from the contract affected by the change. Exercise supported inputs or state transitions where a plausible defect would change the observable result, such as arithmetic limits, partial failure, or cancellation when relevant. Reuse existing coverage and add only cases that protect a distinct regression risk.

## `assertions-not-printing`

Use assertion macros or test-framework checks instead of printing values for manual inspection. Failure messages should contain enough context to diagnose the failure without interaction.

## `deterministic-isolated-tests`

Keep tests deterministic, independent, and repeatable. Clean up files, descriptors, threads, child processes, temporary directories, registry entries, and background tasks. Do not depend on state left by another test. For concurrency tests, prefer controlled synchronization points, virtual time, or model checking over arbitrary sleeps and retry counts.

## `test-the-contract`

Tests should protect the public contract, critical invariants, and failure behavior. Do not test default values, log text, or a container type unless it is itself a stable contract.

## `verification-scope`

Run checks that match the change: start with a fast check for the affected crate or module, then run the broader suite required by the repository. Report the commands actually run and their results; do not overstate the verification scope.