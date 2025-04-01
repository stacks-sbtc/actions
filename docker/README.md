# Docker Action

Generic Docker Setup

- Runs [cleanup](../cleanup)
- Sets some basic env vars based on workflow trigger (i.e. PR)
- Sets up QEMU, buildx and logs into docker

This folder also contains wrappers over other specific docker actions that the main composite calls:
- [build-push-action](./build-push-action) - Build and push Docker images with Buildx
- [login-action](./login-action) - Logs in to dockerhub if the secrets are set
- [metadata-action](./metadata-action) - Extract metadata from GitHub
- [setup-buildx-action](./setup-buildx-action) - Setup QEMU for multi-arch builds
- [setup-qemu-action](./setup-qemu-action) - Setup docker buildx

## Documentation

### Inputs
| Input      | Description          | Required | Default |
| ---------- | -------------------- | -------- | ------- |
| `username` | Docker repo username | false    | `""`    |
| `password` | Docker repo password | false    | `""`    |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Docker Setup
        id: docker_setup
        uses: stacks-sbtc/actions/docker@main
        with:
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_PASSWORD }}
```
