# OpenSpec conventions
- **Change IDs**: verb-led kebab-case (`add-dark-mode`, `refactor-auth`, `remove-legacy-export`).
- **RFC-2119**: SHALL/MUST = mandatory, SHOULD = recommended, MAY = optional. Every requirement MUST use SHALL or MUST.
- **Scenario rule**: every `### Requirement:` MUST have at least one `#### Scenario:` in GIVEN/WHEN/THEN form.
- **Lifecycle**: propose (proposal/tasks/design/delta) -> validate -> apply (implement tasks) -> archive.
- **Archive merge**: on archive, ADDED requirements append to `specs/<domain>/spec.md`, MODIFIED replace the matching `### Requirement`, REMOVED delete it; the change folder moves to `changes/archive/YYYY-MM-DD-<id>/`. Use `openspec archive <id>` when the CLI is present.
- **Validation**: `openspec validate <id> --strict` (zero errors AND warnings); the native equivalent checks requirement keywords, scenarios, and unique delta sections.

## Repository setup
OpenSpec 1.5.0 initialized the directories using `openspec init --tools none`. This deliberately leaves Copilot configuration under this repository's own .github guidance. `openspec update` reports no configured tools in this mode; it is not a spec-validation failure.

The config retains the CLI-required `schema: spec-driven`, project identity, and stack. This is intentionally not the older two-key native-fallback config.

## Working example
`specs/example/spec.md` and `changes/add-example-capability/` are copy-me references, not an actual site capability or approved implementation request. Do not implement or archive the example automatically. Replace or delete the examples when creating the first real capability specification.

## Commands
- `openspec list` lists active changes, including the illustrative example.
- `openspec validate --all --strict --no-interactive` validates specifications and deltas.
- `openspec validate add-example-capability --strict --no-interactive` checks the example change alone.

<!-- generated-by: poppins · do not remove (poppins-commit re-adds it) -->