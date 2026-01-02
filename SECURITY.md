# Security Policy

## Supported Versions

Security updates apply to the latest stable release of each YAMO repository.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

**Please do not open public GitHub issues for security vulnerabilities.**

If you discover a security issue, please email:

**security@soverane.net**

### What to Include

Please provide:
- Description of the vulnerability
- Steps to reproduce
- Affected versions/components
- Potential impact
- Suggested fix (if any)

### Response Timeline

We will:
- **Acknowledge receipt** within 48 hours
- **Provide an initial assessment** within 5 business days
- **Work with you** on a coordinated disclosure timeline
- **Credit you** in the security advisory (if desired)

## Scope

This security policy covers:

### In Scope

- **Smart Contracts** (`yamo-contracts`)
  - Access control vulnerabilities
  - Reentrancy issues
  - Integer overflow/underflow
  - Upgrade mechanism exploits
  
- **IPFS Bundling** (`yamo-core`)
  - Content hash manipulation
  - CID verification bypass
  - Malicious content injection

- **Chain Client Logic** (`yamo-core`)
  - Transaction signing vulnerabilities
  - Private key handling
  - RPC endpoint exploits

- **MCP Server** (`yamo-mcp-server`)
  - Authentication bypass
  - Command injection
  - Unauthorized blockchain operations

- **CLI Tools** (`yamo-cli`)
  - Command injection
  - Path traversal
  - Credential exposure

### Out of Scope

- Third-party dependencies (report to upstream)
- Local development environments
- Social engineering attacks
- DDoS attacks
- Issues requiring physical access

## Security Best Practices

When using YAMO:

### For Developers

1. **Never commit private keys** to version control
2. **Use environment variables** for sensitive configuration
3. **Validate all inputs** before blockchain submission
4. **Keep dependencies updated** regularly
5. **Audit smart contract upgrades** before deployment

### For Node Operators

1. **Secure RPC endpoints** with proper authentication
2. **Monitor transaction activity** for anomalies
3. **Use hardware wallets** for production deployments
4. **Implement rate limiting** on public endpoints
5. **Regular security audits** of infrastructure

### For Contract Deployers

1. **Test thoroughly** on testnets before mainnet
2. **Perform security audits** before production deployment
3. **Implement timelocks** for upgrades
4. **Use multisig wallets** for contract ownership
5. **Monitor events** for suspicious activity

## Known Security Considerations

### Smart Contracts

- Uses OpenZeppelin's audited libraries
- UUPS pattern requires careful upgrade management
- Owner key security is critical for upgrades

### IPFS Storage

- Content is public on IPFS
- CIDs are deterministic (content-addressable)
- Pin services may cache content

### Private Keys

- Never share or commit private keys
- Use environment variables or secure vaults
- Consider hardware wallets for production

## Security Audits

Security audit status:

- **Smart Contracts**: Pending (v1.0.0)
- **Core Library**: Internal review completed
- **MCP Server**: Internal review completed

We welcome community security reviews and will credit all responsible disclosures.

## Disclosure Policy

We follow **coordinated disclosure**:

1. Security issue reported privately
2. Issue confirmed and severity assessed
3. Patch developed and tested
4. Security advisory published
5. Patch released with version bump
6. Public disclosure after users can update

Typical timeline: 30-90 days depending on severity.

## Bug Bounty Program

Coming soon. Watch this space for announcements.

## Contact

- **Security Email**: security@yamo.org
- **PGP Key**: Coming soon

---

Thank you for helping keep YAMO and our community safe! 🔐
