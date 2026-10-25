# Contributing to Modulane

Thank you for helping improve a Modulane tool. This guide covers the conventions shared by every repository in the organisation.

A repository can have its own `CONTRIBUTING.md` with setup instructions, commands and code layout. When it does, GitHub shows that guide instead of this one, and its rules take precedence where they differ.

## Before you start

- **Bugs:** search the existing issues first, then open one with the bug report form.
- **New features:** open an issue with the feature request form before writing a large change. Each tool has a narrow purpose, and agreeing on the problem first saves you from writing code that cannot be merged.
- **Small fixes** such as typos or obvious bugs can go straight to a pull request.

By participating, you agree to follow the [code of conduct](CODE_OF_CONDUCT.md).

## Workflow

Every change reaches `main` through a pull request:

1. Fork the repository and create a branch named after the change, such as `feat/project-search`, `fix/ctrl-c` or `docs/readme`.
2. Make the change, with tests where practical. Bug fixes should include a test that fails without the fix.
3. Run the repository's checks locally. Its README or `CONTRIBUTING.md` names the command, usually `npm run check`.
4. Open a pull request that explains what changed, and why if that is not obvious.
5. CI runs on every pull request and must pass before the change is merged.
6. Pull requests are squash-merged, so the pull request title becomes the commit message on `main`.

## Pull request titles

Titles follow [Conventional Commits](https://www.conventionalcommits.org/): a type, a colon and a short lowercase summary in the imperative.

```text
feat: add project search
fix: restore the menu after ctrl+c
docs: explain alias setup
```

| Type                   | Use it for                                |
| ---------------------- | ----------------------------------------- |
| `feat`                 | New functionality                         |
| `fix`                  | Bug fixes                                 |
| `docs`                 | Documentation only                        |
| `refactor`             | Code changes that do not change behaviour |
| `perf`                 | Performance improvements                  |
| `test`                 | Tests only                                |
| `style`                | Formatting only                           |
| `build`, `ci`, `chore` | Tooling, CI and maintenance               |

In repositories with automated releases, the type decides what is published: `fix` makes a patch release, `feat` a minor release, and the other types none. Do not mark a change as breaking (`feat!:` or a `BREAKING CHANGE:` footer) unless the maintainer has agreed to a major release.

## What makes a good change

- **It fits the tool's purpose.** Modulane tools stay small and focused. A feature that only serves one unusual setup may be better as a configuration option, or outside the tool.
- **It works everywhere.** Tools support Windows, macOS and Linux. Avoid shell-specific commands and hard-coded path separators.
- **It adds few dependencies.** Add a dependency only when it solves a real problem that the platform or the existing dependencies cannot.
- **It keeps the documentation current.** Update the README and any other affected documentation in the same pull request.

## Security issues

Do not report vulnerabilities in issues or pull requests. Follow the [security policy](SECURITY.md) instead.

## License

By contributing, you agree that your contribution is licensed under the license of the repository you contribute to.
