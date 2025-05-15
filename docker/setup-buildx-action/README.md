# Docker Setup Buildx Action

Setup Docker Buildx

## Documentation

| Output      | Description                                                  |
| ----------- | ------------------------------------------------------------ |
| `name`      | Builder name                                                 |
| `driver`    | Builder driver                                               |
| `platforms` | Builder node platforms (preferred or available)              |
| `nodes`     | Builder nodes metadata                                       |

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
