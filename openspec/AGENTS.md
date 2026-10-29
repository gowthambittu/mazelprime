# Spec-driven changes

Read the root AGENTS.md first. Follow [README.md](README.md) for the full conventions.

1. Propose a change under `changes/<verb-led-id>/` with proposal.md, tasks.md, and a delta at `specs/<capability>/spec.md`. Add design.md for non-trivial decisions.
2. Validate with `openspec validate <id> --strict --no-interactive`. Each requirement needs SHALL/MUST and at least one GIVEN/WHEN/THEN scenario.
3. Implement approved tasks and verify the resulting browser behavior. Deployment and live form submissions still require explicit approval.
4. Archive only completed real changes; merge their deltas into canonical specs first.

The example spec/change is instructional only, not a work order. Never backfill the whole existing application into speculative requirements or silently implement the example.

<!-- generated-by: poppins · do not remove (poppins-commit re-adds it) -->