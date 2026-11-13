# 6. Identity and secrets management

Topic map: [section 6](../topic-map.md#6-identity-and-secrets-management). See the [objective index](README.md) for ID and flashcard reference rules.

## 6.1 Enterprise identity architecture

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-06.01.001` | Human versus workload identities | Distinguish human and workload identities by ownership, interaction, and lifecycle. |
| `LO-06.01.002` | Microsoft Entra ID integration | Explain the role of Entra ID in authenticating identities used by delivery systems. |
| `LO-06.01.003` | Service principals and managed identities | Choose a service principal or managed identity for a specified execution environment. |
| `LO-06.01.004` | GitHub Apps versus personal access tokens | Compare GitHub Apps and personal access tokens for automation ownership and permission scope. |
| `LO-06.01.005` | Azure DevOps build service identities | Explain how Azure DevOps build service identities authorise pipeline resource access. |
| `LO-06.01.006` | Authentication versus authorisation | Distinguish proving an identity from granting that identity permission to perform an operation. |
| `LO-06.01.007` | Role-based access control and least privilege | Derive a least-privilege role assignment from the operations a workload must perform. |

## 6.2 Modern pipeline authentication

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-06.02.001` | OpenID Connect (OIDC) | Explain the role of OpenID Connect in conveying a workload's authenticated identity. |
| `LO-06.02.002` | Workload identity federation | Trace how workload identity federation replaces direct management of a persistent workload secret. |
| `LO-06.02.003` | Short-lived versus long-lived credentials | Compare short-lived and long-lived credentials by exposure window and renewal requirements. |
| `LO-06.02.004` | OIDC tokens, claims, audiences, and subjects | Explain how issuer, audience, subject, and other claims contribute to token validation. |
| `LO-06.02.005` | Trust relationships between CI/CD platforms and Entra ID | Identify the trust configuration required between a CI/CD platform and Entra ID. |
| `LO-06.02.006` | Federated identity credentials | Explain how a federated identity credential defines accepted external identity claims. |
| `LO-06.02.007` | Restricting identities by repository, workflow, or environment | Choose claim restrictions that limit access to an intended repository, workflow, or environment. |

## 6.3 Secrets management

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-06.03.001` | GitHub Actions repository, environment, and organisation secrets | Choose GitHub repository, environment, or organisation secret scope for an access requirement. |
| `LO-06.03.002` | Azure Pipelines secret variables | Explain how Azure Pipelines secret variables should be passed to a consuming task without disclosure. |
| `LO-06.03.003` | Azure Key Vault integration | Describe a pipeline's authenticated retrieval of secrets from Azure Key Vault. |
| `LO-06.03.004` | Secret rotation and revocation | Distinguish credential rotation from revocation during routine maintenance or incident response. |
| `LO-06.03.005` | Protecting secrets from logs and artifacts | Identify pipeline paths through which a secret could enter logs or stored artifacts. |
| `LO-06.03.006` | Secret masking limitations | Explain why masking known secret values does not guarantee prevention of all secret disclosure. |
| `LO-06.03.007` | Preventing credential exposure through pull requests | Identify pull request execution paths that must not receive privileged credentials. |
| `LO-06.03.008` | Eliminating unnecessary persistent secrets | Identify a persistent secret that can be replaced by federation or another suitable workload identity mechanism. |

## 6.4 Identity governance

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-06.04.001` | Just-in-time privileged access | Explain how time-limited privileged access reduces standing administrative authority. |
| `LO-06.04.002` | Privileged Identity Management (PIM) for human administrators | Describe the role of PIM activation and approval in human administrator access. |
| `LO-06.04.003` | Separation of duties | Identify incompatible responsibilities that should be assigned to different identities. |
| `LO-06.04.004` | Production versus non-production identities | Explain why production and non-production workloads may require separate identities. |
| `LO-06.04.005` | Break-glass access | Define access, monitoring, and review requirements for a break-glass identity. |
| `LO-06.04.006` | Credential inventory and lifecycle management | Specify the owner, purpose, expiry, and retirement information needed in a credential inventory. |
| `LO-06.04.007` | Auditability of identity usage | Identify logs and identifiers needed to attribute a privileged workload operation. |

## 6.5 Threat modelling

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-06.05.001` | Compromised developer account | Trace the delivery-system access an attacker could gain through a compromised developer account. |
| `LO-06.05.002` | Malicious pull request | Identify the trust boundary crossed when malicious pull request content executes. |
| `LO-06.05.003` | Compromised third-party action | Trace which credentials and artifacts a compromised third-party action could affect. |
| `LO-06.05.004` | Stolen deployment credential | Identify resources exposed by a stolen deployment credential and the immediate containment boundary. |
| `LO-06.05.005` | Privilege escalation through workflow modification | Explain how modifying a workflow can increase an attacker's effective privileges. |
| `LO-06.05.006` | Cross-project lateral movement | Identify permissions or shared resources that enable lateral movement between projects. |
| `LO-06.05.007` | Production environment takeover | Construct an attack path to production and identify controls that interrupt it. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [Microsoft Entra workload identities](https://learn.microsoft.com/en-us/entra/workload-id/workload-identities-overview)
- [GitHub Actions secure use reference](https://docs.github.com/en/actions/reference/security/secure-use)
- [Azure Pipelines security](https://learn.microsoft.com/en-us/azure/devops/pipelines/security/overview?view=azure-devops)
