# 7. Runner and pipeline security

Topic map: [section 7](../topic-map.md#7-runner-and-pipeline-security). See the [objective index](README.md) for ID and flashcard reference rules.

## 7.1 Runner trust models

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-07.01.001` | Trusted versus untrusted workloads | Classify workloads by whether their code and contributors are trusted. |
| `LO-07.01.002` | Hosted versus self-hosted runners | Compare hosted and self-hosted execution using an explicit threat model. |
| `LO-07.01.003` | Persistent versus ephemeral runners | Explain how runner persistence changes the risk of one job affecting another. |
| `LO-07.01.004` | Runner isolation boundaries | Identify the process, host, network, and identity boundaries around a runner job. |
| `LO-07.01.005` | Container isolation and its limitations | Explain which host-level risks remain when a job runs inside a container. |
| `LO-07.01.006` | Virtual machine isolation | Compare virtual machine isolation with shared-host execution for a workload. |
| `LO-07.01.007` | Secure runner registration and decommissioning | Describe secure runner enrolment and removal, including invalidating associated access. |

## 7.2 Pipeline execution security

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-07.02.001` | Least-privilege workflow tokens | Derive the minimum workflow-token permissions needed for a specific job. |
| `LO-07.02.002` | Controlling untrusted code execution | Choose an execution boundary that prevents untrusted code from accessing privileged resources. |
| `LO-07.02.003` | Safe pull request validation | Design pull request validation that separates untrusted execution from privileged deployment. |
| `LO-07.02.004` | Preventing command and script injection | Identify command-injection risks caused by combining executable code with untrusted input. |
| `LO-07.02.005` | Secrets exposure through workflow contexts | Trace how a workflow context value could expose a secret to a job or log. |
| `LO-07.02.006` | Preventing unauthorized pipeline modifications | Identify controls that prevent an unauthorised contributor from changing executable pipeline definitions. |
| `LO-07.02.007` | Restricting privileged workflow triggers | Restrict privileged triggers to authorised callers and appropriately validated inputs. |

## 7.3 GitHub-specific attack surfaces

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-07.03.001` | pull_request_target misuse | Identify unsafe execution of pull request code in a privileged `pull_request_target` workflow. |
| `LO-07.03.002` | Workflow poisoning | Trace how a malicious workflow change can alter a later trusted execution. |
| `LO-07.03.003` | Mutable third-party action tags | Explain the substitution risk of using a mutable tag for a third-party action. |
| `LO-07.03.004` | Compromised action dependencies | Identify the impact of a compromised dependency inside an otherwise approved action. |
| `LO-07.03.005` | Unsafe workflow_run privilege transitions | Identify unsafe transfers of untrusted outputs into a privileged `workflow_run` workflow. |
| `LO-07.03.006` | Cache poisoning | Explain how accepting an attacker-controlled cache entry can influence later execution. |
| `LO-07.03.007` | Artifact poisoning | Explain how consuming an unverified artifact can introduce attacker-controlled code into a trusted job. |
| `LO-07.03.008` | GITHUB_TOKEN abuse | Identify operations an attacker could perform with an overprivileged `GITHUB_TOKEN`. |

## 7.4 Azure DevOps-specific attack surfaces

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-07.04.001` | Excessively privileged service connections | Identify the blast radius of an excessively privileged Azure service connection. |
| `LO-07.04.002` | Collection-scoped build identities | Explain how collection-scoped build identities can broaden cross-project access. |
| `LO-07.04.003` | Insecure agent pools | Identify how sharing an insecure agent pool can expose other pipelines. |
| `LO-07.04.004` | Unrestricted pipeline resource access | Identify risks from allowing pipelines unrestricted access to protected resources. |
| `LO-07.04.005` | Malicious YAML template changes | Explain how a malicious YAML template change can affect consuming pipelines. |
| `LO-07.04.006` | Variable group and secure file exposure | Identify unauthorised access paths to variable groups and secure files. |
| `LO-07.04.007` | Insecure job authorization scopes | Determine whether a job authorization scope grants more repository access than required. |
| `LO-07.04.008` | Bypassing checks through alternative deployment paths | Identify deployment routes that bypass an intended approval or resource check. |

## 7.5 Runner and network hardening

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-07.05.001` | Network egress restrictions | Choose outbound network restrictions that permit required dependencies while limiting exfiltration paths. |
| `LO-07.05.002` | Private network connectivity | Identify the routing and authentication requirements for private runner connectivity. |
| `LO-07.05.003` | Network segmentation | Separate runner networks according to workload trust and environment sensitivity. |
| `LO-07.05.004` | Endpoint protection on self-hosted agents | Identify endpoint protection requirements for a self-hosted agent. |
| `LO-07.05.005` | Patch management and image maintenance | Define an image and patch maintenance process that keeps runner workloads supportable. |
| `LO-07.05.006` | Filesystem cleanup | Identify files and workspaces that must be removed or isolated between jobs. |
| `LO-07.05.007` | Temporary credential lifecycle | Trace the creation, use, expiry, and removal of temporary workload credentials. |
| `LO-07.05.008` | Monitoring runner integrity | Choose integrity signals that could reveal unauthorised changes to a runner. |

## 7.6 Security incident response

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-07.06.001` | Detecting malicious workflow execution | Identify execution patterns and audit events that warrant investigation as malicious workflow activity. |
| `LO-07.06.002` | Revoking compromised tokens | Prioritise credential revocation based on exposure and deployment authority. |
| `LO-07.06.003` | Isolating compromised runners | Describe how to isolate a compromised runner while preserving useful evidence. |
| `LO-07.06.004` | Investigating malicious pipeline modifications | Trace a malicious pipeline modification to its authorisation path and affected runs. |
| `LO-07.06.005` | Identifying potentially compromised artifacts | Determine the set of artifacts potentially affected by a compromised execution period. |
| `LO-07.06.006` | Rebuilding trusted execution infrastructure | Identify which runner images, credentials, and configuration must be rebuilt from trusted sources. |
| `LO-07.06.007` | Restoring secure deployment operations | Define evidence-based criteria for resuming secure deployment after containment. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [GitHub Actions secure use reference](https://docs.github.com/en/actions/reference/security/secure-use)
- [Azure Pipelines security](https://learn.microsoft.com/en-us/azure/devops/pipelines/security/overview?view=azure-devops)
