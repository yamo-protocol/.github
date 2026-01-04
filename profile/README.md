# 🌐 YAMO Protocol

### Immutable Provenance for Agentic Reasoning

YAMO is an open protocol that enables AI agents to anchor reasoning traces, intents, and decisions to EVM-compatible blockchains with optional IPFS deep bundling. It provides a unified, verifiable, and cryptographically secure foundation for agentic cognition.

---

## 🚀 Core Repositories

| Repository | Description | Status |
|------------|-------------|--------|
| [**yamo-core**](https://github.com/yamo-protocol/yamo-core) | Shared blockchain/IPFS client library | [![npm version](https://img.shields.io/npm/v/@yamo/core)](https://www.npmjs.com/package/@yamo/core) |
| [**yamo-contracts**](https://github.com/yamo-protocol/yamo-contracts) | UUPS upgradeable smart contracts for on-chain block storage | [![npm version](https://img.shields.io/npm/v/@yamo/contracts)](https://www.npmjs.com/package/@yamo/contracts) |
| [**yamo-cli**](https://github.com/yamo-protocol/yamo-cli) | Developer CLI for creating, hashing, submitting, and auditing YAMO blocks | [![npm version](https://img.shields.io/npm/v/@yamo/cli)](https://www.npmjs.com/package/@yamo/cli) |
| [**yamo-mcp-server**](https://github.com/yamo-protocol/yamo-mcp-server) | Model Context Protocol bridge enabling agents (Claude, etc.) to submit blocks | [![npm version](https://img.shields.io/npm/v/@yamo/mcp-server)](https://www.npmjs.com/package/@yamo/mcp-server) |
| [**yamo-explorer**](https://github.com/yamo-protocol/yamo-explorer) | Next.js web dashboard for visualizing and auditing reasoning chains | |

## 📚 Standards & Resources

| Repository | Description |
|------------|-------------|
| [**yamo-rfcs**](https://github.com/yamo-protocol/yamo-rfcs) | Standards-track proposals for the YAMO protocol |
| [**yamo-examples**](https://github.com/yamo-protocol/yamo-examples) | Minimal examples and starter templates |

---

## ✨ Key Features

- **🆓 Zero Cost**: Free blockchain anchoring on Ethereum Sepolia
- **🔒 Immutable Storage**: Cryptographically anchored reasoning traces on EVM blockchains
- **📦 IPFS Deep Bundling**: Store full content and artifacts with content-addressable CIDs
- **🤝 Multi-Agent Workflows**: Native support for agent handoffs and consensus
- **🔍 Full Auditability**: Verify any block's integrity via on-chain hash verification or [Etherscan](https://sepolia.etherscan.io/address/0x3c9440fa8d604E732233ea17095e14be1a53b015)
- **🛠 Developer-Friendly**: CLI, MCP server, and TypeScript SDKs with GitHub installation
- **⚡ Upgradeable**: UUPS proxy pattern for contract evolution

---

## 🎯 Quick Start

Visit **[www.soverane.net](https://www.soverane.net)** for the complete protocol overview.

### 🆓 Free & Live on Sepolia

YAMO is deployed on **Ethereum Sepolia** - providing permanent, public blockchain anchoring at **zero cost**:

- **Contract**: [`0x3c9440fa8d604E732233ea17095e14be1a53b015`](https://sepolia.etherscan.io/address/0x3c9440fa8d604E732233ea17095e14be1a53b015)
- **Network**: Sepolia (Chain ID: 11155111)
- **RPC**: `https://rpc.sepolia.org` (free)
- **Cost**: $0 - Sepolia ETH is free from faucets

### Install the CLI

```bash
# Clone the repository
git clone https://github.com/yamo-protocol/yamo-cli.git
cd yamo-cli

# Install and build
npm install && npm run build

# Configure (defaults to Sepolia)
cp .env.example .env

# Use locally (no global install needed)
npm start -- init MyAgent
npm start -- hash myfile.yamo
npm start -- submit myfile.yamo
npm start -- audit block_001
```

**Or install globally:**

```bash
sudo npm link
yamo init MyAgent
```

**Or install from npm:**

```bash
npm install -g @yamo/cli
yamo init MyAgent
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
  ┌──────────────────────────────────────┐
  │       YAMORegistryV2 (UUPS)          │
  │  0x3c9440fa8d604E732233ea17095e14... │
  │                                      │
  │      Ethereum Sepolia (FREE)         │
  │   https://rpc.sepolia.org            │
  └──────────────────────────────────────┘
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

## 🌐 Network Deployment

YAMO Protocol is live on **Ethereum Sepolia** as the production network:

### Why Sepolia (Not Mainnet)?

For AI reasoning provenance, Sepolia provides everything we need:

✅ **Permanent** - Real blockchain, immutable records
✅ **Public** - Verifiable on [Sepolia Etherscan](https://sepolia.etherscan.io)
✅ **Free** - Zero gas costs for users (Sepolia ETH is free)
✅ **Secure** - Same cryptographic guarantees as mainnet
✅ **Production-Ready** - Stable since 2022, not going anywhere

❌ **Don't Need** - Financial value, DeFi integration, or token functionality

**Contract Details:**
- **Address**: `0x3c9440fa8d604E732233ea17095e14be1a53b015`
- **Explorer**: https://sepolia.etherscan.io/address/0x3c9440fa8d604E732233ea17095e14be1a53b015
- **RPC**: https://rpc.sepolia.org
- **Chain ID**: 11155111

Get free Sepolia ETH: [sepoliafaucet.com](https://sepoliafaucet.com)

---

## 🌍 Links

- **Website**: https://www.soverane.net
- **Contract**: https://sepolia.etherscan.io/address/0x3c9440fa8d604E732233ea17095e14be1a53b015
- **Documentation**: https://github.com/yamo-protocol
- **RFCs**: https://github.com/yamo-protocol/yamo-rfcs
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
