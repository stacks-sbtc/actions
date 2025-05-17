# Docker Setup QEMU Action

Setup QEMU for multi-arch builds

## Documentation

### Outputs

| Output      | Description                           |
| ----------- | ------------------------------------- |
| `platforms` | Available platforms (comma separated) |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup QEMU
        id: setup_qemu
        uses: stacks-sbtc/actions/docker/setup-qemu-action@main
```
