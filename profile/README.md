# CapiscIO

<div align="center">

**The Developer-First Trust Layer for AI Agents**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/company/capiscio)
[![Reddit](https://img.shields.io/badge/Reddit-Join-orange?style=flat&logo=reddit)](https://www.reddit.com/r/capiscio)
[![Twitter Follow](https://img.shields.io/twitter/follow/capiscio?style=social)](https://x.com/capiscio)

[Website](https://capisc.io) • [Documentation](https://docs.capisc.io) • [Blog](https://capisc.io/blog) • [Roadmap](https://capisc.io/resources/roadmap)

</div>

---

## ⚡ Zero Trust for the Agent Ecosystem

**CapiscIO** is the open-source standard for **Agent-to-Agent (A2A) Security**. We provide the infrastructure developers need to secure AI agent communication, verify identity, and enforce protocol compliance without the headache.

Stop agent spoofing, replay attacks, and payload tampering in **<1ms**.

### Why CapiscIO?

- **Developer Centric**: CLI-first, CI/CD ready, and drop-in middleware.
- **Protocol Agnostic**: Works with REST, MCP, and the A2A Protocol.
- **Performance Obsessed**: Go-based core, sub-millisecond overhead.

---

## 🛠️ The Open Source Stack

We maintain a suite of high-performance tools to secure the entire agent lifecycle.

### 🏗️ Core Infrastructure

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-core](https://github.com/capiscio/capiscio-core)** | **The Authority Layer.** The high-performance engine for issuing Trust Badges, verifying JWS signatures, and enforcing A2A compliance. | `Go` |

### 🛡️ Runtime Security (Middleware)

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-sdk-python](https://github.com/capiscio/capiscio-sdk-python)** | **Drop-in Enforcement.** Secure your FastAPI, Flask, or Django agents with 3 lines of code. Auto-generates keys and enforces body integrity. | `Python` |

### 🔧 Developer Tooling & CI/CD

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-node](https://github.com/capiscio/capiscio-node)** | **The Official CLI.** Validate agent cards, test endpoints, and check compliance locally. | `TypeScript` |
| **[validate-a2a](https://github.com/capiscio/validate-a2a)** | **GitHub Action.** Automate agent validation in your CI/CD pipeline. Block broken agents before deployment. | `TypeScript` |
| **[capiscio-python](https://github.com/capiscio/capiscio-python)** | **Python CLI Wrapper.** Seamless integration for Python-heavy workflows. | `Python` |

---

## 🗺️ Roadmap: Beyond Validation

With our CLI and Validation tools now **Stable (v1.0)**, we are building the future of Agent Governance.

### 🚀 Q1 2026: The Trust Platform
- **Centralized Registry**: A public ledger for verified agent identities.
- **Trust Badges**: Verifiable credentials for high-quality agents.
- **Dashboard**: Real-time observability for agent traffic and security events.

### 🏛️ Q2 2026: Governance & Policy
- **Policy Engine**: Define organization-wide rules (e.g., "Only talk to agents with Trust Score > 80").
- **Audit Logs**: Immutable records of all agent-to-agent transactions.

[View the full roadmap →](https://capisc.io/resources/roadmap)

---

## 🤝 Contributing

We are building the security standard for the AI era, and we need your help.

1.  **Try the tools**: `npm install -g capiscio-cli`
2.  **Join the discussion**: [Reddit](https://www.reddit.com/r/capiscio)
3.  **Contribute**: Check out "Good First Issues" in any of our repos.

<div align="center">
  <sub>Built with ❤️ by the CapiscIO team. Open Source under Apache 2.0.</sub>
</div>
