# Contributing to YAMO

Thank you for your interest in contributing to the YAMO ecosystem!  
We welcome contributions of all kinds — code, documentation, RFCs, examples, and feedback.

## 🧱 Code of Conduct

By participating, you agree to uphold the YAMO Code of Conduct. We are committed to providing a welcoming and inclusive environment for all contributors.

## 🛠 Development Setup

Each repository includes setup instructions in its README.  
Most projects use:
- Node.js 18+
- npm workspaces (or standalone packages)
- Hardhat (contracts)
- Next.js (explorer)
- TypeScript

### Getting Started

1. **Fork the repository** you want to contribute to
2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
   cd REPO_NAME
   ```
3. **Install dependencies**:
   ```bash
   npm install
   ```
4. **Build the project**:
   ```bash
   npm run build
   ```

## 🧪 Testing

Please ensure all tests pass before submitting a PR:

```bash
npm test
```

For specific packages:
```bash
cd packages/core && npm test
cd packages/contracts && npx hardhat test
```

## 🔀 Branching Strategy

- `main` — stable releases
- `dev` — active development (if applicable)
- feature branches: `feature/<name>`
- fix branches: `fix/<name>`

## 📝 Pull Requests

1. **Fork** the repository
2. **Create a feature branch** from `main`
3. **Write clear commit messages** following [Conventional Commits](https://www.conventionalcommits.org/)
4. **Ensure tests pass** and code is properly formatted
5. **Submit PR** with a clear description of:
   - What problem it solves
   - How it solves it
   - Any breaking changes
   - Screenshots (if UI changes)

### PR Checklist

- [ ] Tests added/updated
- [ ] Documentation updated
- [ ] Code follows project style guidelines
- [ ] Commit messages are clear
- [ ] No merge conflicts
- [ ] All CI checks pass

## 📄 RFC Contributions

For protocol-level changes, propose an RFC in the [yamo-rfcs](https://github.com/yamo-protocol/yamo-rfcs) repository.

1. Copy `template.md`
2. Name it `RFC-XXXX-descriptive-title.md`
3. Fill in all sections
4. Open a PR for discussion
5. Participate in community feedback

See [RFC Process](https://github.com/yamo-protocol/yamo-rfcs#how-to-submit-an-rfc) for details.

## 🎨 Code Style

- **TypeScript**: Follow the existing style in each repo
- **Solidity**: Follow [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html)
- **Formatting**: Run `npm run format` if available
- **Linting**: Run `npm run lint` to check code quality

## 📚 Documentation

Good documentation is crucial:
- Update README files when adding features
- Add inline comments for complex logic
- Include JSDoc/TSDoc for public APIs
- Update examples if behavior changes

## 🐛 Bug Reports

Found a bug? Please open an issue with:
- Clear title and description
- Steps to reproduce
- Expected vs actual behavior
- Environment details (Node version, OS, etc.)
- Relevant logs or screenshots

## 💡 Feature Requests

Have an idea? Open an issue or discussion with:
- Clear use case description
- Why it's valuable
- Potential implementation approach
- Any alternatives considered

## 🙏 Thank You

Your contributions help build the future of transparent, verifiable agentic reasoning.

Every contribution, no matter how small, makes a difference. We appreciate your time and effort! ❤️

---

## 📞 Questions?

- Open a [Discussion](https://github.com/orgs/yamo-protocol/discussions)
- Join our Discord (coming soon)
- Email: hello@yamo.org
