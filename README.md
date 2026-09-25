# workistratorchild

This repository is a child of [`bnb/workistratorparent`](https://github.com/bnb/workistratorparent). The workflows in `.github/workflows/` that come from the parent are managed centrally with [`cutenode/workistrator`](https://github.com/cutenode/workistrator).

## Changing a managed workflow

Edit the template in the parent's `workflow-templates/` directory, not the copy here. The next sync overwrites any hand edits to a managed file with the parent's version.

Workflows in `.github/workflows/` that don't come from a parent template are never touched by the sync, so you can add repository-specific workflows here as usual.

## Working on `main`

Sync commits land directly on `main`, so run `git pull` before pushing local changes to avoid a rejected push.

Branch protection on `main` that requires pull requests or signed commits blocks the sync, because workistrator commits straight to the branch through the GitHub API.
