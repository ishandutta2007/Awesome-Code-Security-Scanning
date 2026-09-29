# Awesome-Code-Security-Scanning

# Top Code Security Scanning Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on SAST, SCA, Secrets Detection & Application Security Posture Management*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Code Security Scanning**. These tools help developers and security teams identify vulnerabilities in first-party code, detect vulnerable open-source dependencies, find hardcoded secrets, and manage application security posture across the SDLC.

**Examples** include Snyk, Semgrep, SonarQube, Checkmarx, Veracode, Mend.io, GitGuardian, OX Security, Apiiro, and ArmorCode (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom rule authoring, and transparent security scanning — ideal for teams that need full control over their code security pipeline without per-developer SaaS fees or vendor lock-in.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Snyk](https://snyk.io/)**
  Developer-first security platform covering SAST (Snyk Code), SCA (Snyk Open Source), container, and IaC scanning. Recent updates include support for stripped/CGo Go binaries, Yarn 4, Ruby 4, PHP 8.5, Swift 6.2, and improved Python pip performance for large ML projects like PyTorch . Snyk Code added C# 14/.NET 10, Kotlin Spring WebFlux/Jax-RS, Go Fiber, and Swift grpc-swift support in February 2026 .

- **[Semgrep](https://semgrep.dev/)**
  Fast, lightweight static analysis platform with unified SAST, SCA, and Secrets scanning. Semgrep Code supports 20+ languages including C/C++, Go, Java, JavaScript, Python, Ruby, Rust, and Terraform . March 2026 introduced AI-powered detection for IDORs and broken authorization, Autofix beta for Code findings, and Cursor/Claude Code plugins . The Semgrep AppSec Platform provides triage workflows and CI/CD integration .

- **[SonarQube](https://www.sonarsource.com/)**
  Industry-standard code quality and security platform with 5,000+ rules across 30+ languages . Provides IDE extensions (IntelliJ, VS Code, Visual Studio, Eclipse) with real-time analysis, plus server/cloud for pull request analysis and CI/CD quality gates . The Sonar way quality profile is built-in for each language .

- **[Checkmarx](https://checkmarx.com/)**
  Enterprise SAST with hybrid query-and-AI engine (Checkmarx Fusion) delivering 70% better fidelity and 60% fewer false positives . Recent updates include SAST engine 9.7.7, AI Triage for SCA, native reachability analysis for Python/Java/JavaScript/C#, and MCP Server for risk triage via AI assistants .

- **[Veracode](https://www.veracode.com/)**
  Enterprise static analysis and SCA platform. Scans compiled binaries with debug information for accurate findings . Supports precompiled ASP.NET, .NET, and Java artifacts. Mobile Behavioral Analysis reviews app permissions for over-permissioning risks .

- **[Mend.io](https://www.mend.io/)**
  Strong Performer in Forrester Wave SCA Q4 2024, scoring highest in prioritization/reachability, remediation/automation, malicious package detection, language support (200+), AI component analysis, and pricing transparency . Generates SBOMs in SPDX, CycloneDX, and VEX formats .

- **[GitGuardian](https://www.gitguardian.com/)**
  Secrets detection and remediation platform. Scans Explore results for secrets with type, severity, confidence, source context, and patch details . GitHub PR integration posts check runs and timeline comments, with customizable remediation guidelines and public share links for incident details .

- **[OX Security](https://www.ox.security/)**
  ASPM platform focused on filtering noise and fixing real risk. Provides evidence-based prioritization (reachability, exploitability, impact), root cause consolidation, no-code remediation, and native pipeline enforcement .

- **[Apiiro](https://apiiro.com/)**
  Agentic application security platform with AutoFix AI Agent. Partnership with Akamai delivers comprehensive API security, unified governance, and prioritized remediation connecting runtime and code-level insights .

- **[ArmorCode](https://www.armorcode.com/)**
  AI-powered ASPM platform with 285+ integrations and 25B+ findings analyzed. Features Anya, an agentic AI for conversational security queries, vulnerability insights, real-time recommendations, and automated actions via MCP .

## Open-Source GitHub Projects

- **[Semgrep CE](https://github.com/semgrep/semgrep)**
  The open-source program analysis engine at the heart of Semgrep. Suitable for ad-hoc scanning, security audits, and pentesting with tolerance for false positives . Supports intraprocedural analysis (single-function scope) for fast, lightweight scanning. Rules are transparent and customizable. Install via `brew install semgrep` or `pip install semgrep`. **LGPL 2.1** (with some Pro rules under commercial license).

- **[argus](https://github.com/argus-ffi/argus)**
  High-performance, multi-threaded secrets scanner written in Rust. Detects secrets, keys, and sensitive information with deep analysis heuristics: Story Mode (natural language risk explanations), Sink Provenance (data flow to network/disk/log sinks), Leak Velocity, Credential Shadowing, Lateral Linkage, and Surface Tension . Supports WASM for in-memory scanning. Risk Heatmap and Flow Context Graph visualization. **Open source**.

- **[OSV-SCALIBR](https://github.com/google/osv-scalibr)**
  Google's open-source software inventory extraction and security finding detection library. Scans containers, filesystems, and source repositories for packages and vulnerabilities using plugins . Supports ScanConfig with capabilities, scan roots, max file size, gitignore handling, and symlink reading. **Apache-2.0**.

### Additional Strong Open-Source Options

- **SAST Engines**: **Semgrep CE** (transparent rules, fast), **CodeQL** (GitHub, semantic code analysis).
- **Secrets Scanning**: **argus** (Rust, deep heuristics, WASM support), **Gitleaks** (repo-focused), **TruffleHog** (800+ secret types).
- **SCA/SBOM**: **OSV-SCALIBR** (Google, plugin-based), **Syft** (SBOM generation), **Grype** (vulnerability scanning).
- **IaC Scanning**: **Checkov** (Bridgecrew, multi-cloud), **KICS** (Checkmarx, open-source).

**Frameworks for building custom systems**: Combine **Semgrep CE** for SAST with custom rules, **argus** for secrets detection with deep heuristics, **OSV-SCALIBR** for SCA and SBOM generation, and **Checkov** for IaC scanning. Add **GitHub Actions** or **GitLab CI** for pipeline integration and **SARIF** output for IDE/PR annotations.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Code security scanning tools handle sensitive vulnerability and credential data; ensure proper access controls and secure storage of findings.
- **Open-source reality**: The open-source ecosystem for code security is **mature and production-ready**. **Semgrep CE** provides a transparent SAST engine with customizable rules . **argus** offers deep secrets detection with novel heuristics like Sink Provenance and Leak Velocity . **OSV-SCALIBR** provides Google-backed SCA and SBOM generation . For enterprise-grade ASPM with unified triage across SAST/SCA/secrets/IaC, commercial platforms (Snyk, Semgrep Platform, ArmorCode, OX Security) offer broader integration and AI-powered remediation that open-source tools require significant assembly to match.

---

**Made for security engineers, AppSec teams, DevSecOps practitioners, and developers building secure software.**
Let's make code security scanning more open, transparent, and developer-friendly.
