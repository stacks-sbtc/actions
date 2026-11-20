# Docker Setup QEMU Action

Setup QEMU for multi-arch builds

Registers the QEMU emulators by running the [tonistiigi/binfmt](https://github.com/tonistiigi/binfmt) image directly, the same thing `docker/setup-qemu-action` does. It does not call that action, which is not on the organization's list of allowed actions.

## Documentation

### Inputs

| Input       | Description                            | Required | Default                                       |
| ----------- | -------------------------------------- | -------- | --------------------------------------------- |
| `image`     | QEMU static binaries Docker image      | false    | `tonistiigi/binfmt:qemu-v10.2.3` (by digest)  |
| `platforms` | Platforms to install (comma separated) | false    | `all`                                         |

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
