# Example Preview Specification

## Purpose
This instructional capability demonstrates the required OpenSpec document structure using a hypothetical local preview status. It is not implemented by the website and must not be interpreted as a production requirement.

## Requirements

### Requirement: Preview status
The example preview SHALL display a ready status when its local sample page loads successfully.

#### Scenario: Happy path
- GIVEN the instructional sample page is available locally
- WHEN a developer loads the sample preview
- THEN a ready status is displayed
- AND no discovery request is transmitted

#### Scenario: Failure path
- GIVEN the instructional sample page cannot load
- WHEN a developer attempts to open the preview
- THEN no ready status is reported

<!-- generated-by: poppins · do not remove (poppins-commit re-adds it) -->