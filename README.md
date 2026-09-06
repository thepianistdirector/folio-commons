# Folio Commons

**Documents, spreadsheets and slides that people and AI can edit together, with every change inspectable.**

Your AI can write a report. Can you still see which cell changed, why the chart moved and where the claim came from?

![Folio Commons: aspirational concept, not an implemented product](assets/vision-concept.png)

> This is a public planning repository. There is no product implementation or playable build yet. The image is an AI-generated vision reference, not a screenshot. All waves and tasks are proposed; no completed work, community approval or funding is implied.

## The mission

Build an open collaborative office workspace where documents, sheets and slides share a portable structured model. Humans and agents should use the same understandable editing operations, with review, undo, source links and reliable export.

Change a source cell, see the linked report and slide update, inspect an agent's proposed edits and accept only what you want. Work locally, reconnect with collaborators and keep an editable copy in an open format.

## Who this is for

Teams producing reports, analyses and presentations, and developers building assistants that must make precise document changes.

## The first thing we want to prove

A small spreadsheet linked to a written memo and one slide. A human and an agent can propose edits, review them, undo them and reopen an exported package without losing the links.

File compatibility and collaboration semantics can consume the whole project. Start with a small declared format subset, test with real users and refuse to claim full office compatibility until it is demonstrated.

## What this could become

An interoperable office environment and document-operation standard, with domain templates, accessible editing, plugins and self-hosted collaboration.

Open office suites already exist. The proposal concentrates on shared structured operations and provenance across artifact types, so AI editing becomes inspectable collaboration rather than replacing a file with a new opaque version.

## Why build it together

Office users, spreadsheet experts, accessibility specialists, format engineers and connector authors can build templates, compatibility fixtures and precise editing tools.

We are looking for founding maintainers and contributors who can make one small, reviewable part real. Bring a concrete use case, a difficult test case, an interface sketch or a focused patch. If you use a coding agent, give it one agreed task and review its result. Accepted work matters more than generated volume.

## How to join

Start with [the project on Tanduna](https://tanduna.com/projects/folio-commons). Read the [six-wave roadmap](ROADMAP.md) and [twelve proposed tasks](TASKS.md), then join the planning discussion and say which result you can help deliver. Propose scope before starting overlapping implementation. GitHub holds the source; Tanduna is where we organize the project and its community.

- **W1: A shared model for editable work.** Define the smallest document graph and change language.
- **W2: One connected document package.** Implement the first useful cross-artifact workflow.
- **W3: Human and agent edits stay reviewable.** Prove collaboration and recovery.
- **W4: Keep the work portable.** Make export and reopening dependable.
- **W5: A workspace people can use daily.** Add accessibility and team operations.
- **W6: An open office ecosystem.** Validate adoption through real artifacts.

## What we are not promising

No promise of perfect import of every Office file, automatic factual correctness or unrestricted agent edits. Sensitive documents remain with their owner; hosted collaboration and inference have operating costs.

There is no delivery date, token target, paid offer or crowdfunding campaign here. Community interest does not guarantee a finished product. The next milestone depends on contributors, maintainer capacity and evidence from the previous one.

## Existing work we should learn from

- [LibreOffice](https://www.libreoffice.org/)

These are related foundations and references, not partners or endorsements. We should reuse compatible components or contribute upstream when that is the better route. This proposal does not claim that its individual ingredients are unprecedented. Dependencies and their licenses will be evaluated before adoption.

## License and contribution

This repository is published under [GNU AGPL-3.0](LICENSE). See [CONTRIBUTING.md](CONTRIBUTING.md) for the proposed contribution workflow and [the image note](assets/README.md) for concept provenance.
