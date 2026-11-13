# 14. Monitoring, reliability and troubleshooting

Topic map: [section 14](../topic-map.md#14-monitoring-reliability-and-troubleshooting). See the [objective index](README.md) for ID and flashcard reference rules.

## 14.1 CI/CD observability

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-14.01.001` | Pipeline execution metrics | Select pipeline metrics that answer a stated operational question. |
| `LO-14.01.002` | Build success and failure rates | Calculate build success and failure rates from clearly defined run outcomes. |
| `LO-14.01.003` | Execution duration | Interpret execution duration separately from time spent waiting for execution. |
| `LO-14.01.004` | Queue wait times | Use queue wait time to identify scheduling or capacity problems. |
| `LO-14.01.005` | Runner utilisation | Interpret runner utilisation alongside workload demand and queue length. |
| `LO-14.01.006` | Deployment success rates | Calculate deployment success rates using an explicit definition of a deployment attempt. |
| `LO-14.01.007` | Failure categorisation | Classify failures so recurring causes can be investigated consistently. |
| `LO-14.01.008` | Logging and tracing | Correlate logs and traces across pipeline stages and external services. |

## 14.2 DORA and delivery performance

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-14.02.001` | Deployment frequency | Calculate deployment frequency for a defined service and measurement interval. |
| `LO-14.02.002` | Change lead time | Determine change lead time from the selected source-change and production-deployment timestamps. |
| `LO-14.02.003` | Change failure rate | Calculate change failure rate using a stated definition of a failed production change. |
| `LO-14.02.004` | Failed deployment recovery time | Determine failed deployment recovery time from the failure and recovery events. |
| `LO-14.02.005` | Reliability and operational stability | Explain how service reliability measures complement delivery performance metrics. |
| `LO-14.02.006` | Using metrics without incentivising poor behaviour | Identify incentives that could improve a reported metric while worsening delivery outcomes. |

## 14.3 Pipeline troubleshooting

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-14.03.001` | YAML parsing errors | Locate a YAML parsing error using its reported position and surrounding structure. |
| `LO-14.03.002` | Trigger evaluation failures | Trace why a configured trigger did not match an observed event. |
| `LO-14.03.003` | Permission-denied errors | Distinguish an authentication failure from an authenticated request denied by permissions. |
| `LO-14.03.004` | Missing variables and secrets | Determine whether a missing value results from definition, scope, or access restrictions. |
| `LO-14.03.005` | Authentication and OIDC failures | Identify the issuer, audience, subject, or permission mismatch behind an OIDC authentication failure. |
| `LO-14.03.006` | Dependency restoration failures | Diagnose dependency restoration failure using source, authentication, version, and network evidence. |
| `LO-14.03.007` | Agent compatibility issues | Identify an agent operating-system or tool-version incompatibility from job output. |
| `LO-14.03.008` | Resource exhaustion | Distinguish CPU, memory, disk, and process-limit exhaustion using available diagnostics. |
| `LO-14.03.009` | Network connectivity problems | Isolate a network failure to name resolution, routing, transport, or service response. |
| `LO-14.03.010` | Intermittent failures | Develop a hypothesis for an intermittent failure from differences between successful and failed runs. |

## 14.4 GitHub-specific troubleshooting

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-14.04.001` | Workflow not triggering | Diagnose a GitHub workflow that did not start using event, filter, and workflow-file evidence. |
| `LO-14.04.002` | Required status check not reported | Identify why a required status check is absent from a pull request. |
| `LO-14.04.003` | GitHub Actions token permissions | Determine whether a failed GitHub operation is caused by insufficient `GITHUB_TOKEN` permissions. |
| `LO-14.04.004` | Third-party action failures | Isolate a third-party action failure to its version, inputs, dependencies, or external service. |
| `LO-14.04.005` | Cache problems | Diagnose a cache miss or inappropriate cache hit from its key and restoration evidence. |
| `LO-14.04.006` | Self-hosted runner offline | Identify registration, connectivity, or service-state causes of an offline self-hosted runner. |
| `LO-14.04.007` | Workflow concurrency deadlocks | Trace a blocked workflow through concurrency groups and dependencies to locate a scheduling deadlock. |
| `LO-14.04.008` | Fork and pull request permission issues | Explain a fork-related workflow failure using the run's permission and secret-access context. |

## 14.5 Azure DevOps-specific troubleshooting

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-14.05.001` | Agent capabilities and demands | Diagnose a queued Azure Pipeline job whose demands do not match available agent capabilities. |
| `LO-14.05.002` | Service connection authorisation failures | Distinguish pipeline authorisation failure from cloud access failure for a service connection. |
| `LO-14.05.003` | Template evaluation errors | Locate a template evaluation failure using parameter types and expression timing. |
| `LO-14.05.004` | Branch policy failures | Identify which Azure Repos branch policy prevents a proposed change from completing. |
| `LO-14.05.005` | Pipeline resource access | Determine whether a pipeline resource failure comes from permissions, checks, or availability. |
| `LO-14.05.006` | Variable expansion problems | Trace an unexpected variable value through its scope and evaluation phase. |
| `LO-14.05.007` | Deployment approval failures | Identify why a deployment approval or check has not allowed execution to proceed. |
| `LO-14.05.008` | Job authorization scope problems | Diagnose repository access failure caused by a pipeline's job authorization scope. |

## 14.6 Operational resilience

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-14.06.001` | Platform outages | Choose a delivery response to a CI/CD platform outage using recovery and release requirements. |
| `LO-14.06.002` | Dependency service outages | Identify which delivery steps fail when an external dependency service is unavailable. |
| `LO-14.06.003` | Runner capacity shortages | Prioritise or reschedule work when runner capacity is insufficient. |
| `LO-14.06.004` | Recovery procedures | Define recovery steps with prerequisites and observable completion criteria. |
| `LO-14.06.005` | Incident response runbooks | Specify the decisions, owners, and evidence required in a pipeline incident runbook. |
| `LO-14.06.006` | Disaster recovery for build infrastructure | Identify build infrastructure configuration and state that must be recoverable after a disaster. |
| `LO-14.06.007` | Preserving release capability during outages | Design an authorised fallback release path that preserves essential validation during an outage. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [DORA delivery performance metrics](https://dora.dev/guides/dora-metrics/)
- [GitHub Actions documentation](https://docs.github.com/en/actions)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
