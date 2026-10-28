# Modulane

**Small tools that speed up everyday development work.**

Modulane is a collection of tools I build for my own workflow and publish for anyone who finds them useful. Each one solves a specific, recurring annoyance, does it with as little setup as possible, and works on Windows, macOS and Linux.

## Tools

| Tool                                                               | What it does                                                                                                                                        | Install                                      |
| ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| [Dev Workspace CLI](https://github.com/modulane/dev-workspace-cli) | Browse the projects in your development folder and run their scripts from one interactive menu, with npm, pnpm, Yarn or Bun detected automatically. | `npm install -g @modulane/dev-workspace-cli` |

More tools are on the way. Watch this organisation or star the repositories to hear about new ones.

## In development

### Nuxt Core

**Build once, reuse everywhere.** Nuxt Core is a reusable foundation for building websites with [Nuxt](https://nuxt.com/). It turns the problems every new site solves again (buttons, forms, navigation, layouts, typography, accessibility, SEO, common sections) into building blocks that are developed and tested once, then combined into new sites.

It comes as [Nuxt layers](https://nuxt.com/docs/guide/going-further/layers) that a site can use together or on their own:

- **Primitives:** accessible, unstyled components to style with your own CSS, Tailwind or anything else.
- **Design:** a design system of tokens and SCSS styles, to use with these components or another library's.
- **Everything:** the primitives styled by the design system.

A site can override any style, component, composable or layout. Nuxt Core is built with Nuxt 4, Vue 3, strict TypeScript and Sass.

The repository is private during early development. It will open to the public, and to contributions, soon.

## Principles

- **Built from real use.** Every tool starts as something I needed in my own work, and I keep using it after it ships.
- **Small and focused.** One job per tool, few dependencies, sensible defaults.
- **Cross-platform.** Tested on Windows, macOS and Linux.
- **Open source.** Released under the MIT License unless a repository says otherwise.

## Getting help

- **Questions and ideas:** open a discussion or issue in the relevant repository.
- **Bugs:** open an issue in the relevant repository.
- **Security vulnerabilities:** never open a public issue. Use _Report a vulnerability_ in the repository's **Security** tab. See the [security policy](https://github.com/modulane/.github/blob/main/SECURITY.md).

## Contributing

Contributions are welcome. Each repository has its own `CONTRIBUTING.md` with setup and workflow details. Nuxt Core will accept contributions once its repository is public.
