# 9. Testing and quality engineering

Topic map: [section 9](../topic-map.md#9-testing-and-quality-engineering). See the [objective index](README.md) for ID and flashcard reference rules.

## 9.1 Testing fundamentals

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-09.01.001` | Unit testing | Identify a behaviour suitable for a unit test and define its isolation boundary. |
| `LO-09.01.002` | Integration testing | Identify an interaction that requires an integration test. |
| `LO-09.01.003` | End-to-end testing | Explain which user journey an end-to-end test should verify. |
| `LO-09.01.004` | Smoke testing | Choose a small set of smoke tests that reveal whether a deployment is basically usable. |
| `LO-09.01.005` | Regression testing | Design a regression test that detects the recurrence of a specific defect. |
| `LO-09.01.006` | Acceptance testing | Translate an acceptance criterion into an observable test result. |
| `LO-09.01.007` | Contract testing | Explain how a contract test detects incompatible expectations between interacting services. |
| `LO-09.01.008` | Performance testing | Choose a performance test and workload model for a stated latency or throughput requirement. |

## 9.2 CI quality gates

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-09.02.001` | Required passing tests | Define which test suites must pass before a change can merge or be promoted. |
| `LO-09.02.002` | Linting and formatting enforcement | Explain how automated linting and formatting checks enforce repository conventions. |
| `LO-09.02.003` | Static code analysis | Identify code properties that static analysis can check without executing the application. |
| `LO-09.02.004` | Type checking | Explain how type checking catches invalid uses of values before runtime. |
| `LO-09.02.005` | Test coverage | Interpret coverage measurements without treating them as proof of test quality. |
| `LO-09.02.006` | Quality thresholds | Choose a quality threshold with a clear pass or fail decision. |
| `LO-09.02.007` | Test result publishing | Explain how publishing test results improves failure diagnosis and release evidence. |
| `LO-09.02.008` | Blocking versus advisory checks | Choose blocking or advisory status for a check based on its reliability and risk. |

## 9.3 Test architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-09.03.001` | Test pyramid | Explain how a test pyramid balances test scope, execution cost, and feedback speed. |
| `LO-09.03.002` | Test isolation | Identify shared state that prevents tests from running independently. |
| `LO-09.03.003` | Mocking and stubbing | Choose a mock or stub according to the interaction or response a test must control. |
| `LO-09.03.004` | Test fixtures | Design test fixtures that provide repeatable setup and cleanup. |
| `LO-09.03.005` | Test parallelisation | Identify ordering and resource conflicts that must be removed before parallelising tests. |
| `LO-09.03.006` | Test data management | Choose a test data strategy that supports repeatability and appropriate data protection. |
| `LO-09.03.007` | Ephemeral test environments | Explain when an ephemeral environment is suitable for integration testing. |
| `LO-09.03.008` | Test reliability and determinism | Identify nondeterministic inputs that make a test's result unreliable. |

## 9.4 Enterprise test governance

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-09.04.001` | Central quality standards | Define a central quality standard with observable compliance criteria. |
| `LO-09.04.002` | Risk-based testing | Prioritise tests based on the likelihood and impact of failure. |
| `LO-09.04.003` | Mandatory security checks | Choose security checks that must be included in a release's mandatory validation. |
| `LO-09.04.004` | Handling flaky tests | Distinguish a flaky test from an intermittent product defect using execution evidence. |
| `LO-09.04.005` | Preventing quality gate bypasses | Identify alternative paths that could bypass a required quality gate. |
| `LO-09.04.006` | Performance regression detection | Choose a baseline and comparison method for detecting performance regressions. |
| `LO-09.04.007` | Release readiness criteria | Define release-readiness criteria from test evidence and unresolved defects. |

## 9.5 Platform-specific implementation

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-09.05.001` | GitHub Actions test reporting | Identify how a GitHub Actions workflow exposes test results to reviewers. |
| `LO-09.05.002` | Azure Pipelines test publishing | Explain how Azure Pipelines test publishing associates results with a pipeline run. |
| `LO-09.05.003` | JUnit and other standard result formats | Identify the result-format compatibility needed between a test runner and a reporting task. |
| `LO-09.05.004` | Code coverage publishing | Explain how code coverage output is collected and made available to reviewers. |
| `LO-09.05.005` | Test matrices across operating systems | Choose an operating-system test matrix from supported application environments. |
| `LO-09.05.006` | Language-specific tooling for PowerShell, .NET, JavaScript, and Python | Match PowerShell, .NET, JavaScript, and Python test tooling to the corresponding project and output requirements. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [Azure Test Plans documentation](https://learn.microsoft.com/en-us/azure/devops/test/?view=azure-devops)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
- [DORA capabilities](https://dora.dev/capabilities/)
