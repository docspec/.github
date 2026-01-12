# Contributing to DocSpec

Thank you for your interest in contributing to DocSpec! This document provides guidelines for contributing to any repository in the DocSpec organization.

## Ways to Contribute

- **Report bugs** - Found something broken? Open an issue
- **Suggest features** - Have an idea? We'd love to hear it
- **Improve documentation** - Help make docs clearer
- **Submit code** - Fix bugs or implement features
- **Test and review** - Help test changes and review PRs

## Getting Started

1. **Fork** the repository you want to contribute to
2. **Clone** your fork locally
3. **Create a branch** for your changes
4. **Make your changes** following the guidelines below
5. **Test** your changes
6. **Submit a pull request**

## Development Guidelines

### Code Style

- Follow the existing code style in the repository
- Use meaningful variable and function names
- Keep functions focused and concise
- Add comments for complex logic

### Elixir Projects

- Run `mix format` before committing
- Ensure `mix test` passes
- Ensure `mix credo` passes with no warnings
- Ensure `mix dialyzer` passes with no warnings
- Use typespecs for public functions

### Commits

We use [Conventional Commits](https://www.conventionalcommits.org/). Format your commit messages as:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

Common types:

- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation changes
- `style` - Formatting, missing semicolons, etc.
- `refactor` - Code restructuring without behavior change
- `test` - Adding or updating tests
- `chore` - Maintenance tasks

Examples:

- `feat(parser): add support for inline code blocks`
- `fix(ast): correct handling of nested lists`
- `docs: update installation instructions`

Reference issues when applicable (e.g., `fix(renderer): resolve crash on empty input (#123)`)

### Pull Requests

- Fill out the PR template completely
- Keep PRs focused on a single change
- Update documentation if needed
- Ensure all tests pass
- Be responsive to review feedback

## AST and Specification Changes

Changes to the DocSpec AST specification require extra consideration:

1. **Discuss first** - Open an issue to discuss the change
2. **Backward compatibility** - Consider impact on existing documents
3. **Update TypeSpec** - Reflect changes in the [specification schema](https://github.com/docspec/docspec)
4. **Document the change** - Update specification documentation

## Reporting Bugs

When reporting bugs, include:

- Version you're using
- Steps to reproduce
- Expected vs actual behavior
- Sample document (if applicable)
- Error messages or logs

## Suggesting Features

When suggesting features:

- Describe the problem you're solving
- Explain your proposed solution
- Consider alternatives you've thought about
- Provide examples or mockups if helpful

## Questions?

- Open a [discussion](https://github.com/orgs/docspec/discussions)
- Review existing issues for similar questions

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (typically EUPL-1.2).
