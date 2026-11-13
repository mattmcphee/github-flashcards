# 11. Deployment strategies and release management

Topic map: [section 11](../topic-map.md#11-deployment-strategies-and-release-management). See the [objective index](README.md) for ID and flashcard reference rules.

## 11.1 Continuous delivery architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-11.01.001` | Continuous delivery versus deployment | Distinguish continuous delivery from continuous deployment by the production release decision. |
| `LO-11.01.002` | Deployment pipelines | Identify the inputs, validation, and outputs of a deployment pipeline. |
| `LO-11.01.003` | Environment progression | Define promotion criteria between successive deployment environments. |
| `LO-11.01.004` | Development, test, staging, and production | Explain the distinct purposes of development, test, staging, and production environments. |
| `LO-11.01.005` | Approval gates | Choose an approval gate based on deployment risk and decision ownership. |
| `LO-11.01.006` | Change control | Identify the information needed to authorise and record a production change. |
| `LO-11.01.007` | Release orchestration | Sequence dependent releases across components while respecting their compatibility constraints. |

## 11.2 Deployment strategies

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-11.02.001` | In-place deployments | Explain the availability and recovery implications of an in-place deployment. |
| `LO-11.02.002` | Rolling deployments | Describe how a rolling deployment replaces instances while maintaining service capacity. |
| `LO-11.02.003` | Blue-green deployments | Explain how a blue-green deployment switches traffic between deployment environments. |
| `LO-11.02.004` | Canary deployments | Choose observation and progression criteria for a canary deployment. |
| `LO-11.02.005` | Feature flag deployments | Explain how feature flags control exposure independently of installing application code. |
| `LO-11.02.006` | Ring-based deployments | Choose deployment rings that progressively expose a change to suitable user groups. |
| `LO-11.02.007` | Progressive delivery | Define automated evidence and stopping conditions for progressive delivery. |

## 11.3 Production safeguards

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-11.03.001` | Manual and automated approvals | Choose manual or automated approval criteria for a deployment risk. |
| `LO-11.03.002` | Deployment windows | Explain how deployment windows balance operational readiness and delivery needs. |
| `LO-11.03.003` | Health checks | Choose health checks that demonstrate application behaviour after deployment. |
| `LO-11.03.004` | Automated rollback | Define an automatic rollback trigger and the evidence needed to avoid a false rollback. |
| `LO-11.03.005` | Roll-forward strategies | Choose when a corrective roll-forward is safer than restoring an earlier version. |
| `LO-11.03.006` | Deployment locks | Explain how deployment locks prevent unsafe concurrent changes. |
| `LO-11.03.007` | Separation of duties | Separate deployment preparation, approval, and execution responsibilities where required. |
| `LO-11.03.008` | Emergency deployment procedures | Define the authorisation and follow-up evidence required for an emergency deployment. |

## 11.4 Environment management

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-11.04.001` | Environment-specific configuration | Identify which configuration values should vary between environments. |
| `LO-11.04.002` | Configuration injection | Explain how configuration is supplied without rebuilding an environment-specific artifact. |
| `LO-11.04.003` | Secret references | Explain how secret references allow configuration to identify a secret without embedding its value. |
| `LO-11.04.004` | Infrastructure drift | Identify a difference between declared and actual infrastructure state. |
| `LO-11.04.005` | Environment parity | Choose which environment characteristics must match to make pre-production tests representative. |
| `LO-11.04.006` | Ephemeral environments | Define lifecycle and cleanup requirements for an ephemeral deployment environment. |
| `LO-11.04.007` | Production deployment protection | Identify access and execution controls that protect the production environment. |

## 11.5 Database and state management

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-11.05.001` | Database schema migrations | Choose a database schema migration sequence that supports the deployment plan. |
| `LO-11.05.002` | Backward-compatible changes | Identify a schema or API change that remains compatible with the previous application version. |
| `LO-11.05.003` | Expand-and-contract migrations | Explain the expand-and-contract sequence for safely replacing a data interface. |
| `LO-11.05.004` | Stateful application deployments | Identify persistent-state constraints that affect application deployment order. |
| `LO-11.05.005` | Data rollback limitations | Explain why reverting application code may not reverse a data migration. |
| `LO-11.05.006` | Coordinating application and database releases | Coordinate application and database releases so simultaneously running versions remain compatible. |

## 11.6 Release engineering

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-11.06.001` | Release candidates | Define the evidence required to designate a build as a release candidate. |
| `LO-11.06.002` | Artifact promotion | Explain how a validated artifact becomes eligible for release through promotion. |
| `LO-11.06.003` | Release notes | Write release-note criteria that capture user-visible changes and operational implications. |
| `LO-11.06.004` | Version traceability | Trace a released version to its source, build, and artifact identifiers. |
| `LO-11.06.005` | Deployment provenance | Identify evidence showing which actor or workflow deployed a particular artifact. |
| `LO-11.06.006` | Change records | Specify the change record needed to explain a release's purpose and authorisation. |
| `LO-11.06.007` | Incident-driven rollback decisions | Choose rollback criteria from incident symptoms, recovery options, and state compatibility. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [Azure Well-Architected safe deployment practices](https://learn.microsoft.com/en-us/azure/well-architected/operational-excellence/safe-deployments)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
