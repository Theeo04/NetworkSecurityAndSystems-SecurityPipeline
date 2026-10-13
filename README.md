# Multi-Architecture Debian Package Security Validation

**Network and Systems Security — Master's Semester Project**

## Overview

This project explores how automated static analysis and runtime monitoring can validate the security of Debian packages before release.

A simple application written in **Rust** will be compiled for **AMD64** and **ARM64**, packaged as `.deb` files, and tested in isolated Debian environments.

## Objectives

- Build Debian packages for AMD64 and ARM64 from the same source code.
- Inspect packages, dependencies, and potential vulnerabilities.
- Install and run packages in isolated Debian virtual machines.
- Monitor processes, permissions, filesystem activity, and network behavior.
- Compare security findings across the two architectures.
- Automatically approve or reject release artifacts based on defined security checks.

## Pipeline

```text
Rust Source Code
       |
       v
Build for AMD64 / ARM64
       |
       v
Create .deb Packages
       |
       v
Static Security Analysis
       |
       v
Install in Debian VMs
       |
       v
Runtime Security Tests
       |
       v
Compare Results & Security Gate
       |
       +---- PASS --> Publish Packages
       |
       +---- FAIL --> Reject Release
```

## Planned Security Tests

| Area | What we validate |
| --- | --- |
| Static analysis | Known vulnerabilities, dependencies, package metadata, and file permissions |
| Installation | Package integrity, installation scripts, and system changes |
| Runtime | Process privileges, unexpected child processes, and filesystem activity |
| Network | Listening ports and unexpected connections |
| Compatibility | Installation and execution on AMD64 and ARM64 |

## Technology Candidates

- **Rust** — application development
- **Debian packaging tools** — `.deb` creation and inspection
- **GitLab CI/CD** — pipeline automation
- **Trivy** — vulnerability scanning and SBOM generation
- **Lintian** — Debian package checks
- **QEMU/KVM** — isolated virtual machines
- **Falco / eBPF** — Linux runtime monitoring, where supported

*The exact tooling and test implementation are still being defined.*

## Research Question

> How effectively can automated static security analysis and runtime testing validate Debian packages across AMD64 and ARM64 before release?

## Expected Deliverables

- Automated build and security validation pipeline
- AMD64 and ARM64 Debian packages
- Static analysis and runtime security reports
- Cross-architecture comparison of findings
- Automated PASS/FAIL release decision
- Final research report

## Status

**Planning / design phase.**
