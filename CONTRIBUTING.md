# Contributing to Modulane

Thank you for helping improve a Modulane project. This guide covers the conventions shared by every repository in the organisation.

A repository can have its own `CONTRIBUTING.md` with setup instructions, commands and code layout. When it does, GitHub shows that guide instead of this one, and its rules take precedence where they differ.

## Before you start

- **Bugs:** search the existing issues first, then open one with the bug report form.
- **New features:** open an issue with the feature request form before writing a large change. Each project has a narrow purpose, and agreeing on the problem first saves you from writing code that cannot be merged.
- **Small fixes** such as typos or obvious bugs can go straight to a pull request.

By participating, you agree to follow the [code of conduct](CODE_OF_CONDUCT.md).

## Workflow

Every change reaches `main` through a pull request:

1. Fork the repository and create a branch named after the change, such as `feat/project-search`, `fix/ctrl-c` or `docs/readme`.
2. Make the change, with tests where practical. Bug fixes should include a test that fails without the fix.
3. Run the repository's checks locally. Its README or `CONTRIBUTING.md` names the command, usually `npm run check`.
4. Open a pull request that explains what changed, and why if that is not obvious, and fill in its [AI use](#ai-use) section.
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

## AI use

AI tools are allowed, but their use is never hidden. The rule is the same for the maintainer and for contributors.

- **Pull requests:** fill in the **AI use** section of the pull request template. Tick **No AI tool was used**, or tick **AI tools were used** and name each tool and what it did under it, for example "Claude Code wrote the first draft of the tests; I reviewed and changed them". The **AI disclosure** check fails until exactly one box is ticked, and a pull request cannot be merged without it. Editing the description runs the check again. Dependabot pull requests are exempt.
- **Issues:** every issue form asks the same question.
- **Comments and reviews:** say so when an AI tool wrote or drafted what you post. No check can verify this, so it relies on you.

You are responsible for everything you submit, whoever or whatever wrote it: read it, test it, and be ready to explain it.

## What makes a good change

- **It fits the project's purpose.** Modulane projects stay focused. A feature that only serves one unusual setup may be better as a configuration option, or outside the project.
- **It works everywhere.** Tools support Windows, macOS and Linux, so avoid shell-specific commands and hard-coded path separators. Website building blocks support every screen size, keyboard use and assistive technology.
- **It adds few dependencies.** Add a dependency only when it solves a real problem that the platform or the existing dependencies cannot.
- **It keeps the documentation current.** Update the README and any other affected documentation in the same pull request.

## Security issues

Do not report vulnerabilities in issues or pull requests. Follow the [security policy](SECURITY.md) instead.

## License

By contributing, you agree that your contribution is licensed under the license of the repository you contribute to.
