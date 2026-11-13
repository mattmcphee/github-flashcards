# 5. Pipeline engineering and scripting

Topic map: [section 5](../topic-map.md#5-pipeline-engineering-and-scripting). See the [objective index](README.md) for ID and flashcard reference rules.

## 5.1 Designing maintainable pipelines

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-05.01.001` | Separation of concerns | Separate build, test, security, and deployment responsibilities in a pipeline design. |
| `LO-05.01.002` | Naming conventions | Choose names that make pipeline jobs, artifacts, and environments identifiable in logs. |
| `LO-05.01.003` | Small, composable jobs | Identify when a large job should be divided into independently meaningful jobs. |
| `LO-05.01.004` | Reusable steps and templates | Extract repeated execution logic into a reusable step or template with a clear contract. |
| `LO-05.01.005` | Parameter-driven workflows | Choose parameters that expose necessary pipeline choices without duplicating implementation. |
| `LO-05.01.006` | Explicit dependencies | Identify dependencies that must be declared to prevent accidental execution ordering. |
| `LO-05.01.007` | Avoiding unnecessary conditional complexity | Simplify conditional logic while preserving the pipeline's required execution paths. |
| `LO-05.01.008` | Documentation and discoverability | Specify the documentation a new maintainer needs to locate and operate a pipeline. |

## 5.2 Execution optimisation

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-05.02.001` | Parallelism and matrix builds | Identify independent work suitable for parallel execution or a matrix. |
| `LO-05.02.002` | Dependency caching | Choose a dependency-cache key and invalidation strategy that preserves correctness. |
| `LO-05.02.003` | Incremental builds | Explain the inputs that must be tracked for an incremental build to remain valid. |
| `LO-05.02.004` | Path-based execution | Identify when path-based execution can safely skip work and when indirect dependencies prevent it. |
| `LO-05.02.005` | Build artifact reuse | Choose when to reuse a previously validated build artifact. |
| `LO-05.02.006` | Reducing checkout and setup overhead | Identify unnecessary checkout and environment-setup work in a pipeline timeline. |
| `LO-05.02.007` | Optimising runner allocation | Match runner resources to job demands without unnecessary idle capacity. |
| `LO-05.02.008` | Avoiding unnecessary pipeline executions | Identify redundant triggers or jobs that can be removed without losing validation. |

## 5.3 Reliability

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-05.03.001` | Timeouts and cancellation handling | Specify timeout and cancellation behaviour for an operation that acquires external resources. |
| `LO-05.03.002` | Retry strategies and transient failures | Choose retry conditions and limits that distinguish transient from persistent failures. |
| `LO-05.03.003` | Idempotent scripts | Identify side effects that make a script unsafe to repeat. |
| `LO-05.03.004` | Resource cleanup | Identify resources that require cleanup after success, failure, or cancellation. |
| `LO-05.03.005` | Partial failure recovery | Choose a recovery point after a partially completed pipeline operation. |
| `LO-05.03.006` | Error propagation and exit codes | Trace how an error or nonzero exit code propagates to the pipeline result. |
| `LO-05.03.007` | Handling flaky external services | Choose a response to an unreliable external service that preserves validation integrity. |
| `LO-05.03.008` | Safe reruns | Determine whether rerunning a failed job would duplicate an external side effect. |

## 5.4 Pipeline testing

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-05.04.001` | YAML validation | Distinguish YAML syntax validation from validation against a pipeline platform's schema. |
| `LO-05.04.002` | Workflow linting | Identify workflow configuration errors that static linting can detect before execution. |
| `LO-05.04.003` | ShellCheck and PowerShell ScriptAnalyzer | Choose ShellCheck or PowerShell ScriptAnalyzer according to the script language. |
| `LO-05.04.004` | Testing reusable workflows and templates | Define tests for the supported inputs and outputs of a reusable workflow or template. |
| `LO-05.04.005` | Testing custom actions and tasks | Define tests that exercise a custom action's or task's externally visible behaviour. |
| `LO-05.04.006` | Mocking external dependencies | Choose external dependencies to mock without concealing the integration behaviour under test. |
| `LO-05.04.007` | Testing deployment logic without deploying | Select a dry-run, plan, or simulated execution approach for checking deployment logic. |
| `LO-05.04.008` | Safe experimentation and staging | Design an isolated staging experiment with observable success and failure criteria. |

## 5.5 PowerShell and scripting in pipelines

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-05.05.001` | PowerShell 5.1 versus PowerShell 7 | Identify compatibility checks needed when moving a pipeline script from Windows PowerShell 5.1 to PowerShell 7. |
| `LO-05.05.002` | Cross-platform scripting considerations | Identify platform-dependent paths, commands, and assumptions in a script. |
| `LO-05.05.003` | $ErrorActionPreference and native process exit codes | Explain how `$ErrorActionPreference` and native exit-code handling affect failure detection for a specified PowerShell version. |
| `LO-05.05.004` | Passing arguments and escaping | Construct argument boundaries that preserve literal values across shell and process invocation. |
| `LO-05.05.005` | Secure logging and error handling | Identify sensitive values that must be excluded from logs and error messages. |
| `LO-05.05.006` | Structured output | Choose a structured output format that downstream automation can reliably parse. |
| `LO-05.05.007` | Environment variables and pipeline outputs | Distinguish process environment variables from explicitly published pipeline outputs. |
| `LO-05.05.008` | Avoiding command injection | Replace executable string construction with an invocation pattern that treats untrusted input as data. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [GitHub Actions documentation](https://docs.github.com/en/actions)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
- [PowerShell preference variables](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_preference_variables?view=powershell-7.5)
