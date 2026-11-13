# 8. Software supply-chain security

Topic map: [section 8](../topic-map.md#8-software-supply-chain-security). See the [objective index](README.md) for ID and flashcard reference rules.

## 8.1 Supply-chain fundamentals

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-08.01.001` | Software supply-chain attack vectors | Locate supply-chain attack opportunities across source, dependencies, builds, and distribution. |
| `LO-08.01.002` | Source code integrity | Identify controls that protect source changes from unauthorised modification. |
| `LO-08.01.003` | Dependency integrity | Explain how dependency integrity can be checked before build execution. |
| `LO-08.01.004` | Build infrastructure integrity | Identify controls that prevent or reveal tampering with build infrastructure. |
| `LO-08.01.005` | Artifact integrity | Explain how artifact integrity can be checked between production and consumption. |
| `LO-08.01.006` | Provenance and chain of custody | Distinguish an artifact's provenance from the record of its transfers and custody. |
| `LO-08.01.007` | Trusted build systems | Identify the trust assumptions required to rely on a build system's outputs. |

## 8.2 Dependency security

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-08.02.001` | Direct versus transitive dependencies | Distinguish direct dependencies from dependencies introduced transitively. |
| `LO-08.02.002` | Dependency pinning | Explain the reproducibility and maintenance tradeoffs of dependency pinning. |
| `LO-08.02.003` | Lockfiles | Explain which dependency resolutions a lockfile records and what it does not guarantee. |
| `LO-08.02.004` | Malicious package detection | Identify package characteristics and behaviour that warrant malicious-package investigation. |
| `LO-08.02.005` | Dependency confusion | Explain how dependency confusion can cause an unintended package source to be selected. |
| `LO-08.02.006` | Typosquatting | Explain how a misleading package name can exploit a dependency selection mistake. |
| `LO-08.02.007` | Vulnerability identification | Interpret a vulnerability finding using affected versions, reachability, and available remediation. |
| `LO-08.02.008` | Automated dependency updates | Choose validation and review controls for an automated dependency update. |
| `LO-08.02.009` | Open-source licence compliance | Identify licence obligations that must be checked before distributing a dependency. |

## 8.3 Static and dynamic analysis

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-08.03.001` | Static Application Security Testing (SAST) | Explain the kinds of source-code weaknesses SAST can identify and its analysis limitations. |
| `LO-08.03.002` | Dynamic Application Security Testing (DAST) | Explain how DAST assesses a running application and which environment access it requires. |
| `LO-08.03.003` | Software Composition Analysis (SCA) | Explain how SCA identifies dependency-related risks. |
| `LO-08.03.004` | Infrastructure as Code scanning | Identify insecure infrastructure settings that an IaC scanner can detect before deployment. |
| `LO-08.03.005` | Container image scanning | Distinguish container image findings from risks introduced only at runtime. |
| `LO-08.03.006` | Secret scanning | Identify where secret scanning fits in source and artifact validation. |
| `LO-08.03.007` | Policy-as-Code security checks | Translate a security requirement into an automatically evaluable policy check. |
| `LO-08.03.008` | Managing false positives and exceptions | Distinguish a false positive from an accepted risk and specify the evidence needed for each. |

## 8.4 GitHub security tooling

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-08.04.001` | CodeQL and code scanning | Explain the relationship between CodeQL analysis and GitHub code scanning findings. |
| `LO-08.04.002` | Dependabot alerts and updates | Distinguish Dependabot vulnerability alerts from dependency update pull requests. |
| `LO-08.04.003` | Dependency review | Explain how dependency review evaluates dependency changes introduced by a pull request. |
| `LO-08.04.004` | Secret scanning and push protection | Choose secret scanning and push protection controls for detection and prevention requirements. |
| `LO-08.04.005` | Repository security advisories | Describe the purpose of a repository security advisory in coordinated vulnerability handling. |
| `LO-08.04.006` | Security campaigns | Explain how security campaigns organise remediation work across repositories. |
| `LO-08.04.007` | GitHub security policies and feature licensing | Identify the current plan and policy prerequisites for a requested GitHub security capability. |

## 8.5 Artifact security

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-08.05.001` | Artifact signing | Explain what validating an artifact signature establishes about its origin and integrity. |
| `LO-08.05.002` | Code signing and certificate protection | Identify controls needed to protect a code-signing key or certificate. |
| `LO-08.05.003` | Artifact attestations | Explain which claims an artifact attestation binds to a specific artifact. |
| `LO-08.05.004` | Build provenance | Identify provenance information needed to connect an artifact to its build inputs and execution. |
| `LO-08.05.005` | Software Bills of Materials (SBOM) | Explain how an SBOM supports component inventory without proving that every component is safe. |
| `LO-08.05.006` | SLSA framework | Relate a stated SLSA specification version's requirements to evidence about a build or source process. |
| `LO-08.05.007` | Sigstore and related technologies | Explain the roles of signing identity and verification evidence in a Sigstore-based workflow. |
| `LO-08.05.008` | Verifying artifacts before deployment | Define verification checks that must succeed before an artifact is deployed. |

## 8.6 Enterprise enforcement

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-08.06.001` | Required vulnerability checks | Choose vulnerability checks that must complete before a change or artifact can advance. |
| `LO-08.06.002` | Security gates | Place security gates at the points where an unacceptable artifact could otherwise be promoted. |
| `LO-08.06.003` | Critical vulnerability thresholds | Define a vulnerability threshold using severity and contextual risk. |
| `LO-08.06.004` | Exception and risk acceptance workflows | Specify ownership, expiry, and review requirements for a security exception. |
| `LO-08.06.005` | Evidence retention | Identify evidence that must be retained to justify a release's security decision. |
| `LO-08.06.006` | Secure release promotion | Explain how release promotion preserves the identity of the artifact that passed security checks. |
| `LO-08.06.007` | Software provenance verification | Evaluate whether provenance satisfies a stated policy about allowed sources and builders. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [GitHub security and code quality documentation](https://docs.github.com/en/code-security)
- [SLSA specification](https://slsa.dev/spec/)
