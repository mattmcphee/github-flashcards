# 16. Advanced enterprise scenarios and architecture

Topic map: [section 16](../topic-map.md#16-advanced-enterprise-scenarios-and-architecture). See the [objective index](README.md) for ID and flashcard reference rules.

## 16.1 Enterprise architecture patterns

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-16.01.001` | Multi-organisation GitHub environments | Design governance and automation boundaries for an enterprise with multiple GitHub organisations. |
| `LO-16.01.002` | Multi-project Azure DevOps environments | Design shared administration and delivery controls across Azure DevOps projects. |
| `LO-16.01.003` | Shared CI/CD platform teams | Define the services and responsibilities owned by a shared CI/CD platform team. |
| `LO-16.01.004` | Hybrid GitHub and Azure DevOps architectures | Assign source control, build, and deployment responsibilities in a hybrid GitHub and Azure DevOps architecture. |
| `LO-16.01.005` | Cross-organisation automation | Identify identity, access, and ownership requirements for cross-organisation automation. |
| `LO-16.01.006` | Federated identity across tenants | Explain the trust configuration and permission boundaries required for identity federation across tenants. |
| `LO-16.01.007` | Multi-cloud deployment architectures | Compare shared and cloud-specific delivery components in a multi-cloud architecture. |

## 16.2 Highly regulated environments

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-16.02.001` | Segregation of duties | Assign incompatible release duties to separate identities in a regulated delivery workflow. |
| `LO-16.02.002` | Privileged deployment workflows | Define approval and execution controls for a privileged deployment workflow. |
| `LO-16.02.003` | Restricted production access | Identify controls that restrict direct production access while supporting necessary operations. |
| `LO-16.02.004` | Formal release approval processes | Specify the evidence and accountable decision required by a formal release approval. |
| `LO-16.02.005` | Audit evidence preservation | Define how release audit evidence remains attributable, complete, and retrievable. |
| `LO-16.02.006` | Change control integration | Integrate pipeline execution with an external change-control decision and record. |
| `LO-16.02.007` | Secure software provenance | Determine whether artifact provenance supports a required regulated-release assurance. |
| `LO-16.02.008` | Compliance-as-Code | Translate an applicable compliance control into an automated check and identify evidence requiring human review. |

## 16.3 Large-scale automation

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-16.03.001` | Thousands of repositories and pipelines | Identify bottlenecks when an automation design expands to thousands of repositories. |
| `LO-16.03.002` | API rate limiting | Design API request scheduling that respects rate limits and handles retries safely. |
| `LO-16.03.003` | Pipeline concurrency management | Choose concurrency controls that balance throughput, fairness, and deployment safety. |
| `LO-16.03.004` | Dynamic runner scaling | Define demand signals and lifecycle controls for dynamic runner scaling. |
| `LO-16.03.005` | Central policy distribution | Design a policy distribution process that detects incomplete application across a fleet. |
| `LO-16.03.006` | Fleet-wide workflow updates | Plan a staged workflow update across repositories with validation and recovery criteria. |
| `LO-16.03.007` | Security posture reporting | Aggregate security findings into a report that identifies risk and remediation ownership. |
| `LO-16.03.008` | Cost optimisation | Identify the largest delivery cost drivers and evaluate savings against performance and reliability. |

## 16.4 Platform migration

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-16.04.001` | Azure Pipelines to GitHub Actions | Map an Azure Pipeline's triggers, jobs, identities, and approvals to a GitHub Actions migration plan. |
| `LO-16.04.002` | GitHub Actions to Azure Pipelines | Map a GitHub Actions workflow's triggers, jobs, identities, and approvals to an Azure Pipelines migration plan. |
| `LO-16.04.003` | Classic to YAML pipelines | Identify behaviour and approvals that must be preserved when replacing a classic pipeline with YAML. |
| `LO-16.04.004` | Migrating secrets to federated identities | Plan a transition from stored credentials to federated authentication with validation and fallback criteria. |
| `LO-16.04.005` | Migrating shared templates | Map shared template contracts to the capabilities of a target automation platform. |
| `LO-16.04.006` | Replacing persistent build agents | Identify persistent agent dependencies that must be removed before adopting ephemeral execution. |
| `LO-16.04.007` | Preserving auditability through migration | Specify which historical run, approval, and artifact records must remain accessible after migration. |
| `LO-16.04.008` | Rollback and coexistence strategies | Define coexistence and rollback criteria for a staged CI/CD platform migration. |

## 16.5 Architectural decision-making

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-16.05.001` | When to choose GitHub Actions | Justify choosing GitHub Actions for a stated repository, integration, and governance context. |
| `LO-16.05.002` | When to choose Azure Pipelines | Justify choosing Azure Pipelines for a stated delivery, integration, and governance context. |
| `LO-16.05.003` | Running GitHub repositories with Azure Pipelines | Explain the integration and authorisation boundaries when Azure Pipelines builds a GitHub repository. |
| `LO-16.05.004` | Platform licensing and cost considerations | Compare platform costs using current licensing, execution, storage, and operational assumptions. |
| `LO-16.05.005` | Operational ownership | Assign ownership for platform administration, reusable automation, and incident response. |
| `LO-16.05.006` | Security feature availability | Verify whether required security controls are available for the proposed platform offering. |
| `LO-16.05.007` | Long-term maintainability | Evaluate a platform design's upgrade, staffing, and dependency maintenance burden. |
| `LO-16.05.008` | Avoiding unnecessary platform complexity | Identify architecture components that can be removed without losing a stated requirement. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [GitHub Enterprise Cloud administration](https://docs.github.com/en/enterprise-cloud@latest/admin)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
- [Azure Well-Architected safe deployment practices](https://learn.microsoft.com/en-us/azure/well-architected/operational-excellence/safe-deployments)
