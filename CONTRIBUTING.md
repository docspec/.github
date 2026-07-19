# Contributing to DocSpec

DocSpec is a streaming document-conversion library built in Rust. Documents flow as typed events, one at a time, in constant memory. Contributions that keep that discipline intact are welcome.

## Ways to Contribute

- **Report bugs** — found something broken? Open an issue
- **Suggest features** — have an idea? Start a discussion
- **Improve documentation** — clearer docs help everyone
- **Submit code** — fix bugs or implement features
- **Review PRs** — a second pair of eyes matters

## Getting Started

1. **Fork** the repository
2. **Clone** your fork locally
3. **Create a branch** for your changes (`git checkout -b feat/my-thing`)
4. **Make your changes** following the guidelines below
5. **Test** your changes
6. **Submit a pull request**

## Development Guidelines

### Toolchain

DocSpec is a Cargo workspace. Before committing:

- Run `cargo fmt` — all `.rs` files must be formatted
- Run `cargo clippy` — zero warnings, no `#[allow]` patches in source code
- Run `cargo test` — all tests must pass

Source code holds the strict line. Test files (`tests/` and `#[cfg(test)]` modules) may suppress specific clippy lints at crate level when the lint doesn't apply to test code, but source code is never patched around.

### Code Style

- No `unwrap()` or `expect()` in source code — use `Result` and `?`
- No `unsafe` — the workspace forbids it entirely
- Never buffer a full document — stream always, event by event
- All public items need doc comments
- Keep functions focused; add comments where the logic isn't obvious

### Commits

DocSpec uses [Conventional Commits](https://www.conventionalcommits.org/). Format:

```
type(scope): description

[optional body]

[optional footer(s)]
```

Common types:

- `feat` — new feature
- `fix` — bug fix
- `docs` — documentation changes
- `refactor` — restructuring without behavior change
- `test` — adding or updating tests
- `chore` — maintenance tasks

Examples:

- `feat(docx-reader): support nested lists`
- `fix(html-writer): correct attribute escaping for empty values`
- `docs: clarify EventSink contract in docspec-core`

Reference issues where applicable: `fix(pipe): handle source error mid-stream (#123)`

Changelogs are generated automatically from conventional commits by release-plz. Don't edit `CHANGELOG.md` by hand.

### Pull Requests

- Fill out the PR template completely
- Keep PRs focused on a single change
- Update documentation if the public API or behavior changes
- Ensure all tests pass and coverage holds
- Be responsive to review feedback

## Event Model and Specification Changes

Changes to the DocSpec event model — the `Event` type and its well-formedness rules — need extra care. The event stream is the contract every reader and writer speaks. Breaking it breaks everything downstream.

1. **Discuss first** — open an issue before writing code
2. **Backward compatibility** — consider impact on existing documents and crates
3. **Update the spec** — reflect changes in `docspec-core`'s event documentation and on [docs.rs](https://docs.rs/docspec-core)
4. **Document the change** — update `ARCHITECTURE.md` and any affected crate READMEs

## Reporting Bugs

Include:

- Version (`cargo pkgid docspec` or commit hash)
- Steps to reproduce
- Expected vs. actual behavior
- A minimal sample document, if applicable
- Error output or logs

## Suggesting Features

Describe:

- The problem you're solving
- Your proposed solution
- Alternatives you've considered
- Examples or mockups, if helpful

## Questions?

- Open a [discussion](https://github.com/orgs/docspec/discussions)
- Check existing issues for similar questions

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT).
