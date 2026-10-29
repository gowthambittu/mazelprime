## ADDED Requirements

### Requirement: Local-only preview label
The example preview SHALL identify its ready status as local-only so that it cannot be confused with confirmation of form delivery.

#### Scenario: Local status is labeled
- GIVEN the instructional sample preview is ready
- WHEN its status is displayed
- THEN the status includes a local-only label
- AND it does not claim that a discovery request was delivered

<!-- generated-by: poppins · do not remove (poppins-commit re-adds it) -->