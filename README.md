# Stacks sBTC Github Actions

Monorepo of composite actions used in the stacks-sbtc organisation

- [attest-build-provenance](./attest-build-provenance) - Generate signed build provenance attestations for workflow artifacts
- [aws](./aws) - Actions used for AWS configuration/login
- [cache](./cache) - Create and use caches
- [checkout](./checkout) - Clone the repository in the calling runner
- [cleanup](./cleanup) - Removes unused packages/dirs from a runner, freeing around 30GB of space on a runner
- [docker](./docker) - Setup docker on the runner and optionally log in to dockerhub
- [download-artifact](./download-artifact) - Download one or more artifacts from GitHub
- [github-pages](./github-pages) - Configure, upload and deploy GitHub Pages
- [github-script](./github-script) - Execute JavaScript code within the runner
- [install-action](./install-action) - Install development tools
- [setup-buf](./setup-buf) - Install `buf` tool to build, lint and format
- [setup-mold](./setup-mold) - Install mold linker
- [setup-node](./setup-node) - Install Node.js
- [setup-pnpm](./setup-pnpm) - Install pnpm package manager
- [setup-python](./setup-python) - Install Python
- [setup-rust-toolchain](./setup-rust-toolchain) - Install Rust toolchain with additional components
- [upload-artifact](./upload-artifact) - Upload an artifact to the GitHub's workflow
- [wait-other-jobs](./wait-other-jobs) - Wait for all or specific jobs to finish

## Repo Structure

This repo is structured as a typical monorepo, with agnostic [composite actions](https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-composite-action) at the top level. Repository specific [composite actions](https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-composite-action) are added at the top level, for example `./aws/amazon-ecr-login`.

At a minimum, any new composite actions will need the following 2 files:

- `action.yml` - The composite action workflow (ex: [docker/action.yml](./docker/action.yml))
- `README.md` - How to use the composite action (ex: [docker/README.md](./docker/README.md))

There may or may not be additional folders/logic depending upon the complexity of the workflow, the above 2 files are the minimum requirement.
