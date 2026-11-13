# 10. Artifacts, dependencies and versioning

Topic map: [section 10](../topic-map.md#10-artifacts-dependencies-and-versioning). See the [objective index](README.md) for ID and flashcard reference rules.

## 10.1 Build artifacts

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-10.01.001` | Definition and purpose of build artifacts | Identify which build outputs should become distributable artifacts. |
| `LO-10.01.002` | Build output versus pipeline cache | Distinguish a release artifact from a disposable pipeline cache. |
| `LO-10.01.003` | Immutable artifact principles | Explain how immutable artifacts preserve the identity of tested build outputs. |
| `LO-10.01.004` | Artifact naming and metadata | Choose artifact names and metadata that identify source revision and build context. |
| `LO-10.01.005` | Artifact retention | Define artifact retention using release support and recovery requirements. |
| `LO-10.01.006` | Artifact promotion | Explain how artifact promotion changes release eligibility without rebuilding the artifact. |
| `LO-10.01.007` | Artifact storage and access control | Choose artifact storage permissions that separate publishing from consumption. |

## 10.2 Package and artifact registries

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-10.02.001` | GitHub Packages | Identify when GitHub Packages is an appropriate registry for a supported package format. |
| `LO-10.02.002` | GitHub Container Registry | Explain the role of GitHub Container Registry in publishing and consuming container images. |
| `LO-10.02.003` | Azure Artifacts | Choose an Azure Artifacts feed structure for a team's package distribution needs. |
| `LO-10.02.004` | Azure Container Registry | Explain the role of Azure Container Registry in storing and distributing container images. |
| `LO-10.02.005` | npm and NuGet registries | Distinguish npm and NuGet package publication and consumption requirements. |
| `LO-10.02.006` | Private versus public registries | Choose private or public registry visibility for a distribution requirement. |
| `LO-10.02.007` | Registry permissions and authentication | Define the authentication and permissions required by registry publishers and consumers. |

## 10.3 Dependency management

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-10.03.001` | Dependency caching | Choose a dependency-cache strategy that tolerates cache misses and avoids stale restoration. |
| `LO-10.03.002` | Package lockfiles | Explain how a package lockfile constrains dependency resolution. |
| `LO-10.03.003` | Reproducible dependency restoration | Identify configuration and inputs needed to reproduce dependency restoration. |
| `LO-10.03.004` | Private package feeds | Identify the authentication and source configuration needed to restore from a private feed. |
| `LO-10.03.005` | Upstream sources | Explain how upstream package sources affect resolution and availability. |
| `LO-10.03.006` | Package provenance | Identify provenance evidence that helps assess a package's origin. |
| `LO-10.03.007` | Dependency vulnerability management | Prioritise dependency vulnerability remediation using exposure, affected versions, and available fixes. |

## 10.4 Versioning and release identification

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-10.04.001` | Semantic Versioning | Choose a semantic version increment from the compatibility impact of a change. |
| `LO-10.04.002` | Git tags | Explain how a Git tag identifies a source revision for a release. |
| `LO-10.04.003` | Release branches | Explain how release branches support changes to a maintained release line. |
| `LO-10.04.004` | Build numbers | Distinguish a build number from a product's public version. |
| `LO-10.04.005` | Commit SHA identification | Use a commit SHA to identify the exact source revision associated with an artifact. |
| `LO-10.04.006` | Pre-release versions | Explain how pre-release identifiers distinguish candidate releases from stable releases. |
| `LO-10.04.007` | Release notes and changelogs | Select changes and compatibility information that belong in release notes or a changelog. |
| `LO-10.04.008` | Release immutability | Identify changes to published release content that would violate release immutability. |

## 10.5 Artifact lifecycle

| ID | Topic | Learning objective |
| --- | --- | --- |
| `LO-10.05.001` | Build and validation | Define evidence required for a build output to pass validation. |
| `LO-10.05.002` | Security scanning | Identify the security scans required before an artifact advances in its lifecycle. |
| `LO-10.05.003` | Signing and attestation | Identify the signing and attestation evidence attached to an approved artifact. |
| `LO-10.05.004` | Publication | Specify the destination and access requirements for publishing an artifact. |
| `LO-10.05.005` | Promotion between environments | Determine whether an artifact has met the requirements for promotion to the next environment. |
| `LO-10.05.006` | Deployment | Trace a deployment to the exact artifact version consumed. |
| `LO-10.05.007` | Retention and disposal | Define when an artifact can be retained, archived, or disposed of. |

## Reference starting points

Use these primary sources when researching card answers; see the index for version and source-recording requirements.

- [Semantic Versioning specification](https://semver.org/)
- [Azure Pipelines documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops)
- [SLSA specification](https://slsa.dev/spec/)
