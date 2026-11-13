# 3. GitHub Actions

Topic map: [section 3](../topic-map.md#3-github-actions). See the [objective index](README.md) for ID and flashcard reference rules.

## 3.1 Core GitHub Actions architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.01.001` | Events and workflow triggers | Explain how a GitHub event selects workflows for execution. |
| `LO-03.01.002` | Workflows, jobs, steps, and actions | Trace the relationship between workflows, jobs, steps, and actions in a workflow file. |
| `LO-03.01.003` | GitHub-hosted versus self-hosted runners | Compare GitHub-hosted and self-hosted runners for isolation and operational responsibility. |
| `LO-03.01.004` | Runner labels and groups | Distinguish runner labels used for selection from runner groups used for access organisation. |
| `LO-03.01.005` | Workflow execution lifecycle | Trace a workflow run from trigger evaluation through queuing, execution, and completion. |
| `LO-03.01.006` | Job isolation and execution contexts | Explain job isolation boundaries and identify how execution contexts expose data to steps and jobs. |
| `LO-03.01.007` | Workflow dependencies using needs | Determine job ordering and prerequisite outcomes from `needs` dependencies. |

## 3.2 Workflow triggering

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.02.001` | push, pull_request, workflow_dispatch | Choose `push`, `pull_request`, or `workflow_dispatch` for a stated execution requirement. |
| `LO-03.02.002` | workflow_call, workflow_run, repository_dispatch | Distinguish `workflow_call`, `workflow_run`, and `repository_dispatch` by their invocation contracts. |
| `LO-03.02.003` | Scheduled execution | Explain the scheduling conditions and timing limitations to check for a scheduled workflow. |
| `LO-03.02.004` | Branch, tag, and path filters | Predict whether branch, tag, and path filters permit a workflow to run. |
| `LO-03.02.005` | Trigger recursion and workflow chaining | Identify event and token conditions that permit or suppress a chained workflow run. |
| `LO-03.02.006` | Avoiding duplicate executions | Identify overlapping triggers that cause redundant runs for the same change. |
| `LO-03.02.007` | Security differences between pull_request and pull_request_target | Compare `pull_request` and `pull_request_target` by execution context and trust implications. |

## 3.3 Workflow logic and YAML

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.03.001` | Expressions and context objects | Select the appropriate GitHub Actions context and expression for a required value. |
| `LO-03.03.002` | Environment variables versus configuration variables | Distinguish environment variables from GitHub configuration variables by access syntax and scope. |
| `LO-03.03.003` | Job-level versus step-level configuration | Determine which job-level settings apply to a step and which settings a step overrides. |
| `LO-03.03.004` | Conditional execution using if | Evaluate an `if` expression using the relevant context and status conditions. |
| `LO-03.03.005` | Matrix strategies | Derive the job combinations produced by a matrix with inclusions and exclusions. |
| `LO-03.03.006` | Concurrency groups | Explain how concurrency group keys determine which workflow or job runs compete. |
| `LO-03.03.007` | Cancellation of redundant builds | Choose cancellation behaviour that removes redundant work without interrupting required deployments. |
| `LO-03.03.008` | Timeouts, retries, and exit codes | Distinguish timeout, retry, and exit-code handling when diagnosing a failed workflow. |

## 3.4 Reusability

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.04.001` | Composite actions | Identify when a composite action is suitable for sharing a sequence of steps. |
| `LO-03.04.002` | Reusable workflows | Describe the inputs, secrets, outputs, and jobs forming a reusable workflow's contract. |
| `LO-03.04.003` | Workflow templates | Explain how a workflow template supports initial setup and how later updates reach consumers. |
| `LO-03.04.004` | Organisation-shared automation | Choose a distribution and ownership model for organisation-shared automation. |
| `LO-03.04.005` | Cross-repository workflow consumption | Identify access and reference requirements for consuming a workflow from another repository. |
| `LO-03.04.006` | Versioning reusable components | Choose a versioning strategy that balances reproducibility with controlled component updates. |
| `LO-03.04.007` | Choosing composite actions versus reusable workflows | Choose a composite action or reusable workflow based on the required execution and reuse boundary. |

## 3.5 GitHub Actions security

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.05.001` | GITHUB_TOKEN permissions | Determine the minimum `GITHUB_TOKEN` permissions required by a workflow operation. |
| `LO-03.05.002` | Read-only versus write access | Identify operations that require write access rather than read-only repository access. |
| `LO-03.05.003` | Repository and environment secrets | Choose repository or environment secret scope for a stated deployment boundary. |
| `LO-03.05.004` | OIDC authentication | Trace the exchange of a GitHub OIDC identity token for external workload credentials. |
| `LO-03.05.005` | Action dependency pinning | Explain how pinning an action to an immutable revision reduces dependency substitution risk. |
| `LO-03.05.006` | Third-party action allowlisting | Define criteria for allowing a third-party action to run in an organisation. |
| `LO-03.05.007` | Script-injection attacks | Identify unsafe interpolation of untrusted workflow values into executable scripts. |
| `LO-03.05.008` | Untrusted pull request execution | Identify which resources must remain inaccessible when executing an untrusted pull request. |
| `LO-03.05.009` | Environment protection and deployment approvals | Explain how environment protections and approvals control access to deployment execution. |

## 3.6 Enterprise GitHub Actions infrastructure

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.06.001` | GitHub-hosted runners and larger runners | Choose between standard GitHub-hosted and larger runners using current capacity and feature requirements. |
| `LO-03.06.002` | Self-hosted runner registration and lifecycle | Describe secure registration, maintenance, and removal of a self-hosted runner. |
| `LO-03.06.003` | Ephemeral runners | Explain how ephemeral runner lifecycle choices limit cross-job persistence. |
| `LO-03.06.004` | Actions Runner Controller (ARC) | Describe the role of Actions Runner Controller in managing Kubernetes-based runner infrastructure. |
| `LO-03.06.005` | Runner scale sets | Explain how runner scale sets relate queued work to runner capacity. |
| `LO-03.06.006` | Network isolation and private networking | Identify private connectivity and isolation requirements for a workflow's dependencies. |
| `LO-03.06.007` | Runner groups and repository restrictions | Use runner groups and repository restrictions to define which repositories may use a runner pool. |
| `LO-03.06.008` | Enterprise workflow policies | Identify enterprise policy controls needed to govern workflow execution. |

## 3.7 Operational management

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-03.07.001` | Workflow debugging | Choose a debugging approach from a workflow's failing stage and available diagnostics. |
| `LO-03.07.002` | Run logs and step summaries | Use run logs and step summaries to distinguish execution evidence from high-level results. |
| `LO-03.07.003` | Cache and artifact management | Choose cache and artifact retention practices for speed, reproducibility, and storage control. |
| `LO-03.07.004` | GitHub Actions billing and usage | Identify the usage dimensions and current plan terms needed to estimate GitHub Actions cost. |
| `LO-03.07.005` | Concurrency and capacity limits | Distinguish concurrency limits from runner-capacity shortages when jobs queue. |
| `LO-03.07.006` | GitHub REST API and CLI automation | Choose a GitHub REST API or CLI operation to inspect or manage workflow runs. |
| `LO-03.07.007` | Workflow metrics and auditing | Select workflow metrics and audit events that demonstrate reliability and accountable changes. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [GitHub Actions documentation](https://docs.github.com/en/actions)
- [GitHub Actions secure use reference](https://docs.github.com/en/actions/reference/security/secure-use)
