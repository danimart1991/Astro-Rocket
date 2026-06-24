# VS Code in Astro Rocket

Short guide to work with this repository in VS Code without extra setup.

## Configuration files

In this codebase, VS Code uses these files:

- `.vscode/settings.json`: editor, linting, and formatting settings.
- `.vscode/extensions.json`: recommended project extensions.
- `.vscode/tasks.json`: common tasks (`dev`, `build`, `check`, `lint`, `test`, `validate`).

## Recommended workflow

1. Open the project folder in VS Code.
2. Install the recommended extensions when prompted.
3. Run `pnpm install` once.
4. Start development with `pnpm dev` or the `dev` task.

## Runtime environment

- This project is ready to run in a Dev Container.
- If you work on Windows + WSL, follow the workflow in `docs/dev-environment.md`.

## Practical notes

- If you change files in `.vscode/`, you usually do not need to rebuild the container.
- If you change `.devcontainer/Dockerfile` or `.devcontainer/devcontainer.json`, rebuilding is recommended.
