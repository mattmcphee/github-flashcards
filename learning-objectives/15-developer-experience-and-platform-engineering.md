# 15. Developer experience and platform engineering

Topic map: [section 15](../topic-map.md#15-developer-experience-and-platform-engineering). See the [objective index](README.md) for ID and flashcard reference rules.

## 15.1 Internal developer platforms

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-15.01.001` | Platform engineering fundamentals | Explain how platform engineering treats internal delivery capabilities as a product for development teams. |
| `LO-15.01.002` | Golden paths | Describe a golden path and the supported choices it offers a service team. |
| `LO-15.01.003` | Standardised service templates | Identify the service configuration and delivery defaults a standard template should provide. |
| `LO-15.01.004` | Self-service repository provisioning | Define the inputs and controls for self-service repository creation. |
| `LO-15.01.005` | Self-service CI/CD onboarding | Describe a self-service onboarding flow that connects a service to supported CI/CD. |
| `LO-15.01.006` | Developer portals | Identify information and actions a developer portal should make discoverable. |
| `LO-15.01.007` | Infrastructure abstraction | Choose an infrastructure abstraction that reduces user effort while exposing necessary operational decisions. |

## 15.2 Shared automation

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-15.02.001` | Central workflow repositories | Define ownership and consumption boundaries for a central workflow repository. |
| `LO-15.02.002` | Reusable workflow libraries | Design a reusable workflow library around clear, documented consumer contracts. |
| `LO-15.02.003` | Shared Azure Pipeline templates | Identify Azure Pipeline steps or structures suitable for a shared template library. |
| `LO-15.02.004` | Versioning and compatibility contracts | Define versioning and compatibility promises for shared automation. |
| `LO-15.02.005` | Ownership and support responsibilities | Assign support, maintenance, and incident responsibilities for shared pipeline components. |
| `LO-15.02.006` | Breaking change management | Plan the communication and migration steps for a breaking automation change. |
| `LO-15.02.007` | Automated template updates | Choose validation and rollout controls for automated updates to template consumers. |

## 15.3 Developer productivity

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-15.03.001` | Fast pull request feedback | Identify changes that shorten the time to actionable pull request feedback. |
| `LO-15.03.002` | Local validation before pushing | Choose validations that developers can run locally before pushing a change. |
| `LO-15.03.003` | Pre-commit checks | Select pre-commit checks that provide useful feedback at acceptable local cost. |
| `LO-15.03.004` | Development containers | Explain how a development container improves reproducibility of the editing and validation environment. |
| `LO-15.03.005` | Standardised tooling | Choose standard tools and versions that reduce avoidable differences between developer environments. |
| `LO-15.03.006` | IDE integration | Identify IDE integrations that expose relevant checks and diagnostics during editing. |
| `LO-15.03.007` | Automated code quality fixes | Distinguish formatting fixes suitable for automation from changes requiring semantic review. |
| `LO-15.03.008` | Reducing pipeline maintenance overhead | Identify repeated pipeline maintenance tasks that can be simplified or centralised. |

## 15.4 AI-assisted development

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-15.04.001` | GitHub Copilot | Identify an appropriate GitHub Copilot assistance task and the review needed for its output. |
| `LO-15.04.002` | AI code review | Evaluate an AI code-review finding against the actual code and supporting evidence. |
| `LO-15.04.003` | AI-assisted pull request preparation | Identify the source changes and validation evidence needed to verify an AI-prepared pull request. |
| `LO-15.04.004` | AI-generated workflow YAML | Review AI-generated workflow YAML for correctness, permissions, and untrusted-input handling. |
| `LO-15.04.005` | Agent-driven repository maintenance | Define a bounded repository-maintenance task that an agent can execute with verifiable results. |
| `LO-15.04.006` | Automated dependency upgrades | Specify tests and review criteria for an automatically proposed dependency upgrade. |
| `LO-15.04.007` | AI-assisted failure diagnosis | Evaluate an AI failure diagnosis against logs, configuration, and reproducible observations. |
| `LO-15.04.008` | Human approval and validation boundaries | Choose which AI-assisted changes require human approval based on impact and authority. |

## 15.5 Agentic CI/CD

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-15.05.001` | AI agents creating branches and pull requests | Define branch and pull request permissions for an agent proposing repository changes. |
| `LO-15.05.002` | Automated remediation workflows | Design a bounded remediation workflow with explicit triggers and success criteria. |
| `LO-15.05.003` | AI-generated tests | Evaluate whether AI-generated tests check intended behaviour rather than reproducing implementation assumptions. |
| `LO-15.05.004` | Agent-triggered workflow execution | Identify the authorisation required for an agent to trigger a workflow. |
| `LO-15.05.005` | Identity and permissions for AI agents | Derive a least-privilege identity and credential lifecycle for an automation agent. |
| `LO-15.05.006` | Sandboxing agent-executed code | Define filesystem, network, and execution limits for a sandbox running agent-generated code. |
| `LO-15.05.007` | Preventing prompt injection through repository content | Identify repository content that attempts to redirect an agent beyond its authorised task. |
| `LO-15.05.008` | Restricting autonomous modification of production pipelines | Place review and permission boundaries around agent changes to production pipelines. |
| `LO-15.05.009` | Auditability and rollback of agent changes | Trace an agent's changes and executions to an identity and define how to reverse their effects. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [DORA capabilities](https://dora.dev/capabilities/)
- [Responsible use of GitHub Copilot](https://docs.github.com/en/copilot/responsible-use)
- [GitHub Actions documentation](https://docs.github.com/en/actions)
