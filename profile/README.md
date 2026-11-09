# Modulane

**Open-source projects for the parts of web development you keep redoing.**

Modulane is a set of projects I build for my own web development work and publish for anyone who finds them useful. Each one takes a job I kept redoing by hand, from finding and running project scripts to rebuilding the same website parts, and makes it something I set up once and stop thinking about.

## Projects

| Project                                                            | What it does                                                                                                                                                                              | Install                                         |
| ------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| [Dev Workspace CLI](https://github.com/modulane/dev-workspace-cli) | Browse the projects in your development folder and run their scripts from one interactive menu, with npm, pnpm, Yarn or Bun detected automatically.                                       | `npm install -g @modulane/dev-workspace-cli`    |
| [Nuxt Core](https://github.com/modulane/nuxt-core)                 | Build websites with [Nuxt](https://nuxt.com/) from tested building blocks: accessible unstyled components, a design system, or both, as Nuxt layers that a site extends and can override. | None yet: not on npm until it is usable         |
| [AI Disclosure](https://github.com/modulane/ai-disclosure)         | A GitHub Action that fails a pull request until its description says whether AI tools were used, and how. No token, no checkout, safe on forks.                                           | `uses: modulane/ai-disclosure@v1` in a workflow |

## Configs and templates

These hold the setup that modulane repositories share, so each one stops carrying its own copy. They are built for this organisation first: anyone can use the public ones, but they follow what modulane repositories need.

| Repository                                     | What it holds                                                                                                                                                                                                                             | Install                                                            |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [configs](https://github.com/modulane/configs) | The shared Prettier options and ESLint flat configs for Node.js packages and Nuxt projects, each published on npm on its own.                                                                                                             | `npm install -D @modulane/prettier-config @modulane/eslint-config` |
| repo-template _(private)_                      | The reference GitHub setup every modulane repository starts from and follows: rulesets, CI ending in a single **CI passed** job, pull request title and label checks, AI disclosure, zizmor, Dependabot for actions and semantic-release. | Not published                                                      |

## Planned and in development

Nothing here is on npm yet. These repositories are private until they are usable, and each one moves up to a section above when it is released.

| Project              | What it will do                                                                                                                           | Status         |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| Nuxt Extras          | Small Nuxt modules that work alongside Nuxt Core, each released on its own. The first one, nuxt-ripple, adds a `v-ripple` directive.      | In development |
| create-modulane-nuxt | Start a Nuxt site on Nuxt Core in one command, with linting, CI and releases set up: `npm create @modulane/nuxt`.                         | Planned        |
| terminal-ui          | The mouse-first, keyboard-complete terminal menus from Dev Workspace CLI, as a library, so every modulane CLI looks and behaves the same. | Planned        |
| branch-pruner        | Review stale Git branches in an interactive menu, squash merges included, before anything is deleted locally or on GitHub.                | Planned        |
| repo-check           | Check that a modulane repository still matches the reference setup, as a CLI and as a GitHub Action, and report what has drifted.         | Planned        |
| workflows            | Reusable GitHub Actions workflows that every modulane repository calls, so a change reaches all of them at once.                          | Planned        |

Watch this organisation or star the repositories to hear when one is released.

## Principles

- **Built from real use.** Every project starts as something I needed in my own work, and I keep using it after it ships.
- **Focused.** One job per project, few dependencies, sensible defaults.
- **Works everywhere.** Tools run on Windows, macOS and Linux. Website building blocks work on every screen size, with a keyboard and with assistive technology.
- **Open source.** Released under the MIT License unless a repository says otherwise.

## Getting help

- **Questions and ideas:** open a discussion or issue in the relevant repository.
- **Bugs:** open an issue in the relevant repository.
- **Security vulnerabilities:** never open a public issue. Use _Report a vulnerability_ in the repository's **Security** tab. See the [security policy](https://github.com/modulane/.github/blob/main/SECURITY.md).

## Contributing

Contributions are welcome. Each repository has its own `CONTRIBUTING.md` with setup and workflow details. Issues labelled `good first issue` or `help wanted` are ready to pick up.
