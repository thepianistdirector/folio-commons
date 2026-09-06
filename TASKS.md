# Folio Commons: proposed work packages

These are planning briefs. No task is complete or approved for automatic execution. Before implementation, maintainers must publish a scoped task revision with the actual repository, paths, tools and validation commands.

## W1-T1 — Specify the memo-sheet-slide model

**Wave:** W1 · **Status:** Planned · **Prerequisites:** None; begin with maintainer scope review

Model cells, paragraphs, charts, references and typed edit operations.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A single source value can be traced to its uses in a memo and a slide.
- Operations distinguish proposed changes from accepted document state.

## W1-T2 — Create compatibility and conflict fixtures

**Wave:** W1 · **Status:** Planned · **Prerequisites:** W1-T1

Build small examples of formulas, references, concurrent edits and broken links.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Each fixture declares expected round-trip behavior and unsupported features.
- Conflicting human and agent edits have a visible resolution outcome.

## W2-T1 — Build the source spreadsheet and linked memo

**Wave:** W2 · **Status:** Planned · **Prerequisites:** W1-T1, W1-T2

Implement the bounded cell model, formula subset and referenced text blocks.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Editing a source cell updates its declared dependents without changing unrelated content.
- Invalid formulas and missing references appear as errors rather than invented values.

## W2-T2 — Build the linked slide view

**Wave:** W2 · **Status:** Planned · **Prerequisites:** W1-T1, W1-T2

Render a small chart and narrative linked to the same source model.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- The displayed chart can be traced to its source cells.
- Users can change presentation without silently modifying the underlying data.

## W3-T1 — Implement change proposals and selective acceptance

**Wave:** W3 · **Status:** Planned · **Prerequisites:** W2-T1, W2-T2

Expose typed operations to a reference agent integration with a human review surface.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A user can accept one proposed edit and reject another independently.
- An agent cannot bypass the document's editing permissions.

## W3-T2 — Implement undo and concurrent edit recovery

**Wave:** W3 · **Status:** Planned · **Prerequisites:** W2-T1, W2-T2

Define operation history, offline changes and conflict resolution.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Undo restores the intended prior state without erasing another collaborator's unrelated work.
- Reconnect surfaces incompatible edits instead of silently overwriting them.

## W4-T1 — Publish the open package format

**Wave:** W4 · **Status:** Planned · **Prerequisites:** W3-T1, W3-T2

Export document structure, sources and revision metadata in a documented format.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A clean installation reopens the reference package with working links.
- The format has a versioned migration path and clear asset licensing metadata.

## W4-T2 — Implement a bounded external format bridge

**Wave:** W4 · **Status:** Planned · **Prerequisites:** W3-T1, W3-T2

Select a narrow import/export subset with explicit compatibility fixtures.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Supported fixtures round-trip without undisclosed semantic loss.
- Unsupported content is reported before a destructive conversion.

## W5-T1 — Test editing with diverse input needs

**Wave:** W5 · **Status:** Planned · **Prerequisites:** W4-T1, W4-T2

Evaluate keyboard navigation, screen reader output, zoom and non-color feedback.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Users can complete the reference edit-review-export workflow without a pointer.
- Observed barriers are fixed and retested on the affected flow.

## W5-T2 — Add self-hosted collaboration and recovery

**Wave:** W5 · **Status:** Planned · **Prerequisites:** W4-T1, W4-T2

Implement team access, backups and restoration for the supported package model.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- A restored workspace preserves permissions and document dependencies.
- Revoked collaborators cannot retrieve later document revisions.

## W6-T1 — Pilot reports with working teams

**Wave:** W6 · **Status:** Planned · **Prerequisites:** W5-T1, W5-T2

Observe a bounded set of real consented reports from source data to final export.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Record editing effort, compatibility failures and trust in proposed changes.
- Publish anonymized findings and revise scope before expanding formats.

## W6-T2 — Publish extension contracts and examples

**Wave:** W6 · **Status:** Planned · **Prerequisites:** W5-T1, W5-T2

Enable templates, renderers and agent clients without unrestricted document access.

Start only after the listed prerequisites and scope are accepted by a maintainer. Work in the project's own repository. Document assumptions, unresolved questions and reproducible evidence. This is a proposed work package, not a claim that the implementation already exists.

Acceptance criteria:

- Two independent extensions use the public contracts.
- A faulty extension can be disabled without losing editable document content.
