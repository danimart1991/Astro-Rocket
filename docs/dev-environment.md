# Development Environment

This project is designed to run inside a Dev Container on WSL with Docker Engine (no Docker Desktop required).

## Architecture at a glance

- Windows: VS Code UI
- WSL (Debian): Docker Engine
- Dev Container: Node 24 + pnpm 11.9.0

The project should live in the WSL filesystem (for example, under /home/...), not under /mnt/c/...

## Prerequisites

1. Install Docker Engine in Debian WSL using official docs:
https://docs.docker.com/engine/install/debian/
2. Complete Linux post-installation so docker works without sudo:
https://docs.docker.com/engine/install/linux-postinstall/
3. Optional but recommended: disable Windows PATH inheritance in WSL to avoid Docker command conflicts.

Example /etc/wsl.conf:

[interop]
appendWindowsPath=false

Then restart WSL from PowerShell:
wsl --shutdown

## First run

1. Open the folder in WSL.
2. Run Dev Containers: Reopen in Container.
3. Wait for postCreateCommand to finish (pnpm install --frozen-lockfile).
4. Start development server:
pnpm dev
5. Open http://localhost:4321 on Windows.

Note: first startup can take a while (dependency install + Vite/Astro warm-up).

## Daily workflow

- Start: pnpm dev
- Stop: Ctrl+C
- Hot reload works on file save.
- No rebuild is needed for normal source/content changes.

## When container rebuild is required

Rebuild only if you change container definition:

- .devcontainer/Dockerfile
- .devcontainer/devcontainer.json

Command: Dev Containers: Rebuild Container

## Why this setup is stable now

- pnpm is pinned in the image (11.9.0) and Corepack prompt is disabled.
- pnpm install uses frozen lockfile in postCreate.
- Build scripts required by dependencies are explicitly approved in pnpm-workspace.yaml.
- Astro dev server is exposed to host access through the container settings.

## Common issues and quick fixes

1. Browser opens localhost:4321 but keeps loading
- Wait a little on first run.
- Check dev logs until you see Astro ready.
- If needed, restart pnpm dev once.

2. Error about ignored build scripts (ERR_PNPM_IGNORED_BUILDS)
- Ensure pnpm-workspace.yaml contains allowBuilds for @parcel/watcher, esbuild, and sharp.

3. Post-create fails after changing devcontainer files
- Run Dev Containers: Rebuild Container.

## Useful commands

- pnpm dev
- pnpm build
- pnpm preview
- pnpm check
- pnpm lint
- pnpm test
- pnpm validate

## Reference files

- .devcontainer/devcontainer.json
- .devcontainer/Dockerfile
- pnpm-workspace.yaml
