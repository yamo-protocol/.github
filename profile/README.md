# 🌐 YAMO Protocol

### Immutable Provenance for Agentic Reasoning

YAMO is an open protocol that enables AI agents to anchor reasoning traces, intents, and decisions to EVM-compatible blockchains with optional IPFS deep bundling. It provides a unified, verifiable, and cryptographically secure foundation for agentic cognition.

---

## 🚀 Core Repositories

| Repository | Description | Status |
|------------|-------------|--------|
| [**yamo-core**](https://github.com/yamo-protocol/yamo-core) | Shared blockchain/IPFS client library | ![Version](https://img.shields.io/badge/version-1.0.0-blue) |
| [**yamo-cli**](https://github.com/yamo-protocol/yamo-cli) | Developer CLI for creating, hashing, submitting, and auditing YAMO blocks | ![Version](https://img.shields.io/badge/version-1.0.0-blue) |
| [**yamo-contracts**](https://github.com/yamo-protocol/yamo-contracts) | UUPS upgradeable smart contracts for on-chain block storage | ![Version](https://img.shields.io/badge/version-1.0.0-blue) |
| [**yamo-explorer**](https://github.com/yamo-protocol/yamo-explorer) | Next.js web dashboard for visualizing and auditing reasoning chains | ![Version](https://img.shields.io/badge/version-1.0.0-blue) |
| [**yamo-mcp-server**](https://github.com/yamo-protocol/yamo-mcp-server) | Model Context Protocol bridge enabling agents (Claude, etc.) to submit blocks | ![Version](https://img.shields.io/badge/version-1.0.0-blue) |

## 📚 Standards & Resources

| Repository | Description |
|------------|-------------|
| [**yamo-rfcs**](https://github.com/yamo-protocol/yamo-rfcs) | Standards-track proposals for the YAMO protocol |
| [**yamo-examples**](https://github.com/yamo-protocol/yamo-examples) | Minimal examples and starter templates |

---

## ✨ Key Features

- **🔒 Immutable Storage**: Cryptographically anchored reasoning traces on EVM blockchains
- **📦 IPFS Deep Bundling**: Store full content and artifacts with content-addressable CIDs
- **🤝 Multi-Agent Workflows**: Native support for agent handoffs and consensus
- **🔍 Full Auditability**: Verify any block's integrity via on-chain hash verification
- **🛠 Developer-Friendly**: CLI, MCP server, and TypeScript SDKs
- **⚡ Upgradeable**: UUPS proxy pattern for contract evolution

---

## 🎯 Quick Start

Visit **[www.soverane.net](https://www.soverane.net)** for the complete protocol overview.

### Install the CLI

```bash
npm install -g @yamo/cli
```

### Initialize a YAMO Block

```bash
yamo init MyAgent
```

### Submit to Blockchain

```bash
yamo submit my-block.yamo
```

### Verify Block Integrity

```bash
yamo audit block_001
```

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        AI Agents                             │
│          (Claude, GPT, Custom Agents, etc.)                  │
└────────────────────┬────────────────────────────────────────┘
                     │
                     ▼
          ┌──────────────────────┐
          │   YAMO MCP Server    │
          │  (Tool Integration)  │
          └──────────┬───────────┘
                     │
         ┌───────────┴───────────┐
         │                       │
         ▼                       ▼
  ┌─────────────┐         ┌─────────────┐
  │ YAMO Core   │         │    IPFS     │
  │ (ethers.js) │         │  (Pinata)   │
  └──────┬──────┘         └─────────────┘
         │
         ▼
  ┌─────────────────────┐
  │  YAMORegistryV2     │
  │  Smart Contract     │
  │  (EVM Blockchain)   │
  └─────────────────────┘
```

---

## 📖 Protocol Specification

YAMO blocks use a structured DSL format (`.yamo` files):

```yamo
agent: TranslationAgent;
intent: translate_document;
context: platform;yamo_protocol_v0.4;
constraints:
  - language;en_to_fr;
  - preserve_formatting;true;
priority: high;
output: translated.txt;
meta: model;claude-3-opus;
log: translation_complete;timestamp;2025-01-02T00:00Z;
handoff: ValidationAgent;
```

Each block is:
1. Hashed (SHA256)
2. Uploaded to IPFS (optional, with artifacts)
3. Anchored on-chain with hash + CID
4. Verifiable by anyone

See [RFC-0001](https://github.com/yamo-protocol/yamo-rfcs/blob/main/RFC-0001-yamo-v1.0.md) for the full specification.

---

## 🤝 Contributing

We welcome contributions of all kinds! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

### Ways to Contribute

- 🐛 Report bugs and issues
- 💡 Propose new features via RFCs
- 📝 Improve documentation
- 🔧 Submit pull requests
- 💬 Join discussions

---

## 🔐 Security

Security is paramount. If you discover a vulnerability, please email:

**security@yamo.org**

Do not open public issues for security concerns. See [SECURITY.md](./SECURITY.md) for our full policy.

---

## 📜 License

All repositories are released under the [MIT License](https://opensource.org/licenses/MIT) unless otherwise noted.

---

## 🌍 Links

- **Website**: https://www.soverane.net
- **Documentation**: https://github.com/yamo-protocol
- **Discord**: Coming soon
- **Twitter**: Coming soon

---

## 🏛 Governance

YAMO is governed through a transparent, community-driven RFC process inspired by IETF and Ethereum EIP workflows. Protocol changes are proposed, discussed, and ratified through the [yamo-rfcs](https://github.com/yamo-protocol/yamo-rfcs) repository.

---

<p align="center">
  <strong>Building the future of transparent, verifiable agentic reasoning.</strong>
</p>

<p align="center">
  Made with ❤️ by the YAMO community
</p>
