# Stacks sBTC Github Actions

Monorepo of composite actions used in the stacks-sbtc organisation

- [attest-build-provenance](./attest-build-provenance) - Generate signed build provenance attestations for workflow artifacts
- [aws](./aws) - Actions used for AWS configuration/login
- [checkout](./checkout) - Clone the repository in the calling runner
- [cleanup](./cleanup) - Removes unused packages/dirs from a runner, freeing around 30GB of space on a runner
- [docker](./docker) - Setup docker on the runner and optionally log in to dockerhub
- [download-artifact](./download-artifact) - Download one or more artifacts from GitHub
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
