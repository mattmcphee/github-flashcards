# CI/CD topic map

## 1. CI/CD fundamentals

### 1.1 Fundamental concepts

- Continuous Integration, Continuous Delivery, Continuous Deployment
- Differences between CI, CD, and release management
- Source-to-production software delivery lifecycle
- Pipeline as Code and declarative automation
- Build automation versus deployment automation
- Shift-left testing and security
- Trunk-based development versus GitFlow
- DevOps, DevSecOps, and platform engineering

### 1.2 Pipeline architecture

- Pipeline triggers, stages, jobs, steps, tasks, and actions
- Directed acyclic graphs (DAGs)
- Dependency graphs and execution ordering
- Parallel versus sequential execution
- Build pipelines versus deployment pipelines
- Pipeline orchestration and reusable components
- Multi-stage and multi-environment pipelines
- Event-driven versus scheduled pipelines

### 1.3 Core engineering principles

- Build once, deploy many
- Immutable build artifacts
- Deterministic and reproducible builds
- Pipeline idempotency
- Infrastructure and configuration immutability
- Separation of build and release responsibilities
- Fail-fast principles
- Rollback versus roll-forward

### 1.4 Enterprise architectural decisions

- Centralised versus decentralised CI/CD
- Monorepo versus multirepo
- Single pipeline versus multiple specialised pipelines
- Standardisation versus team autonomy
- Hosted versus self-hosted execution
- Trust boundaries between systems and environments
- Designing CI/CD for scalability and maintainability

## 2. Source control and repository governance

### 2.1 Git fundamentals

- Commits, trees, blobs, references, and HEAD
- Branches, tags, and commit ancestry
- Merge, rebase, cherry-pick, revert, and reset
- Fast-forward versus three-way merges
- Merge conflicts and conflict resolution
- Signed commits and tags
- Git hooks and their limitations

### 2.2 Enterprise branching strategies

- Trunk-based development
- GitFlow
- Feature branches
- Release and hotfix branches
- Short-lived versus long-lived branches
- Feature flags as an alternative to branching
- Branching strategies for high-frequency deployment

### 2.3 Pull request governance

- Required reviews and approval thresholds
- CODEOWNERS and ownership enforcement
- Required status checks
- Dismissing stale approvals
- Preventing self-approval where supported
- Merge queues and merge trains
- Squash, merge commit, and rebase strategies
- Review of changes to pipeline configuration

### 2.4 Repository security and policy

- GitHub rulesets and branch protection
- Azure Repos branch policies
- Tag protection and release immutability
- Repository visibility and permission boundaries
- Restricting force pushes and deletion
- Secret scanning and push protection
- Repository creation and lifecycle governance
- Managing external collaborators

## 3. GitHub Actions

### 3.1 Core GitHub Actions architecture

- Events and workflow triggers
- Workflows, jobs, steps, and actions
- GitHub-hosted versus self-hosted runners
- Runner labels and groups
- Workflow execution lifecycle
- Job isolation and execution contexts
- Workflow dependencies using needs

### 3.2 Workflow triggering

- push, pull_request, workflow_dispatch
- workflow_call, workflow_run, repository_dispatch
- Scheduled execution
- Branch, tag, and path filters
- Trigger recursion and workflow chaining
- Avoiding duplicate executions
- Security differences between pull_request and pull_request_target

### 3.3 Workflow logic and YAML

- Expressions and context objects
- Environment variables versus configuration variables
- Job-level versus step-level configuration
- Conditional execution using if
- Matrix strategies
- Concurrency groups
- Cancellation of redundant builds
- Timeouts, retries, and exit codes

### 3.4 Reusability

- Composite actions
- Reusable workflows
- Workflow templates
- Organisation-shared automation
- Cross-repository workflow consumption
- Versioning reusable components
- Choosing composite actions versus reusable workflows

### 3.5 GitHub Actions security

- GITHUB_TOKEN permissions
- Read-only versus write access
- Repository and environment secrets
- OIDC authentication
- Action dependency pinning
- Third-party action allowlisting
- Script-injection attacks
- Untrusted pull request execution
- Environment protection and deployment approvals

### 3.6 Enterprise GitHub Actions infrastructure

- GitHub-hosted runners and larger runners
- Self-hosted runner registration and lifecycle
- Ephemeral runners
- Actions Runner Controller (ARC)
- Runner scale sets
- Network isolation and private networking
- Runner groups and repository restrictions
- Enterprise workflow policies

### 3.7 Operational management

- Workflow debugging
- Run logs and step summaries
- Cache and artifact management
- GitHub Actions billing and usage
- Concurrency and capacity limits
- GitHub REST API and CLI automation
- Workflow metrics and auditing

## 4. Azure DevOps and Azure Pipelines

### 4.1 Azure DevOps architecture

- Azure DevOps organisations
- Projects and team boundaries
- Azure Repos
- Azure Pipelines
- Azure Artifacts
- Azure Boards
- Azure Test Plans
- Azure DevOps Services versus Azure DevOps Server

### 4.2 Azure Pipelines fundamentals

- YAML pipelines versus classic pipelines
- Pipeline triggers and scheduled execution
- Stages, jobs, tasks, and steps
- Agent jobs versus agentless jobs
- Multi-stage pipeline architecture
- Pipeline resources
- Pipeline completion triggers
- Job dependencies and conditions

### 4.3 Pipeline templates

- YAML template inclusion
- extends templates
- Parameters versus variables
- Template expressions and compile-time evaluation
- Runtime expressions and macro variables
- Nested templates
- Centrally governed pipeline structures
- Restricting unsafe tasks using template design

### 4.4 Agent architecture

- Microsoft-hosted agents
- Self-hosted Windows and Linux agents
- Agent pools and queues
- Agent capabilities and demands
- Agent authentication and permissions
- Agent maintenance and upgrades
- Container jobs
- Agent isolation and persistence

### 4.5 Service connections

- Azure Resource Manager service connections
- Workload identity federation
- Service principals versus managed identities
- Service connection permissions
- Pipeline authorisation
- Protected resources
- Resource-level approvals and checks
- Service connection auditing

### 4.6 Environments and approvals

- Deployment jobs
- Environment resources
- Manual approvals
- Branch control checks
- Required template checks
- Business-hours restrictions
- Exclusive locks
- REST API and Azure Monitor checks
- Deployment history and traceability

### 4.7 Enterprise administration

- Organisation and project security
- Entra ID integration
- Build service identities
- Job authorization scope
- Variable groups and secure files
- Azure Artifacts feeds
- Pipeline resource permissions
- REST APIs and Azure DevOps CLI
- Audit logging

## 5. Pipeline engineering and scripting

### 5.1 Designing maintainable pipelines

- Separation of concerns
- Naming conventions
- Small, composable jobs
- Reusable steps and templates
- Parameter-driven workflows
- Explicit dependencies
- Avoiding unnecessary conditional complexity
- Documentation and discoverability

### 5.2 Execution optimisation

- Parallelism and matrix builds
- Dependency caching
- Incremental builds
- Path-based execution
- Build artifact reuse
- Reducing checkout and setup overhead
- Optimising runner allocation
- Avoiding unnecessary pipeline executions

### 5.3 Reliability

- Timeouts and cancellation handling
- Retry strategies and transient failures
- Idempotent scripts
- Resource cleanup
- Partial failure recovery
- Error propagation and exit codes
- Handling flaky external services
- Safe reruns

### 5.4 Pipeline testing

- YAML validation
- Workflow linting
- ShellCheck and PowerShell ScriptAnalyzer
- Testing reusable workflows and templates
- Testing custom actions and tasks
- Mocking external dependencies
- Testing deployment logic without deploying
- Safe experimentation and staging

### 5.5 PowerShell and scripting in pipelines

- PowerShell 5.1 versus PowerShell 7
- Cross-platform scripting considerations
- $ErrorActionPreference and native process exit codes
- Passing arguments and escaping
- Secure logging and error handling
- Structured output
- Environment variables and pipeline outputs
- Avoiding command injection

## 6. Identity and secrets management

### 6.1 Enterprise identity architecture

- Human versus workload identities
- Microsoft Entra ID integration
- Service principals and managed identities
- GitHub Apps versus personal access tokens
- Azure DevOps build service identities
- Authentication versus authorisation
- Role-based access control and least privilege

### 6.2 Modern pipeline authentication

- OpenID Connect (OIDC)
- Workload identity federation
- Short-lived versus long-lived credentials
- OIDC tokens, claims, audiences, and subjects
- Trust relationships between CI/CD platforms and Entra ID
- Federated identity credentials
- Restricting identities by repository, workflow, or environment

### 6.3 Secrets management

- GitHub Actions repository, environment, and organisation secrets
- Azure Pipelines secret variables
- Azure Key Vault integration
- Secret rotation and revocation
- Protecting secrets from logs and artifacts
- Secret masking limitations
- Preventing credential exposure through pull requests
- Eliminating unnecessary persistent secrets

### 6.4 Identity governance

- Just-in-time privileged access
- Privileged Identity Management (PIM) for human administrators
- Separation of duties
- Production versus non-production identities
- Break-glass access
- Credential inventory and lifecycle management
- Auditability of identity usage

### 6.5 Threat modelling

- Compromised developer account
- Malicious pull request
- Compromised third-party action
- Stolen deployment credential
- Privilege escalation through workflow modification
- Cross-project lateral movement
- Production environment takeover

## 7. Runner and pipeline security

### 7.1 Runner trust models

- Trusted versus untrusted workloads
- Hosted versus self-hosted runners
- Persistent versus ephemeral runners
- Runner isolation boundaries
- Container isolation and its limitations
- Virtual machine isolation
- Secure runner registration and decommissioning

### 7.2 Pipeline execution security

- Least-privilege workflow tokens
- Controlling untrusted code execution
- Safe pull request validation
- Preventing command and script injection
- Secrets exposure through workflow contexts
- Preventing unauthorized pipeline modifications
- Restricting privileged workflow triggers

### 7.3 GitHub-specific attack surfaces

- pull_request_target misuse
- Workflow poisoning
- Mutable third-party action tags
- Compromised action dependencies
- Unsafe workflow_run privilege transitions
- Cache poisoning
- Artifact poisoning
- GITHUB_TOKEN abuse

### 7.4 Azure DevOps-specific attack surfaces

- Excessively privileged service connections
- Collection-scoped build identities
- Insecure agent pools
- Unrestricted pipeline resource access
- Malicious YAML template changes
- Variable group and secure file exposure
- Insecure job authorization scopes
- Bypassing checks through alternative deployment paths

### 7.5 Runner and network hardening

- Network egress restrictions
- Private network connectivity
- Network segmentation
- Endpoint protection on self-hosted agents
- Patch management and image maintenance
- Filesystem cleanup
- Temporary credential lifecycle
- Monitoring runner integrity

### 7.6 Security incident response

- Detecting malicious workflow execution
- Revoking compromised tokens
- Isolating compromised runners
- Investigating malicious pipeline modifications
- Identifying potentially compromised artifacts
- Rebuilding trusted execution infrastructure
- Restoring secure deployment operations

## 8. Software supply-chain security

### 8.1 Supply-chain fundamentals

- Software supply-chain attack vectors
- Source code integrity
- Dependency integrity
- Build infrastructure integrity
- Artifact integrity
- Provenance and chain of custody
- Trusted build systems

### 8.2 Dependency security

- Direct versus transitive dependencies
- Dependency pinning
- Lockfiles
- Malicious package detection
- Dependency confusion
- Typosquatting
- Vulnerability identification
- Automated dependency updates
- Open-source licence compliance

### 8.3 Static and dynamic analysis

- Static Application Security Testing (SAST)
- Dynamic Application Security Testing (DAST)
- Software Composition Analysis (SCA)
- Infrastructure as Code scanning
- Container image scanning
- Secret scanning
- Policy-as-Code security checks
- Managing false positives and exceptions

### 8.4 GitHub security tooling

- CodeQL and code scanning
- Dependabot alerts and updates
- Dependency review
- Secret scanning and push protection
- Repository security advisories
- Security campaigns
- GitHub security policies and feature licensing

### 8.5 Artifact security

- Artifact signing
- Code signing and certificate protection
- Artifact attestations
- Build provenance
- Software Bills of Materials (SBOM)
- SLSA framework
- Sigstore and related technologies
- Verifying artifacts before deployment

### 8.6 Enterprise enforcement

- Required vulnerability checks
- Security gates
- Critical vulnerability thresholds
- Exception and risk acceptance workflows
- Evidence retention
- Secure release promotion
- Software provenance verification

## 9. Testing and quality engineering

### 9.1 Testing fundamentals

- Unit testing
- Integration testing
- End-to-end testing
- Smoke testing
- Regression testing
- Acceptance testing
- Contract testing
- Performance testing

### 9.2 CI quality gates

- Required passing tests
- Linting and formatting enforcement
- Static code analysis
- Type checking
- Test coverage
- Quality thresholds
- Test result publishing
- Blocking versus advisory checks

### 9.3 Test architecture

- Test pyramid
- Test isolation
- Mocking and stubbing
- Test fixtures
- Test parallelisation
- Test data management
- Ephemeral test environments
- Test reliability and determinism

### 9.4 Enterprise test governance

- Central quality standards
- Risk-based testing
- Mandatory security checks
- Handling flaky tests
- Preventing quality gate bypasses
- Performance regression detection
- Release readiness criteria

### 9.5 Platform-specific implementation

- GitHub Actions test reporting
- Azure Pipelines test publishing
- JUnit and other standard result formats
- Code coverage publishing
- Test matrices across operating systems
- Language-specific tooling for PowerShell, .NET, JavaScript, and Python

## 10. Artifacts, dependencies and versioning

### 10.1 Build artifacts

- Definition and purpose of build artifacts
- Build output versus pipeline cache
- Immutable artifact principles
- Artifact naming and metadata
- Artifact retention
- Artifact promotion
- Artifact storage and access control

### 10.2 Package and artifact registries

- GitHub Packages
- GitHub Container Registry
- Azure Artifacts
- Azure Container Registry
- npm and NuGet registries
- Private versus public registries
- Registry permissions and authentication

### 10.3 Dependency management

- Dependency caching
- Package lockfiles
- Reproducible dependency restoration
- Private package feeds
- Upstream sources
- Package provenance
- Dependency vulnerability management

### 10.4 Versioning and release identification

- Semantic Versioning
- Git tags
- Release branches
- Build numbers
- Commit SHA identification
- Pre-release versions
- Release notes and changelogs
- Release immutability

### 10.5 Artifact lifecycle

- Build and validation
- Security scanning
- Signing and attestation
- Publication
- Promotion between environments
- Deployment
- Retention and disposal

## 11. Deployment strategies and release management

### 11.1 Continuous delivery architecture

- Continuous delivery versus deployment
- Deployment pipelines
- Environment progression
- Development, test, staging, and production
- Approval gates
- Change control
- Release orchestration

### 11.2 Deployment strategies

- In-place deployments
- Rolling deployments
- Blue-green deployments
- Canary deployments
- Feature flag deployments
- Ring-based deployments
- Progressive delivery

### 11.3 Production safeguards

- Manual and automated approvals
- Deployment windows
- Health checks
- Automated rollback
- Roll-forward strategies
- Deployment locks
- Separation of duties
- Emergency deployment procedures

### 11.4 Environment management

- Environment-specific configuration
- Configuration injection
- Secret references
- Infrastructure drift
- Environment parity
- Ephemeral environments
- Production deployment protection

### 11.5 Database and state management

- Database schema migrations
- Backward-compatible changes
- Expand-and-contract migrations
- Stateful application deployments
- Data rollback limitations
- Coordinating application and database releases

### 11.6 Release engineering

- Release candidates
- Artifact promotion
- Release notes
- Version traceability
- Deployment provenance
- Change records
- Incident-driven rollback decisions

## 12. Infrastructure as Code and GitOps

### 12.1 IaC fundamentals

- Declarative versus imperative infrastructure
- Desired-state configuration
- Infrastructure drift
- Immutable infrastructure
- Infrastructure testing
- State management
- Change approval and auditing

### 12.2 IaC technologies

- Terraform
- OpenTofu
- Azure Bicep
- ARM templates
- PowerShell automation
- Ansible
- Kubernetes manifests
- Helm

### 12.3 IaC pipelines

- Validate, plan, and apply
- Pull request plan review
- Securing state files
- State locking
- Secrets management
- Production approval controls
- Automated drift detection
- Destroy operations and safeguards

### 12.4 GitOps

- Git as a desired-state source
- Pull-based versus push-based deployment
- Reconciliation loops
- Argo CD and Flux
- GitOps repository models
- Drift correction
- GitOps security boundaries

### 12.5 Enterprise Azure integration

- Azure landing zones
- Subscription vending
- Management groups and subscriptions
- Azure Policy
- RBAC as Code
- Entra ID workload identities
- Infrastructure deployment permissions
- Policy compliance checks

## 13. Enterprise governance and compliance

### 13.1 Enterprise governance architecture

- Enterprise versus organisation versus repository controls
- Centralised governance models
- Delegated administration
- Policy inheritance
- Standardised repository baselines
- Repository ownership and accountability
- Governance exceptions and their lifecycle

### 13.2 Enterprise GitHub governance

- Enterprise and organisation policies
- Repository rulesets
- GitHub Actions execution policies
- Required workflow controls
- Restricting third-party actions
- Approved workflow templates
- Repository custom properties
- Enterprise audit logging
- GitHub Apps governance

### 13.3 Azure DevOps governance

- Organisation and project security
- Project-scoped identities
- Branch policies
- Centrally managed extends templates
- Required template checks
- Protected service connections
- Agent pool authorisation
- Pipeline permissions
- Disabling unused classic pipeline capabilities

### 13.4 Compliance and auditing

- Audit log retention
- Deployment traceability
- Evidence collection
- Change management
- Security control enforcement
- Least privilege and separation of duties
- Policy exception reviews
- Regulatory compliance considerations

### 13.5 Enterprise policy design

- Policy-as-Code
- Centrally enforced security baselines
- Version-controlled policies
- Gradual rollout of stricter requirements
- Exception management
- Monitoring policy drift
- Measuring compliance adoption

### 13.6 Organisation-wide automation

- GitHub REST and GraphQL APIs
- Azure DevOps REST APIs
- GitHub CLI and Azure DevOps CLI
- Automated repository provisioning
- Automated branch policy configuration
- Repository security audits
- Organisation-wide compliance reporting
- Automated remediation and its safeguards

## 14. Monitoring, reliability and troubleshooting

### 14.1 CI/CD observability

- Pipeline execution metrics
- Build success and failure rates
- Execution duration
- Queue wait times
- Runner utilisation
- Deployment success rates
- Failure categorisation
- Logging and tracing

### 14.2 DORA and delivery performance

- Deployment frequency
- Change lead time
- Change failure rate
- Failed deployment recovery time
- Reliability and operational stability
- Using metrics without incentivising poor behaviour

### 14.3 Pipeline troubleshooting

- YAML parsing errors
- Trigger evaluation failures
- Permission-denied errors
- Missing variables and secrets
- Authentication and OIDC failures
- Dependency restoration failures
- Agent compatibility issues
- Resource exhaustion
- Network connectivity problems
- Intermittent failures

### 14.4 GitHub-specific troubleshooting

- Workflow not triggering
- Required status check not reported
- GitHub Actions token permissions
- Third-party action failures
- Cache problems
- Self-hosted runner offline
- Workflow concurrency deadlocks
- Fork and pull request permission issues

### 14.5 Azure DevOps-specific troubleshooting

- Agent capabilities and demands
- Service connection authorisation failures
- Template evaluation errors
- Branch policy failures
- Pipeline resource access
- Variable expansion problems
- Deployment approval failures
- Job authorization scope problems

### 14.6 Operational resilience

- Platform outages
- Dependency service outages
- Runner capacity shortages
- Recovery procedures
- Incident response runbooks
- Disaster recovery for build infrastructure
- Preserving release capability during outages

## 15. Developer experience and platform engineering

### 15.1 Internal developer platforms

- Platform engineering fundamentals
- Golden paths
- Standardised service templates
- Self-service repository provisioning
- Self-service CI/CD onboarding
- Developer portals
- Infrastructure abstraction

### 15.2 Shared automation

- Central workflow repositories
- Reusable workflow libraries
- Shared Azure Pipeline templates
- Versioning and compatibility contracts
- Ownership and support responsibilities
- Breaking change management
- Automated template updates

### 15.3 Developer productivity

- Fast pull request feedback
- Local validation before pushing
- Pre-commit checks
- Development containers
- Standardised tooling
- IDE integration
- Automated code quality fixes
- Reducing pipeline maintenance overhead

### 15.4 AI-assisted development

- GitHub Copilot
- AI code review
- AI-assisted pull request preparation
- AI-generated workflow YAML
- Agent-driven repository maintenance
- Automated dependency upgrades
- AI-assisted failure diagnosis
- Human approval and validation boundaries

### 15.5 Agentic CI/CD

- AI agents creating branches and pull requests
- Automated remediation workflows
- AI-generated tests
- Agent-triggered workflow execution
- Identity and permissions for AI agents
- Sandboxing agent-executed code
- Preventing prompt injection through repository content
- Restricting autonomous modification of production pipelines
- Auditability and rollback of agent changes

## 16. Advanced enterprise scenarios and architecture

### 16.1 Enterprise architecture patterns

- Multi-organisation GitHub environments
- Multi-project Azure DevOps environments
- Shared CI/CD platform teams
- Hybrid GitHub and Azure DevOps architectures
- Cross-organisation automation
- Federated identity across tenants
- Multi-cloud deployment architectures

### 16.2 Highly regulated environments

- Segregation of duties
- Privileged deployment workflows
- Restricted production access
- Formal release approval processes
- Audit evidence preservation
- Change control integration
- Secure software provenance
- Compliance-as-Code

### 16.3 Large-scale automation

- Thousands of repositories and pipelines
- API rate limiting
- Pipeline concurrency management
- Dynamic runner scaling
- Central policy distribution
- Fleet-wide workflow updates
- Security posture reporting
- Cost optimisation

### 16.4 Platform migration

- Azure Pipelines to GitHub Actions
- GitHub Actions to Azure Pipelines
- Classic to YAML pipelines
- Migrating secrets to federated identities
- Migrating shared templates
- Replacing persistent build agents
- Preserving auditability through migration
- Rollback and coexistence strategies

### 16.5 Architectural decision-making

- When to choose GitHub Actions
- When to choose Azure Pipelines
- Running GitHub repositories with Azure Pipelines
- Platform licensing and cost considerations
- Operational ownership
- Security feature availability
- Long-term maintainability
- Avoiding unnecessary platform complexity
