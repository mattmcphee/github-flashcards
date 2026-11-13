# 2. Source control and repository governance

Topic map: [section 2](../topic-map.md#2-source-control-and-repository-governance). See the [objective index](README.md) for ID and flashcard reference rules.

## 2.1 Git fundamentals

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-02.01.001` | Commits, trees, blobs, references, and HEAD | Explain how commits, trees, blobs, references, and `HEAD` relate in Git's object and reference model. |
| `LO-02.01.002` | Branches, tags, and commit ancestry | Determine how branches and tags identify commits within a commit ancestry graph. |
| `LO-02.01.003` | Merge, rebase, cherry-pick, revert, and reset | Choose merge, rebase, cherry-pick, revert, or reset for a stated history-editing goal. |
| `LO-02.01.004` | Fast-forward versus three-way merges | Predict when integrating a branch permits a fast-forward and when it requires a merge commit. |
| `LO-02.01.005` | Merge conflicts and conflict resolution | Resolve a merge conflict while preserving the intended behaviour of both relevant changes. |
| `LO-02.01.006` | Signed commits and tags | Explain what verifying a signed commit or tag establishes and what it does not establish. |
| `LO-02.01.007` | Git hooks and their limitations | Explain why local Git hooks alone cannot enforce repository-wide policy. |

## 2.2 Enterprise branching strategies

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-02.02.001` | Trunk-based development | Describe an integration workflow that keeps the main branch releasable under trunk-based development. |
| `LO-02.02.002` | GitFlow | Trace feature, release, and hotfix changes through a GitFlow workflow. |
| `LO-02.02.003` | Feature branches | Explain the purpose and integration lifecycle of a feature branch. |
| `LO-02.02.004` | Release and hotfix branches | Choose a release or hotfix branch for a maintenance scenario. |
| `LO-02.02.005` | Short-lived versus long-lived branches | Compare the integration risks of short-lived and long-lived branches. |
| `LO-02.02.006` | Feature flags as an alternative to branching | Explain how feature flags separate code integration from exposing functionality. |
| `LO-02.02.007` | Branching strategies for high-frequency deployment | Select a branching strategy that supports frequent deployment and timely integration. |

## 2.3 Pull request governance

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-02.03.001` | Required reviews and approval thresholds | Choose review and approval requirements appropriate to the risk of a repository change. |
| `LO-02.03.002` | CODEOWNERS and ownership enforcement | Explain how `CODEOWNERS` contributes to review routing and how enforcement depends on repository controls. |
| `LO-02.03.003` | Required status checks | Explain how required status checks determine whether a proposed change can merge. |
| `LO-02.03.004` | Dismissing stale approvals | Identify when an earlier approval should become stale after a pull request changes. |
| `LO-02.03.005` | Preventing self-approval where supported | Identify platform controls that can separate change authorship from approval. |
| `LO-02.03.006` | Merge queues and merge trains | Explain how merge queues and merge trains validate changes against an evolving target branch. |
| `LO-02.03.007` | Squash, merge commit, and rebase strategies | Compare the resulting history of squash, merge-commit, and rebase integration strategies. |
| `LO-02.03.008` | Review of changes to pipeline configuration | Identify pipeline-definition changes that require security-sensitive review. |

## 2.4 Repository security and policy

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-02.04.001` | GitHub rulesets and branch protection | Compare GitHub rulesets and branch protection for enforcing repository change controls. |
| `LO-02.04.002` | Azure Repos branch policies | Select Azure Repos branch policies for a stated review and validation requirement. |
| `LO-02.04.003` | Tag protection and release immutability | Explain how tag protection supports trustworthy release identifiers. |
| `LO-02.04.004` | Repository visibility and permission boundaries | Determine who can read or change repository content from its visibility and permission model. |
| `LO-02.04.005` | Restricting force pushes and deletion | Explain the risks of force pushes and branch deletion on shared protected branches. |
| `LO-02.04.006` | Secret scanning and push protection | Distinguish detecting committed secrets from blocking secret introduction through push protection. |
| `LO-02.04.007` | Repository creation and lifecycle governance | Define ownership, access, and retirement checks for a repository lifecycle. |
| `LO-02.04.008` | Managing external collaborators | Choose access and review controls for an external collaborator. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [Pro Git](https://git-scm.com/book/en/v2)
- [GitHub Enterprise Cloud administration](https://docs.github.com/en/enterprise-cloud@latest/admin)
