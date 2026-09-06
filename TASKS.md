# Folio Commons: task contracts

Twelve proposed work packages, with named waves and dependency order. None is completed by publishing this document. The linked Tanduna revision is the contribution authority; this repository records the maintainer's intended contract while Tanduna's structured requirement support is being updated.

Every task below names its repository, branch, verified planning commit, preferred model, allowed fallback, immutable public skills, task-specific testing procedure and maintainer acceptance flow. A later implementation task still needs its prerequisite code, a rebased execution revision, narrow file scope and real functional commands. Do not treat the current planning commit as if that future code exists.

The allowed model pair is GPT-6 Astra and Claude Fable 5.1, with the effort stated per task. A model declaration is not independent runtime evidence; unresolved proof remains visible to the maintainer. See [CONTRIBUTING.md](CONTRIBUTING.md) and [the machine-readable authored contracts](task-contracts.json).

## W1-T1 — Specify the memo-sheet-slide model

**Wave:** W1 · **Prerequisites:** None; maintainer scope review first

Model cells, paragraphs, charts, references and typed edit operations.

**Saved Tanduna task:** [W1-T1](https://tanduna.com/p/folio-commons/tasks/tsk_f8d1815785cce174ec31793111d99539)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Maintainer accepts the scoped design protocol; this is not product implementation.

**Preferred:** `gpt-6-astra` / medium. **Accepted fallback:** `claude-fable-5-1` / medium. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A single source value can be traced to its uses in a memo and a slide.
- Operations distinguish proposed changes from accepted document state.

### Testing procedure

Trace typed values from a source sheet into a memo and slide. Change one input, explain update propagation, and include a stale reference, cycle and unsupported formula in the model walkthrough.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W1-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W1-T2 — Create compatibility and conflict fixtures

**Wave:** W1 · **Prerequisites:** W1-T1

Build small examples of formulas, references, concurrent edits and broken links.

**Saved Tanduna task:** [W1-T2](https://tanduna.com/p/folio-commons/tasks/tsk_5c11367cee5234bbd0a3253fb197fadc)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Each fixture declares expected round-trip behavior and unsupported features.
- Conflicting human and agent edits have a visible resolution outcome.

### Testing procedure

Create fixtures for concurrent edits, unsupported formatting/formulas and broken links. Define preserved editable data and visible diagnostics for each, including a successful and lossy external-format example.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W1-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W2-T1 — Build the source spreadsheet and linked memo

**Wave:** W2 · **Prerequisites:** W1-T1, W1-T2

Implement the bounded cell model, formula subset and referenced text blocks.

**Saved Tanduna task:** [W2-T1](https://tanduna.com/p/folio-commons/tasks/tsk_df6acad51010093596d265814de910b6)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `claude-fable-5-1` / high. **Accepted fallback:** `gpt-6-astra` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Editing a source cell updates its declared dependents without changing unrelated content.
- Invalid formulas and missing references appear as errors rather than invented values.

### Testing procedure

Edit a source cell and inspect its formula and linked memo text. Break a reference and enter an unsupported formula; verify clear diagnostics and preservation of unrelated source content.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W2-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W2-T2 — Build the linked slide view

**Wave:** W2 · **Prerequisites:** W1-T1, W1-T2, W2-T1

Render a small chart and narrative linked to the same source model.

**Saved Tanduna task:** [W2-T2](https://tanduna.com/p/folio-commons/tasks/tsk_ef1b3343c4fe2dc1e607e14efc1c840e)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `claude-fable-5-1` / high. **Accepted fallback:** `gpt-6-astra` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- The displayed chart can be traced to its source cells.
- Users can change presentation without silently modifying the underlying data.

### Testing procedure

Change a source value and inspect the linked slide and editable source. Resize and navigate with keyboard; verify the displayed value is current and the slide has not become an uneditable image.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W2-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W3-T1 — Implement change proposals and selective acceptance

**Wave:** W3 · **Prerequisites:** W2-T1, W2-T2

Expose typed operations to a reference agent integration with a human review surface.

**Saved Tanduna task:** [W3-T1](https://tanduna.com/p/folio-commons/tasks/tsk_b049bda217180d6ac33c49b74d5db042)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `claude-fable-5-1` / high. **Accepted fallback:** `gpt-6-astra` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A user can accept one proposed edit and reject another independently.
- An agent cannot bypass the document's editing permissions.

### Testing procedure

Propose changes spanning a sheet, memo and slide. Accept one and reject another; compare unaffected artifacts and inspect source lineage with a second actor reviewing the same proposal.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W3-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W3-T2 — Implement undo and concurrent edit recovery

**Wave:** W3 · **Prerequisites:** W2-T1, W2-T2, W3-T1

Define operation history, offline changes and conflict resolution.

**Saved Tanduna task:** [W3-T2](https://tanduna.com/p/folio-commons/tasks/tsk_e3b1425fe23fefe86a431646f8748ce3)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Undo restores the intended prior state without erasing another collaborator's unrelated work.
- Reconnect surfaces incompatible edits instead of silently overwriting them.

### Testing procedure

Make concurrent changes from two actors, then undo one accepted edit. Verify the other actor's work survives; disconnect/reconnect and compare the recovered artifact graph.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W3-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W4-T1 — Publish the open package format

**Wave:** W4 · **Prerequisites:** W3-T1, W3-T2

Export document structure, sources and revision metadata in a documented format.

**Saved Tanduna task:** [W4-T1](https://tanduna.com/p/folio-commons/tasks/tsk_13d5641de4f57776808274ae1a381b0f)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A clean installation reopens the reference package with working links.
- The format has a versioned migration path and clear asset licensing metadata.

### Testing procedure

Export the native package and reopen in a clean workspace. Compare types, formulas, links, formatting and attribution; exercise an unsupported version and missing referenced artifact.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W4-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W4-T2 — Implement a bounded external format bridge

**Wave:** W4 · **Prerequisites:** W3-T1, W3-T2, W4-T1

Select a narrow import/export subset with explicit compatibility fixtures.

**Saved Tanduna task:** [W4-T2](https://tanduna.com/p/folio-commons/tasks/tsk_0f549bda0829135a70617f971fc4adf8)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Supported fixtures round-trip without undisclosed semantic loss.
- Unsupported content is reported before a destructive conversion.

### Testing procedure

Round-trip the declared supported subset through the external format. Include one unsupported feature and verify an explicit loss/unsupported report without claiming full format fidelity.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W4-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W5-T1 — Test editing with diverse input needs

**Wave:** W5 · **Prerequisites:** W4-T1, W4-T2

Evaluate keyboard navigation, screen reader output, zoom and non-color feedback.

**Saved Tanduna task:** [W5-T1](https://tanduna.com/p/folio-commons/tasks/tsk_173ddfa47406ff8302ce3e188c44b487)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `claude-fable-5-1` / high. **Accepted fallback:** `gpt-6-astra` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Users can complete the reference edit-review-export workflow without a pointer.
- Observed barriers are fixed and retested on the affected flow.

### Testing procedure

Complete selecting, editing, reviewing and undoing across all three artifact types using each claimed input/accessibility mode. Retain observed barriers and corrections, including keyboard-only review.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W5-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W5-T2 — Add self-hosted collaboration and recovery

**Wave:** W5 · **Prerequisites:** W4-T1, W4-T2

Implement team access, backups and restoration for the supported package model.

**Saved Tanduna task:** [W5-T2](https://tanduna.com/p/folio-commons/tasks/tsk_4078e501aad6a6d1da387b6ac9eb9220)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- A restored workspace preserves permissions and document dependencies.
- Revoked collaborators cannot retrieve later document revisions.

### Testing procedure

Have a second operator install the collaboration service, edit with two users and restore a disposable backup. Compare restored links and accepted changes; exercise interrupted save recovery.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W5-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W6-T1 — Pilot reports with working teams

**Wave:** W6 · **Prerequisites:** W5-T1, W5-T2

Observe a bounded set of real consented reports from source data to final export.

**Saved Tanduna task:** [W6-T1](https://tanduna.com/p/folio-commons/tasks/tsk_cea6b6913209ce77e89af7160d3c4cd8)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Record editing effort, compatibility failures and trust in proposed changes.
- Publish anonymized findings and revise scope before expanding formats.

### Testing procedure

Observe a consented working team preparing a real bounded report. Track stale-data errors, correction time, review decisions and export friction; publish only sanitized evidence and actual usage.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

This task uses the saved reproducible manual protocol. Distinguish paper/synthetic exercises from actual participant or physical observations.

**Evidence artifact:** `docs/work/W6-T1/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.

## W6-T2 — Publish extension contracts and examples

**Wave:** W6 · **Prerequisites:** W5-T1, W5-T2

Enable templates, renderers and agent clients without unrestricted document access.

**Saved Tanduna task:** [W6-T2](https://tanduna.com/p/folio-commons/tasks/tsk_81bfa47a382037709147475df9227b28)

**Repository:** [https://github.com/thepianistdirector/folio-commons](https://github.com/thepianistdirector/folio-commons) · **Branch:** `main`

**Planning base commit:** [`8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2`](https://github.com/thepianistdirector/folio-commons/commit/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2)

**Execution gate:** Prerequisite results must be accepted and integrated. Maintainer publishes a new task revision against that integrated base before execution; runtime work also needs the real harness and exact allowed paths.

**Preferred:** `gpt-6-astra` / high. **Accepted fallback:** `claude-fable-5-1` / high. Other models require a maintainer revision before work.

**Required skills:** [contribution protocol](https://raw.githubusercontent.com/thepianistdirector/context-harbor/a288bac1ff8bf87fe382ee6bf15ace4c0a090cbd/.agents/skills/tanduna-contribution/SKILL.md) and [Folio Commons validation](https://raw.githubusercontent.com/thepianistdirector/folio-commons/8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2/.agents/skills/folio-commons-validation/SKILL.md), at the linked immutable versions.

### Acceptance criteria

- Two independent extensions use the public contracts.
- A faulty extension can be disabled without losing editable document content.

### Testing procedure

Build a second extension from the published contract and run valid, malformed and incompatible-version examples. Verify it preserves typed editable content and reports unsupported capabilities.

Record setup/fixtures, actions, expected and observed results, relevant logs or artifacts, and PASS / FAIL / NOT RUN for each criterion.

Existing baseline checks (repository root; identity and patch hygiene only):

```sh
git rev-parse HEAD
git status --short
git diff --check 8d5b3044dcc43c9ea79743d0139f6f8f6f0f4af2
```

Exact functional commands, fixtures and paths must be ratified in the execution revision once the prerequisite-selected stack/harness exists. Do not claim these future checks ran.

**Evidence artifact:** `docs/work/W6-T2/acceptance.md` plus the actual patch, fixtures and logs within the approved task scope.

### Acceptance workflow

1. Contributor identifies the saved Tanduna task revision, repository/base, accepted prerequisites, selected primary or fallback model and effort, and exact required skill versions.
2. Contributor performs the task-specific testing procedure and maps each original acceptance criterion to setup, expected result, observed result and reproducible evidence. Failed and unrun checks remain visible.
3. Maintainer reproduces the material checks, reviews the scoped patch or design artifact and verifies the stated model/skill evidence. Unsupported model claims or missing evidence remain unresolved rather than accepted automatically.
4. Maintainer records acceptance or requested changes against the reviewed revision. A passing format check, generated patch or completed model invocation does not by itself satisfy the task.
