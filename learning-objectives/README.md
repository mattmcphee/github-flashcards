# Learning objectives

This catalogue contains 665 learning objectives covering all 665 topic bullets in the [topic map](../topic-map.md), organised into 16 sections and 87 numbered subtopics. Each table row preserves the original topic label and states an observable learning outcome.

An objective describes what the learner should be able to demonstrate. It is not a flashcard answer. One objective may need several focused cards, especially when a topic lists related concepts or requires both explanation and application.

## Section index

| Section | Objectives |
| --- | --- |
| [1. CI/CD fundamentals](01-cicd-fundamentals.md) | 31 |
| [2. Source control and repository governance](02-source-control-and-repository-governance.md) | 30 |
| [3. GitHub Actions](03-github-actions.md) | 53 |
| [4. Azure DevOps and Azure Pipelines](04-azure-devops-and-azure-pipelines.md) | 58 |
| [5. Pipeline engineering and scripting](05-pipeline-engineering-and-scripting.md) | 40 |
| [6. Identity and secrets management](06-identity-and-secrets-management.md) | 36 |
| [7. Runner and pipeline security](07-runner-and-pipeline-security.md) | 45 |
| [8. Software supply-chain security](08-software-supply-chain-security.md) | 46 |
| [9. Testing and quality engineering](09-testing-and-quality-engineering.md) | 37 |
| [10. Artifacts, dependencies and versioning](10-artifacts-dependencies-and-versioning.md) | 36 |
| [11. Deployment strategies and release management](11-deployment-strategies-and-release-management.md) | 42 |
| [12. Infrastructure as Code and GitOps](12-infrastructure-as-code-and-gitops.md) | 38 |
| [13. Enterprise governance and compliance](13-enterprise-governance-and-compliance.md) | 48 |
| [14. Monitoring, reliability and troubleshooting](14-monitoring-reliability-and-troubleshooting.md) | 47 |
| [15. Developer experience and platform engineering](15-developer-experience-and-platform-engineering.md) | 39 |
| [16. Advanced enterprise scenarios and architecture](16-advanced-enterprise-scenarios-and-architecture.md) | 39 |

## Objective IDs

Use the format `LO-SS.TT.NNN`, for example `LO-03.02.007`:

- `LO` identifies a learning objective.
- `SS` is the two-digit section number at allocation.
- `TT` is the two-digit subtopic number within that section at allocation.
- `NNN` is the three-digit objective sequence within that subtopic, starting at `001`.

For example, `LO-03.02.007` covers the security differences between `pull_request` and `pull_request_target`. The initial allocation follows the bullet order in the topic map. IDs are case-sensitive and unique across the catalogue.

IDs are permanent reference keys once allocated. Keep an existing ID when clarifying wording without changing the assessed outcome, or when moving an objective to a different topic. The prefix records its original location; the objective's current heading and Topic column record its current placement.

Allocate the next unused sequence number when adding an objective. Do not renumber existing objectives to close gaps or match a reordered topic map. Do not reuse an ID for a different outcome.

When replacing, splitting, merging, or retiring an outcome, retain its old ID as a row marked **Retired**, with replacement IDs or a reason. Assign new IDs to materially different outcomes and update affected card references. New cards must reference active objectives.

## Referencing objectives from flashcards

Every flashcard must reference at least one active objective through a field named `LearningObjectiveIds` in its editable source. Preserve that field when defining the Anki note type or export mapping.

Store multiple IDs as a single space-separated list, with no duplicate IDs. For example:

```text
LearningObjectiveIds: LO-03.02.007 LO-07.03.001
```

This example links the comparison of pull request event security with identifying unsafe use of `pull_request_target`. It demonstrates reference syntax, not a complete card or import-file schema.

- Use the exact IDs, including their zero padding.
- Link only objectives actually assessed by the question and answer.
- Prefer one focused objective per card. Include multiple IDs when the same focused question genuinely assesses their relationship.
- Create multiple cards when an objective requires distinct facts, comparisons, or scenarios.
- Keep objective IDs in metadata so they need not appear in the study prompt.
- If an Anki note generates several cards, ensure the references are valid for each generated card. Split the note or record a card-specific mapping in the editable source when the cards assess different objectives.
- Before export, check that every card has references and that every referenced ID exists and is active.

The full field order, note type, and import settings will be documented when the first flashcard format is introduced.

## Sources and changing product behaviour

Each section includes primary reference starting points. The linked pages were checked on 2026-11-13. These links are research entry points, not a claim that every future card answer has been verified.

When writing a card, consult the specific documentation supporting its answer and retain that direct source link with the card source. Record an access date for changeable facts. Include the relevant platform, version, plan, or hosting model when it changes the answer.

Use the version selector in product documentation where available. For example, a PowerShell 7.5 reference alone does not establish Windows PowerShell 5.1 behaviour. Record the specification version when making claims about SLSA, and verify current DORA definitions rather than treating the topic map as a complete or permanent metric taxonomy.

Objectives about licensing, limits, security controls, and product capabilities intentionally require checking the applicable offering rather than memorising an unspecified universal rule.
