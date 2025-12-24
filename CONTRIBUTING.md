# Contributing to Neural Garage

Thank you for considering contributing to Neural Garage! We're building next-generation, AI-powered code analysis tools, and we'd love your help.

## Ways to Contribute

- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🧪 Add test cases
- 🔧 Fix issues
- 🚀 Implement new features
- 🌍 Add language support

## Getting Started

### 1. Fork and Clone

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/YOUR_USERNAME/bury.git
cd bury
```

### 2. Set Up Development Environment

```bash
# Install Rust (if not already installed)
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Install dependencies
cargo build

# Run tests
cargo test

# Run locally
cargo run -- --help
```

See [DEVELOPMENT.md](https://github.com/neural-garage/bury/blob/main/DEVELOPMENT.md) for detailed setup instructions.

### 3. Create a Branch

```bash
git checkout -b feature/my-awesome-feature
# or
git checkout -b fix/bug-description
```

## Development Workflow

### Before You Code

1. Check existing [issues](https://github.com/neural-garage/bury/issues) and [discussions](https://github.com/neural-garage/bury/discussions)
2. For major changes, open an issue first to discuss
3. Make sure tests pass: `cargo test`

### While Coding

1. Follow Rust best practices
2. Write tests for new functionality
3. Update documentation as needed
4. Run `cargo fmt` to format code
5. Run `cargo clippy` to catch common mistakes
6. Ensure all tests pass

### Code Style

We use standard Rust formatting:

```bash
# Format code
cargo fmt

# Lint code
cargo clippy --all-targets --all-features -- -D warnings

# Run all checks
make all  # (if available)
```

### Commit Messages

Write clear, concise commit messages:

```
feat: add support for Java parsing
fix: correct false positive in method detection
docs: update installation instructions
test: add test cases for Python parser
chore: update dependencies
```

Use conventional commits:
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation only
- `test:` - Adding tests
- `refactor:` - Code refactoring
- `chore:` - Maintenance tasks

### Testing

```bash
# Run all tests
cargo test

# Run specific test
cargo test test_parse_python

# Run with output
cargo test -- --nocapture

# Run tests with coverage (if tarpaulin installed)
cargo tarpaulin
```

## Submitting Changes

### 1. Push Your Branch

```bash
git push origin feature/my-awesome-feature
```

### 2. Create a Pull Request

- Go to the repository on GitHub
- Click "New Pull Request"
- Select your branch
- Fill in the PR template:
  - Describe what changed
  - Link related issues
  - Add screenshots (if UI changes)
  - Note any breaking changes

### 3. Code Review

- Maintainers will review your PR
- Address any feedback
- Once approved, your PR will be merged!

## Pull Request Guidelines

### Good PRs

- ✅ Focused on a single concern
- ✅ Include tests
- ✅ Update documentation
- ✅ Pass all CI checks
- ✅ Have clear commit messages

### Avoid

- ❌ Mixing multiple unrelated changes
- ❌ Breaking existing functionality
- ❌ Skipping tests
- ❌ Ignoring code style

## Adding Language Support

Want to add support for a new language?

1. Study existing parsers: `src/parser/python.rs`, `src/parser/typescript.rs`
2. Add tree-sitter dependency for your language in `Cargo.toml`
3. Create `src/parser/yourlang.rs`
4. Implement the `Parser` trait
5. Add tests in `tests/fixtures/yourlang/`
6. Update README.md

See [Language Support Guide](https://github.com/neural-garage/bury/blob/main/docs/adding-languages.md) for details.

## Reporting Bugs

Use the [bug report template](https://github.com/neural-garage/bury/issues/new?template=bug_report.md):

- Describe the bug
- Steps to reproduce
- Expected vs actual behavior
- Environment (OS, Rust version, bury version)
- Relevant code samples

## Suggesting Features

Use the [feature request template](https://github.com/neural-garage/bury/issues/new?template=feature_request.md):

- Describe the feature
- Explain the use case
- Provide examples
- Consider implementation approach

## Community Guidelines

- Be respectful and inclusive
- Follow our [Code of Conduct](./CODE_OF_CONDUCT.md)
- Help others in discussions
- Give constructive feedback
- Celebrate contributions

## Recognition

Contributors will be:
- Listed in release notes
- Mentioned in the README (for significant contributions)
- Given credit in commit messages

## Questions?

- 💬 Ask in [Discussions](https://github.com/neural-garage/bury/discussions)
- 📧 Open an issue
- 📖 Check [SUPPORT.md](./SUPPORT.md)

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT OR Apache-2.0).

---

Thank you for contributing to Neural Garage! 🧠🔧
