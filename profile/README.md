# CapiscIO

<div align="center">

**The identity and integrity guard for AI agents**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/company/capiscio)
[![Reddit](https://img.shields.io/badge/Reddit-Join-orange?style=flat&logo=reddit)](https://www.reddit.com/r/capiscio)
[![Twitter Follow](https://img.shields.io/twitter/follow/capiscio?style=social)](https://x.com/capiscio)

[Website](https://capisc.io) • [Documentation](https://docs.capisc.io) • [Blog](https://capisc.io/blog) • [Roadmap](https://capisc.io/platform)

</div>

---

## ⚡ What CapiscIO Does

CapiscIO is an open source **runtime guard** for AI agents.

We enforce:

- **Identity** – Ed25519 signed envelopes so you know which agent actually called you.  
- **Payload integrity** – SHA-256 body hashing so tampered requests are rejected.  
- **Freshness** – strict `iat` / `exp` checks so replayed traffic die on arrival.

All with **sub-millisecond overhead** in Python and Go.

Use CapiscIO as:

- A **Python SDK** (SimpleGuard) to guard your agent endpoints.  
- A **Go middleware / sidecar** in front of HTTP services.  
- A **Docker sidecar** (`capiscio/guard`) for containerized deployments.  
- A **CLI** (Node or Python) to validate agent cards and test endpoints in CI.

---

## 🤔 Why CapiscIO?

- **Developer first**  
  CLI ready, CI friendly, and a drop-in guard you can wire in with a couple of lines.

- **Protocol aware**  
  Built for A2A and MCP protocols. Guards both agent-to-agent and agent-to-tool communication.

- **Performance obsessed**  
  Go based core and a pure Python guard, both adding well under 1 ms per call in our benchmarks.

---

## 🛠️ The Open Source Stack

We keep the stack small and focused: core enforcement, runtime guard, and CLI tooling.

### 🧠 Core Enforcement

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-core](https://github.com/capiscio/capiscio-core)** | High performance enforcement engine used by sidecars and CLIs. Verifies Ed25519 JWS envelopes, enforces body hashes, and checks timestamps with microsecond-level overhead. Also available as `capiscio/guard` Docker image. | `Go` |

### 🛡️ Runtime Guard (SDK)

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-sdk-python](https://github.com/capiscio/capiscio-sdk-python)** | Drop-in guard for Python services (FastAPI / Flask / etc). Auto-discovers keys, enforces identity, payload integrity, and replay protection at the HTTP boundary. | `Python` |

### 🔧 Developer Tooling & CLI

Both CLIs wrap `capiscio-core`, so dev-time checks and runtime enforcement share the same semantics.

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-node](https://github.com/capiscio/capiscio-node)** | Node-based `capiscio` CLI. Validate agent cards, test live endpoints, and run security checks locally or in CI. | `TypeScript / Node` |
| **[capiscio-python](https://github.com/capiscio/capiscio-python)** | Python package `capiscio` exposing the same CLI experience and core behaviour for Python-centric environments. | `Python` |
| **[validate-a2a](https://github.com/capiscio/validate-a2a)** | GitHub Action that runs the `capiscio` CLI in your pipeline. Validates agent cards, enforces Proof of Possession, and checks MCP server compliance. | `TypeScript` |

### 🌐 Registry & Control Plane _(Beta)_

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[capiscio-server](https://github.com/capiscio/capiscio-server)** | Registry API and Certificate Authority. Issues Trust Badges (RFC-002), manages agent/MCP server identities, and provides key discovery. | `Go` |

---

## 🗺️ Roadmap: From Guard to Platform

Today, CapiscIO ships the **guard and tooling**. We’re working with design partners on the next layers.

### Stage 1 – The Guard _(Live)_

- Local enforcement SDK (Python) and Go middleware / sidecars.  
- Identity, integrity, and freshness checks at the protocol boundary.  
- `capiscio` CLI (Node and Python) plus GitHub Action for dev-time and CI validation.

### Stage 2 – The Registry _(Beta)_

- Centralized discovery of trusted agent and MCP server keys.  
- Trust Badges with 5 validation levels (Self-Signed → Extended Validation).  
- MCP Server Registry for tool identity management.  
- Managed key lifecycle and trust stores for teams running many agents.

### Stage 3 – The Platform _(Planned)_

- Cross-agent observability and traces.  
- Policy and governance over which agents can call which tools.  
- Audit-friendly exports for your existing SIEM / compliance stack.

We are intentionally **co-designing** Stage 2 and 3 with a small set of design partners.

[Read more about the architecture and roadmap →](https://capisc.io/platform)

---

## 🤝 Contributing

We’re building the security layer we wish existed before everyone deployed multi-agent systems.

You can help by:

1. **Trying the tools**

   ```bash
   # Node CLI (recommended entry point)
   npm install -g capiscio

   # Python CLI wrapper (if you prefer Python tooling)
   pip install capiscio

   # Python guard SDK
   pip install capiscio-sdk

   # Docker sidecar
   docker pull capiscio/guard

2.  **Join the discussion**:
 - [Reddit](https://www.reddit.com/r/capiscio)
 - [LinkedIn](https://www.linkedin.com/company/capiscio)
 - [X](https://x.com/capiscio)
3.  **Contribute**: Check out "Good First Issues" in any of our repos. 
Open issues if you hit edge cases securing agents in the wild.

<div align="center">
  <sub>Built with ❤️ by the CapiscIO team. Open Source under Apache 2.0.</sub>
</div>
