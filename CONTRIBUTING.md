# Contributing to MyAstroBoard

First off, thank you for taking the time to contribute! 🌙

These guidelines apply across the **MyAstroBoard** organization: the main dashboard, its sister apps, the integrations, the website, and anything we build next. Each repository adds its own `CONTRIBUTING.md` for local setup (dependencies, how to run it, the exact check commands); read it too, it takes precedence on anything project-specific.

The full rule set shared by every repository, for humans and AI assistants alike, is in [standards/ORG_STANDARDS.md](./standards/ORG_STANDARDS.md). This page is the short version.

## Code of Conduct

By participating in any MyAstroBoard project, you agree to uphold our [Code of Conduct](./CODE_OF_CONDUCT.md). We want every space around the project to stay welcoming for astronomers and developers of all skill levels.

## Ways to contribute

You don't need to write code to help:

- **Report bugs** you run into
- **Suggest features** or improvements
- **Improve the documentation**: fix a typo, clarify a step, add an example
- **Help with translations**: keep languages accurate and natural
- **Test under real conditions** and share feedback from the field
- **Help other users** in issues and discussions

## Before you start

- **Search existing issues and discussions** first: your bug or idea may already be tracked.
- For anything non-trivial, **open an issue before writing code**, so we can agree on the approach before you invest time.
- Keep each contribution **focused on a single concern**: it makes review faster and history cleaner.

## Reporting a bug

Open an issue and include, as far as you can:

- What you expected to happen, and what actually happened
- Clear steps to reproduce
- The project and version (release tag or commit)
- Your environment (how it's deployed, browser/OS where relevant)
- Logs, screenshots, or error messages

> ⚠️ Found a **security** issue? Do **not** open a public issue: see our [Security Policy](./SECURITY.md).

## Suggesting a feature

Open an issue describing the problem you're trying to solve, not only the solution you have in mind. Context about your observing setup or workflow helps us design something that works for more people.

## Submitting changes

1. **Fork** the repository and create a branch from `main` named `<type>/<short-description>`, with type one of `feature`, `fix`, `chore`, `docs`, `refactor`, `test`, `ci` (e.g. `fix/timezone-display`, `feature/aurora-alerts`).
2. Make your changes, keeping them **small and focused**, with tests for new behavior.
3. Write commit messages in the [Conventional Commits](https://www.conventionalcommits.org/) format: `<type>: <subject>`, imperative mood, at most 72 characters, with a body explaining the *why* when it isn't obvious. Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `ci`, `chore`.
4. **Add a changelog entry**: a `feature/` or `fix/` branch must add a one- or two-line bullet under `## [Unreleased]` in `CHANGELOG.md` (CI checks it).
5. Run the repository's checks (tests, formatter, linter; see its `CONTRIBUTING.md`).
6. Open a **pull request against `main`**, link the related issue, and describe what you changed and how you tested it.

**Used an AI tool?** That's fine; just say so. Add a `Co-Authored-By:` trailer naming the tool to the commits it helped write, and mention it in the pull request.

## Coding style

- **Match the surrounding code**: follow the conventions already present in the file and project.
- **English** for code, comments, docs and commit messages; user-facing text goes through the project's translation files.
- **ASCII punctuation** in source and translation files: straight `'` and `-`, no curly apostrophes or long dashes.
- Prefer **small, readable changes** over large rewrites; if a big refactor seems needed, open an issue to discuss it first.
- Don't mix unrelated changes (formatting + logic + dependencies) in one pull request.

## Review and merging

A maintainer will review your pull request. Reviews are about the code, never the person: expect questions and suggestions, and feel free to push back with reasoning. Once it's approved and checks pass, a maintainer squash-merges it.

## Recognition

Every contribution counts, from a one-character typo fix to a major feature. Thank you for helping keep MyAstroBoard a friendly project for the astronomy community. 🌌
