# Folio Commons roadmap

This is a public planning repository. There is no product implementation or playable build yet. The image is an AI-generated vision reference, not a screenshot. All waves and tasks are proposed; no completed work, community approval or funding is implied.

The order reflects dependencies, not calendar commitments. Each wave advances only when its stated outcome is demonstrated and a maintainer accepts the next scope. Capacity targets are hypotheses to test.

## W1 — A shared model for editable work

Define the smallest document graph and change language.

- **W1-T1: Specify the memo-sheet-slide model.** Model cells, paragraphs, charts, references and typed edit operations.
- **W1-T2: Create compatibility and conflict fixtures.** Build small examples of formulas, references, concurrent edits and broken links.

## W2 — One connected document package

Implement the first useful cross-artifact workflow.

- **W2-T1: Build the source spreadsheet and linked memo.** Implement the bounded cell model, formula subset and referenced text blocks.
- **W2-T2: Build the linked slide view.** Render a small chart and narrative linked to the same source model.

## W3 — Human and agent edits stay reviewable

Prove collaboration and recovery.

- **W3-T1: Implement change proposals and selective acceptance.** Expose typed operations to a reference agent integration with a human review surface.
- **W3-T2: Implement undo and concurrent edit recovery.** Define operation history, offline changes and conflict resolution.

## W4 — Keep the work portable

Make export and reopening dependable.

- **W4-T1: Publish the open package format.** Export document structure, sources and revision metadata in a documented format.
- **W4-T2: Implement a bounded external format bridge.** Select a narrow import/export subset with explicit compatibility fixtures.

## W5 — A workspace people can use daily

Add accessibility and team operations.

- **W5-T1: Test editing with diverse input needs.** Evaluate keyboard navigation, screen reader output, zoom and non-color feedback.
- **W5-T2: Add self-hosted collaboration and recovery.** Implement team access, backups and restoration for the supported package model.

## W6 — An open office ecosystem

Validate adoption through real artifacts.

- **W6-T1: Pilot reports with working teams.** Observe a bounded set of real consented reports from source data to final export.
- **W6-T2: Publish extension contracts and examples.** Enable templates, renderers and agent clients without unrestricted document access.

See [TASKS.md](TASKS.md) for observable acceptance criteria.
