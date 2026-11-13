# 12. Infrastructure as Code and GitOps

Topic map: [section 12](../topic-map.md#12-infrastructure-as-code-and-gitops). See the [objective index](README.md) for ID and flashcard reference rules.

## 12.1 IaC fundamentals

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-12.01.001` | Declarative versus imperative infrastructure | Compare declarative and imperative infrastructure definitions by how they express the desired result. |
| `LO-12.01.002` | Desired-state configuration | Explain how a desired-state definition is compared with deployed resources. |
| `LO-12.01.003` | Infrastructure drift | Identify infrastructure drift and distinguish authorised changes from unexpected divergence. |
| `LO-12.01.004` | Immutable infrastructure | Explain how replacing infrastructure supports an immutable operating model. |
| `LO-12.01.005` | Infrastructure testing | Choose static, integration, or policy tests for an infrastructure change. |
| `LO-12.01.006` | State management | Explain why an IaC tool may need state and how that state affects change planning. |
| `LO-12.01.007` | Change approval and auditing | Identify approval and audit evidence required for an infrastructure change. |

## 12.2 IaC technologies

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-12.02.001` | Terraform | Explain how Terraform configuration, providers, state, and plans contribute to infrastructure management. |
| `LO-12.02.002` | OpenTofu | Explain how OpenTofu configuration, providers, state, and plans contribute to infrastructure management. |
| `LO-12.02.003` | Azure Bicep | Explain the role of Azure Bicep in declaring Azure resources. |
| `LO-12.02.004` | ARM templates | Explain the structure and deployment role of an ARM template. |
| `LO-12.02.005` | PowerShell automation | Identify when PowerShell automation is appropriate for an infrastructure operation. |
| `LO-12.02.006` | Ansible | Explain how Ansible playbooks and inventories describe configuration work on target systems. |
| `LO-12.02.007` | Kubernetes manifests | Explain how Kubernetes manifests describe resources submitted to a cluster. |
| `LO-12.02.008` | Helm | Explain how Helm charts and values package configurable Kubernetes resources. |

## 12.3 IaC pipelines

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-12.03.001` | Validate, plan, and apply | Distinguish the checks performed during IaC validation, planning, and application. |
| `LO-12.03.002` | Pull request plan review | Identify destructive or unexpected resource changes in a proposed infrastructure plan. |
| `LO-12.03.003` | Securing state files | Identify the confidentiality and access requirements of an infrastructure state file. |
| `LO-12.03.004` | State locking | Explain how state locking prevents conflicting infrastructure operations. |
| `LO-12.03.005` | Secrets management | Identify secret exposure risks in IaC definitions, state, plans, and logs. |
| `LO-12.03.006` | Production approval controls | Choose production approval controls for an infrastructure plan. |
| `LO-12.03.007` | Automated drift detection | Define how automated drift detection should report and route unexpected changes. |
| `LO-12.03.008` | Destroy operations and safeguards | Identify the scope and authorisation checks required before destroying infrastructure. |

## 12.4 GitOps

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-12.04.001` | Git as a desired-state source | Explain how a version-controlled declaration serves as the desired-state source for GitOps. |
| `LO-12.04.002` | Pull-based versus push-based deployment | Compare pull-based reconciliation with a pipeline pushing changes to a target. |
| `LO-12.04.003` | Reconciliation loops | Explain how a reconciliation loop detects and attempts to correct state divergence. |
| `LO-12.04.004` | Argo CD and Flux | Compare Argo CD and Flux using a stated reconciliation and operational requirement. |
| `LO-12.04.005` | GitOps repository models | Choose a GitOps repository layout based on application ownership and environment boundaries. |
| `LO-12.04.006` | Drift correction | Choose whether a detected drift requires reconciliation or an authorised desired-state update. |
| `LO-12.04.007` | GitOps security boundaries | Identify the trust boundaries between Git repositories, reconcilers, and deployment targets. |

## 12.5 Enterprise Azure integration

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-12.05.001` | Azure landing zones | Explain the role of an Azure landing zone in providing a governed deployment foundation. |
| `LO-12.05.002` | Subscription vending | Describe the checks needed when provisioning a subscription through a vending process. |
| `LO-12.05.003` | Management groups and subscriptions | Relate management groups and subscriptions to Azure governance scope. |
| `LO-12.05.004` | Azure Policy | Explain how Azure Policy evaluates or enforces resource configuration requirements. |
| `LO-12.05.005` | RBAC as Code | Represent a required Azure role assignment as a reviewable infrastructure change. |
| `LO-12.05.006` | Entra ID workload identities | Choose an Entra workload identity for an Azure infrastructure deployment. |
| `LO-12.05.007` | Infrastructure deployment permissions | Determine the minimum resource scopes and permissions required by an infrastructure deployment. |
| `LO-12.05.008` | Policy compliance checks | Place policy compliance checks at appropriate points before and after infrastructure changes. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [OpenGitOps principles](https://opengitops.dev/)
- [Azure landing zones](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/)
