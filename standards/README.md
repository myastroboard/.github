# Organization standards

The single source of the rules and shared configuration of every MyAstroBoard repository.

| File | Synced to | Repositories |
|---|---|---|
| [ORG_STANDARDS.md](ORG_STANDARDS.md) | `.github/instructions/org-standards.instructions.md` | all |
| [ruff.base.toml](ruff.base.toml) | `.github/org/ruff.base.toml` | Python repositories |

## How a change reaches the repositories

1. Edit the file here and merge to `main`.
2. [sync-standards](../.github/workflows/sync-standards.yml) opens (or updates) a pull request
   `chore: sync organization standards` in each repository, on the branch
   `chore/org-standards-sync`. It can also be run by hand from the Actions tab.
3. Review and merge each pull request. Until then, that repository keeps the previous version.

## How a repository uses them

- Its `CLAUDE.md` (or `AGENTS.md`) imports the rules on a line of its own:
  `@.github/instructions/org-standards.instructions.md`. GitHub Copilot reads the same file
  directly from `.github/instructions/`.
- Its `ruff.toml` (or `[tool.ruff]` in `pyproject.toml`) extends the baseline:
  `extend = ".github/org/ruff.base.toml"`, then adds rules with `extend-select`. Using `select`
  instead would replace the baseline rules, not add to them.

## Adding a repository

Add it to the `matrix` of [sync-standards.yml](../.github/workflows/sync-standards.yml), give the
sync token access to it, and add it to the family table in ORG_STANDARDS.md.

## The ORG_SYNC_TOKEN secret

The sync writes to other repositories, which the workflow's own `GITHUB_TOKEN` cannot do. It uses
a fine-grained personal access token stored as the `ORG_SYNC_TOKEN` Actions secret of this
repository:

- **Resource owner**: `myastroboard`
- **Repository access**: only the repositories listed in the workflow matrix
- **Permissions**: Contents: read and write, Pull requests: read and write (Metadata: read is
  added automatically)
- **Expiration**: the token expires; renew it before then, or the sync fails with a 401.

If the organization requires approval for fine-grained tokens, approve it under
Organization settings > Personal access tokens > Pending requests.
