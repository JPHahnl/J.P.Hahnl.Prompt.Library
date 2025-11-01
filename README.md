# 🧠 Sys.Kernel Framework  
**A Unified Architecture for C# 13 / .NET 9**  
*Built with Clarity · Strength · Dignity*

---

## 🌌 Vision

**Sys.Kernel** is not just a framework — it’s a principle.  
It redefines how .NET systems are structured, verified, and evolved.  
Every layer, every analyzer, every build step serves one goal:  
> **To bring discipline, determinism, and dignity back to software architecture.**

This repository contains both the **Sys.Kernel framework** itself and the **AI prompt library** that designs, verifies, and documents it — an end-to-end ecosystem for next-generation C# development.

---

## 🧱 Core Concept

Sys.Kernel is a *layered, analyzer-clean, runtime-verified framework* written for **C# 13 / .NET 9**.

### Architectural Model
```
Sdk → Core → Runtime → Diagnostics → Development
                ↑
             (Tests)
```

| Layer | Description |
|:--|:--|
| **Kernel.Sdk** | The self-describing SDK layer. Defines attributes, constants, exceptions, and T4/MSBuild-generated metadata. Serves as the interface to the build and compiler. |
| **Kernel.Core** | Extends Sdk with functional primitives, immutables, and runtime-safe abstractions. |
| **Kernel.Runtime** | Execution engine of Sys.Kernel — service hosting, configuration, dependency injection, and lifecycle management. |
| **Kernel.Diagnostics** | Logging, tracing, EventSource, and OpenTelemetry integration. |
| **Kernel.Development** | Analyzers, templates, and tooling for VS and CI/CD environments. |
| **Kernel.Tests** | Verification suite for architecture, performance, security, and stability. |

---

## ⚙️ Technology Stack

- **Language:** C# 13  
- **Framework:** .NET 9  
- **Build System:** MSBuild + deterministic builds  
- **Testing:** NUnit 4.4  
- **Code Analysis:**  
  - `Meziantou.Analyzer`  
  - `Microsoft.CodeAnalysis.NetAnalyzers`  
  - `Roslynator.Analyzers`  
  - `SonarAnalyzer.CSharp`  
  - `NetArchTest.Rules`  
  - `AsyncFixer`  
  - `PublicApiAnalyzers`

All projects must compile with **0 analyzer warnings**.  
No `#pragma` suppressions — ever.

---

## 🧩 Included Prompts

This repository also includes the **Sys.Kernel AI Prompt Library** — a structured set of domain-specific prompts that orchestrate architecture, diagnostics, and framework evolution using AI-assisted analysis.

| Prompt | Purpose |
|:--|:--|
| [SysKernel.Master.prompt.v4.0.md](./SysKernel.Master.prompt.v4.0.md) | Master orchestration prompt integrating all sub-domains. |
| [Architecture_Verification.prompt.v3.1.md](./Architecture_Verification.prompt.v3.1.md) | Validates layering, dependencies, and modular integrity. |
| [API_Stability_Versioning.prompt.v3.1.md](./API_Stability_Versioning.prompt.v3.1.md) | Enforces SemVer, API stability, and changelog compliance. |
| [Security_SafeDefaults.prompt.v3.1.md](./Security_SafeDefaults.prompt.v3.1.md) | Defines secure-by-default patterns and cryptography standards. |
| [Diagnostics_Telemetry.prompt.v3.1.md](./Diagnostics_Telemetry.prompt.v3.1.md) | Establishes structured EventSource telemetry and observability. |
| [nunit_test_generation.prompt.v3.1.md](./nunit_test_generation.prompt.v3.1.md) | Generates NUnit 4.4 tests with retry/timeouts. |
| [documentation.prompt.v3.1.md](./documentation.prompt.v3.1.md) | Enforces XML + DevDoc consistency. |
| [better_naming.prompt.v3.1.md](./better_naming.prompt.v3.1.md) | Governs identifier and naming consistency. |
| [thread_safety_concurrency.prompt.v3.1.md](./thread_safety_concurrency.prompt.v3.1.md) | Ensures concurrency correctness and lock-free safety. |

A complete overview is available in the  
📖 [SysKernel_PromptLibrary_Index.md](./SysKernel_PromptLibrary_Index.md)

---

## 🧮 CI/CD Integration

Every commit is automatically verified via GitHub Actions:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Build
        run: dotnet build --configuration Release --deterministic
      - name: Test
        run: dotnet test --filter Category!=Integration
      - name: Analyzer Validation
        run: dotnet format analyzers --verify-no-changes
      - name: Architecture Rules
        run: dotnet test --filter Category=Architecture
```

---

## 🧠 Design Principles

1. **Analyzer-Clean by Design**  
   Every commit is a promise of quality.  
   Warnings are signals of broken clarity.

2. **Self-Describing Architecture**  
   Build metadata and SDK generation ensure transparency between the developer, build system, and runtime.

3. **Runtime Minimalism**  
   Each layer serves one purpose — no reflection magic, no hidden coupling.

4. **Deterministic Builds**  
   Every artifact can be reproduced exactly, ensuring consistency across environments.

5. **The Königsweg**  
   - **Clarity** → Know what your code means.  
   - **Strength** → Make it resilient, measurable, and testable.  
   - **Würde (Dignity)** → Build with intention and respect for complexity.

---

## 🧭 Philosophy

> “A framework should not just run — it should *reveal* its structure.  
>  Sys.Kernel is a living mirror of the system that builds it.”  
>  — *Josef Hahnl, Syntony Austria*

---

## 📜 License

© 2025 Josef Hahnl — Syntony Austria  
All rights reserved.  
For inquiries, licensing, or collaboration opportunities, contact via [SyntonyAustria](https://syntonyblog.wordpress.com/).

---
