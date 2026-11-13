# 1. CI/CD fundamentals

Topic map: [section 1](../topic-map.md#1-cicd-fundamentals). See the [objective index](README.md) for ID and flashcard reference rules.

## 1.1 Fundamental concepts

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-01.01.001` | Continuous Integration, Continuous Delivery, Continuous Deployment | Distinguish continuous integration, continuous delivery, and continuous deployment by their automation and production-release criteria. |
| `LO-01.01.002` | Differences between CI, CD, and release management | Explain how CI and CD activities contribute to release management without covering all release responsibilities. |
| `LO-01.01.003` | Source-to-production software delivery lifecycle | Trace a source change through build, validation, packaging, promotion, and production deployment. |
| `LO-01.01.004` | Pipeline as Code and declarative automation | Explain how version-controlled pipeline definitions make delivery automation reviewable and repeatable. |
| `LO-01.01.005` | Build automation versus deployment automation | Distinguish producing a build artifact from installing or activating that artifact in an environment. |
| `LO-01.01.006` | Shift-left testing and security | Identify testing and security checks that can move earlier in a delivery lifecycle. |
| `LO-01.01.007` | Trunk-based development versus GitFlow | Compare the integration frequency and branch structure of trunk-based development and GitFlow. |
| `LO-01.01.008` | DevOps, DevSecOps, and platform engineering | Distinguish the responsibilities and goals of DevOps, DevSecOps, and platform engineering. |

## 1.2 Pipeline architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-01.02.001` | Pipeline triggers, stages, jobs, steps, tasks, and actions | Relate triggers, stages, jobs, steps, tasks, and actions to their roles in a pipeline. |
| `LO-01.02.002` | Directed acyclic graphs (DAGs) | Explain why a pipeline dependency graph must not contain a cycle. |
| `LO-01.02.003` | Dependency graphs and execution ordering | Determine a valid execution order from a pipeline dependency graph. |
| `LO-01.02.004` | Parallel versus sequential execution | Choose parallel or sequential execution based on dependencies and shared resources. |
| `LO-01.02.005` | Build pipelines versus deployment pipelines | Distinguish build-pipeline outputs from deployment-pipeline outcomes. |
| `LO-01.02.006` | Pipeline orchestration and reusable components | Identify which orchestration responsibilities belong in a pipeline and which can be delegated to reusable components. |
| `LO-01.02.007` | Multi-stage and multi-environment pipelines | Map stages to validation and deployment responsibilities across multiple environments. |
| `LO-01.02.008` | Event-driven versus scheduled pipelines | Choose event-driven or scheduled execution for a stated automation requirement. |

## 1.3 Core engineering principles

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-01.03.001` | Build once, deploy many | Explain why promoting the same built artifact improves consistency across environments. |
| `LO-01.03.002` | Immutable build artifacts | Identify changes that would violate an artifact's immutability. |
| `LO-01.03.003` | Deterministic and reproducible builds | Identify uncontrolled inputs that prevent deterministic or reproducible builds. |
| `LO-01.03.004` | Pipeline idempotency | Predict whether repeating a pipeline operation will change its intended final state. |
| `LO-01.03.005` | Infrastructure and configuration immutability | Explain how replacing infrastructure or configuration differs from modifying it in place. |
| `LO-01.03.006` | Separation of build and release responsibilities | Assign build and release responsibilities to separate controls and owners. |
| `LO-01.03.007` | Fail-fast principles | Order checks to expose inexpensive, decisive failures early. |
| `LO-01.03.008` | Rollback versus roll-forward | Choose rollback or roll-forward given a failed deployment and its reversibility constraints. |

## 1.4 Enterprise architectural decisions

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-01.04.001` | Centralised versus decentralised CI/CD | Compare centralised and decentralised CI/CD ownership for governance and team independence. |
| `LO-01.04.002` | Monorepo versus multirepo | Compare monorepo and multirepo delivery implications for dependencies, permissions, and change coordination. |
| `LO-01.04.003` | Single pipeline versus multiple specialised pipelines | Choose a single pipeline or specialised pipelines for a given delivery workflow. |
| `LO-01.04.004` | Standardisation versus team autonomy | Identify which pipeline standards should be mandatory and which decisions teams can own. |
| `LO-01.04.005` | Hosted versus self-hosted execution | Choose hosted or self-hosted execution based on networking, control, and maintenance requirements. |
| `LO-01.04.006` | Trust boundaries between systems and environments | Locate trust boundaries in a delivery architecture and identify the data or authority crossing each boundary. |
| `LO-01.04.007` | Designing CI/CD for scalability and maintainability | Identify architectural bottlenecks and maintenance risks as repository and pipeline counts grow. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [DORA capabilities](https://dora.dev/capabilities/)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
