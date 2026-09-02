# YAMO Protocol — Archived

**Status: archived, September 2026.** The YAMO chain protocol — anchoring agent
reasoning traces to Ethereum Sepolia with optional IPFS bundling — is no longer
developed or maintained. The repositories below are kept read-only as a record.

- The npm packages `@yamo/cli`, `@yamo/core`, and `@yamo/mcp-server` are
  deprecated. Existing installs keep working but receive no updates or security
  fixes. Do not start new work on them.
- The Sepolia contract at `0x3c9440fa8d604E732233ea17095e14be1a53b015` remains
  on-chain but is unmaintained.
- The account of the thesis, and why it was retired, is at
  **[soverane.net](https://www.soverane.net)**.

## Repositories

| Repository | Was | Status |
|------------|-----|--------|
| [yamo-core](https://github.com/yamo-protocol/yamo-core) | Shared blockchain/IPFS client library (`@yamo/core`) | Archived |
| [yamo-contracts](https://github.com/yamo-protocol/yamo-contracts) | UUPS upgradeable contracts for on-chain block storage | Archived |
| [yamo-cli](https://github.com/yamo-protocol/yamo-cli) | Developer CLI for creating, hashing, submitting, and auditing blocks (`@yamo/cli`) | Archived |
| [yamo-mcp-server](https://github.com/yamo-protocol/yamo-mcp-server) | Model Context Protocol bridge for submitting blocks (`@yamo/mcp-server`) | Archived |
| [yamo-explorer](https://github.com/yamo-protocol/yamo-explorer) | Next.js dashboard for auditing reasoning chains | Archived |
| [yamo-rfcs](https://github.com/yamo-protocol/yamo-rfcs) | Standards-track proposals; RFC-0001 is the protocol specification | Reference |
| [yamo-examples](https://github.com/yamo-protocol/yamo-examples) | Minimal examples and starter templates | Reference |

## Still active

`@yamo/memory-mesh`, the agent memory layer published under the same npm scope,
is a separate project and is **not** part of this retirement. It continues to be
developed: [npmjs.com/package/@yamo/memory-mesh](https://www.npmjs.com/package/@yamo/memory-mesh).

## License

All repositories are released under the [MIT License](https://opensource.org/licenses/MIT) unless otherwise noted.
