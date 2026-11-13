# 13. Enterprise governance and compliance

Topic map: [section 13](../topic-map.md#13-enterprise-governance-and-compliance). See the [objective index](README.md) for ID and flashcard reference rules.

## 13.1 Enterprise governance architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-13.01.001` | Enterprise versus organisation versus repository controls | Identify which governance decisions belong at enterprise, organisation, or repository scope. |
| `LO-13.01.002` | Centralised governance models | Explain the responsibilities and bottlenecks of a centralised governance model. |
| `LO-13.01.003` | Delegated administration | Define the authority and accountability delegated to a project or repository administrator. |
| `LO-13.01.004` | Policy inheritance | Determine how inherited policies affect a lower-level administrative scope. |
| `LO-13.01.005` | Standardised repository baselines | Define a repository baseline with measurable security and maintenance requirements. |
| `LO-13.01.006` | Repository ownership and accountability | Identify the owner accountable for access, changes, and retirement of a repository. |
| `LO-13.01.007` | Governance exceptions and their lifecycle | Define approval, expiry, and review stages for a governance exception. |

## 13.2 Enterprise GitHub governance

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-13.02.001` | Enterprise and organisation policies | Identify the GitHub enterprise or organisation scope suitable for a policy. |
| `LO-13.02.002` | Repository rulesets | Choose repository rulesets that express a required change-control standard. |
| `LO-13.02.003` | GitHub Actions execution policies | Select GitHub Actions policies that constrain permitted workflow execution. |
| `LO-13.02.004` | Required workflow controls | Identify supported controls for requiring workflow validation under a stated GitHub plan and repository configuration. |
| `LO-13.02.005` | Restricting third-party actions | Define an approval policy for third-party actions and reusable dependencies. |
| `LO-13.02.006` | Approved workflow templates | Explain how approved workflow templates support consistent onboarding and what ongoing enforcement they require. |
| `LO-13.02.007` | Repository custom properties | Use repository custom properties to classify repositories for governance decisions. |
| `LO-13.02.008` | Enterprise audit logging | Identify enterprise audit events needed to investigate a policy or access change. |
| `LO-13.02.009` | GitHub Apps governance | Define installation, permission review, ownership, and retirement requirements for a GitHub App. |

## 13.3 Azure DevOps governance

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-13.03.001` | Organisation and project security | Assign Azure DevOps organisation and project permissions according to administrative responsibilities. |
| `LO-13.03.002` | Project-scoped identities | Explain how project-scoped identities limit a pipeline's access boundary. |
| `LO-13.03.003` | Branch policies | Choose branch policies that enforce review and validation requirements. |
| `LO-13.03.004` | Centrally managed extends templates | Explain how centrally maintained `extends` templates constrain consuming pipelines. |
| `LO-13.03.005` | Required template checks | Identify protected resources that should require an approved template. |
| `LO-13.03.006` | Protected service connections | Define access and checks for a production service connection. |
| `LO-13.03.007` | Agent pool authorisation | Determine which projects and pipelines may use an agent pool. |
| `LO-13.03.008` | Pipeline permissions | Separate permission to edit a pipeline from permission to use its protected resources. |
| `LO-13.03.009` | Disabling unused classic pipeline capabilities | Identify unused classic pipeline capabilities that can be disabled after checking existing consumers. |

## 13.4 Compliance and auditing

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-13.04.001` | Audit log retention | Choose audit retention requirements from the organisation's investigation and evidence needs. |
| `LO-13.04.002` | Deployment traceability | Trace a deployment back to its change, approval, source, and artifact. |
| `LO-13.04.003` | Evidence collection | Identify evidence needed to demonstrate that a specified delivery control operated. |
| `LO-13.04.004` | Change management | Describe how a delivery change moves through the organisation's change-management process. |
| `LO-13.04.005` | Security control enforcement | Distinguish a documented security policy from evidence of its technical enforcement. |
| `LO-13.04.006` | Least privilege and separation of duties | Evaluate a delivery workflow for excessive privilege and incompatible responsibilities. |
| `LO-13.04.007` | Policy exception reviews | Assess whether a policy exception remains justified at its review date. |
| `LO-13.04.008` | Regulatory compliance considerations | Identify which delivery evidence must be mapped to an organisation's applicable regulatory requirements. |

## 13.5 Enterprise policy design

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-13.05.001` | Policy-as-Code | Translate a governance requirement into a version-controlled executable policy. |
| `LO-13.05.002` | Centrally enforced security baselines | Choose security requirements that should be enforced centrally. |
| `LO-13.05.003` | Version-controlled policies | Explain how review and version history make policy changes accountable. |
| `LO-13.05.004` | Gradual rollout of stricter requirements | Design a staged policy rollout with impact assessment and enforcement criteria. |
| `LO-13.05.005` | Exception management | Define a process for requesting and retiring policy exceptions. |
| `LO-13.05.006` | Monitoring policy drift | Detect differences between the intended policy baseline and deployed controls. |
| `LO-13.05.007` | Measuring compliance adoption | Choose measures that show policy adoption and unresolved compliance gaps. |

## 13.6 Organisation-wide automation

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-13.06.001` | GitHub REST and GraphQL APIs | Choose GitHub REST or GraphQL APIs for a stated administration query or mutation. |
| `LO-13.06.002` | Azure DevOps REST APIs | Identify an Azure DevOps REST API operation needed for an administration task. |
| `LO-13.06.003` | GitHub CLI and Azure DevOps CLI | Choose GitHub CLI or Azure DevOps CLI for a platform-specific automation task. |
| `LO-13.06.004` | Automated repository provisioning | Define the inputs and baseline settings required to provision a repository. |
| `LO-13.06.005` | Automated branch policy configuration | Design a repeatable operation that applies branch policies without unintended changes. |
| `LO-13.06.006` | Repository security audits | Select evidence for an automated repository security audit. |
| `LO-13.06.007` | Organisation-wide compliance reporting | Aggregate repository findings into an organisation-wide report with accountable owners. |
| `LO-13.06.008` | Automated remediation and its safeguards | Define scope limits, review, and recovery controls for automated remediation. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [GitHub Enterprise Cloud administration](https://docs.github.com/en/enterprise-cloud@latest/admin)
- [Azure Pipelines security](https://learn.microsoft.com/en-us/azure/devops/pipelines/security/overview?view=azure-devops)
- [Azure landing zones](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/)
