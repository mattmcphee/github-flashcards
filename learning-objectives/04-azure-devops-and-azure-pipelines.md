# 4. Azure DevOps and Azure Pipelines

Topic map: [section 4](../topic-map.md#4-azure-devops-and-azure-pipelines). See the [objective index](README.md) for ID and flashcard reference rules.

## 4.1 Azure DevOps architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.01.001` | Azure DevOps organisations | Explain the role of an Azure DevOps organisation as an administrative boundary. |
| `LO-04.01.002` | Projects and team boundaries | Explain how projects and teams organise work and scope access within Azure DevOps. |
| `LO-04.01.003` | Azure Repos | Identify the source-control responsibilities provided by Azure Repos. |
| `LO-04.01.004` | Azure Pipelines | Identify the build and deployment responsibilities provided by Azure Pipelines. |
| `LO-04.01.005` | Azure Artifacts | Identify the package-management responsibilities provided by Azure Artifacts. |
| `LO-04.01.006` | Azure Boards | Identify the work-tracking responsibilities provided by Azure Boards. |
| `LO-04.01.007` | Azure Test Plans | Identify the test-management responsibilities provided by Azure Test Plans. |
| `LO-04.01.008` | Azure DevOps Services versus Azure DevOps Server | Compare Azure DevOps Services and Server by hosting responsibility, update model, and feature availability. |

## 4.2 Azure Pipelines fundamentals

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.02.001` | YAML pipelines versus classic pipelines | Compare YAML and classic pipelines by definition storage, reviewability, and administration. |
| `LO-04.02.002` | Pipeline triggers and scheduled execution | Determine which Azure Pipeline trigger or schedule matches a delivery requirement. |
| `LO-04.02.003` | Stages, jobs, tasks, and steps | Relate stages, jobs, tasks, and steps in an Azure Pipeline definition. |
| `LO-04.02.004` | Agent jobs versus agentless jobs | Choose an agent or agentless job based on supported execution requirements. |
| `LO-04.02.005` | Multi-stage pipeline architecture | Divide a delivery process into stages with explicit validation and deployment boundaries. |
| `LO-04.02.006` | Pipeline resources | Explain how pipeline resources declare external inputs or dependencies. |
| `LO-04.02.007` | Pipeline completion triggers | Determine when a pipeline-completion trigger should start a downstream pipeline. |
| `LO-04.02.008` | Job dependencies and conditions | Evaluate job dependencies and conditions to predict execution after success, failure, or skipping. |

## 4.3 Pipeline templates

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.03.001` | YAML template inclusion | Explain how including a YAML template contributes reusable pipeline structure. |
| `LO-04.03.002` | extends templates | Explain how an `extends` template establishes the outer structure of a pipeline. |
| `LO-04.03.003` | Parameters versus variables | Choose parameters or variables according to evaluation timing, type, and intended use. |
| `LO-04.03.004` | Template expressions and compile-time evaluation | Predict the structure produced by a template expression at compile time. |
| `LO-04.03.005` | Runtime expressions and macro variables | Distinguish runtime expressions from macro variable expansion. |
| `LO-04.03.006` | Nested templates | Trace values and structure through nested templates. |
| `LO-04.03.007` | Centrally governed pipeline structures | Identify which pipeline behaviours a central template should govern. |
| `LO-04.03.008` | Restricting unsafe tasks using template design | Explain how template design can restrict tasks and where additional enforcement is required. |

## 4.4 Agent architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.04.001` | Microsoft-hosted agents | Explain the provisioning and maintenance responsibilities associated with Microsoft-hosted agents. |
| `LO-04.04.002` | Self-hosted Windows and Linux agents | Compare self-hosted Windows and Linux agents for workload compatibility and maintenance. |
| `LO-04.04.003` | Agent pools and queues | Distinguish agent pools from project-level agent queues. |
| `LO-04.04.004` | Agent capabilities and demands | Match a job's demands to available agent capabilities. |
| `LO-04.04.005` | Agent authentication and permissions | Identify the identities and permissions involved in agent registration and job execution. |
| `LO-04.04.006` | Agent maintenance and upgrades | Plan agent upgrades without losing required workload compatibility. |
| `LO-04.04.007` | Container jobs | Identify the execution requirements and isolation limitations of container jobs. |
| `LO-04.04.008` | Agent isolation and persistence | Explain how persistent agent state can affect later jobs. |

## 4.5 Service connections

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.05.001` | Azure Resource Manager service connections | Explain the deployment access represented by an Azure Resource Manager service connection. |
| `LO-04.05.002` | Workload identity federation | Trace workload identity federation for an Azure Pipeline service connection. |
| `LO-04.05.003` | Service principals versus managed identities | Compare service principals and managed identities for a stated Azure workload. |
| `LO-04.05.004` | Service connection permissions | Determine who may administer or use a service connection from its permissions. |
| `LO-04.05.005` | Pipeline authorisation | Explain how pipeline authorisation controls use of a service connection. |
| `LO-04.05.006` | Protected resources | Identify which pipeline resources require protection against untrusted consumers. |
| `LO-04.05.007` | Resource-level approvals and checks | Choose resource-level approvals and checks for a deployment trust boundary. |
| `LO-04.05.008` | Service connection auditing | Identify audit evidence needed to trace service connection changes and use. |

## 4.6 Environments and approvals

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.06.001` | Deployment jobs | Explain how a deployment job associates execution with an environment. |
| `LO-04.06.002` | Environment resources | Describe the role of environment resources in identifying deployment targets. |
| `LO-04.06.003` | Manual approvals | Identify the approver and decision point for a manual deployment approval. |
| `LO-04.06.004` | Branch control checks | Explain how branch control checks constrain the source of a deployment. |
| `LO-04.06.005` | Required template checks | Explain how a required template check governs pipelines consuming a protected resource. |
| `LO-04.06.006` | Business-hours restrictions | Determine how business-hours restrictions affect when deployment may proceed. |
| `LO-04.06.007` | Exclusive locks | Explain how an exclusive lock controls competing deployments. |
| `LO-04.06.008` | REST API and Azure Monitor checks | Choose a REST API or Azure Monitor check for a stated external validation requirement. |
| `LO-04.06.009` | Deployment history and traceability | Trace a deployment to its environment, run, and source revision. |

## 4.7 Enterprise administration

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-04.07.001` | Organisation and project security | Distinguish organisation-level and project-level Azure DevOps security responsibilities. |
| `LO-04.07.002` | Entra ID integration | Explain how Entra ID integration relates user identity to Azure DevOps access. |
| `LO-04.07.003` | Build service identities | Identify the build service identity used by a pipeline and its required permissions. |
| `LO-04.07.004` | Job authorization scope | Explain how job authorization scope affects the resources a pipeline can access. |
| `LO-04.07.005` | Variable groups and secure files | Choose variable groups or secure files for a stated pipeline configuration need. |
| `LO-04.07.006` | Azure Artifacts feeds | Define appropriate producer and consumer access to an Azure Artifacts feed. |
| `LO-04.07.007` | Pipeline resource permissions | Identify permissions required for a pipeline to consume a protected resource. |
| `LO-04.07.008` | REST APIs and Azure DevOps CLI | Choose REST API or Azure DevOps CLI operations for an administrative automation task. |
| `LO-04.07.009` | Audit logging | Select audit events needed to investigate administrative and permission changes. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
- [Azure Pipelines security](https://learn.microsoft.com/en-us/azure/devops/pipelines/security/overview?view=azure-devops)
