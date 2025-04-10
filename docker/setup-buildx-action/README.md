# Docker Setup Buildx Action

Setup Docker Buildx

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Buildx
        id: setup_buildx
        uses: stacks-sbtc/actions/docker/setup-buildx-action@main
```
