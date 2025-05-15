# Setup Node Action

Download and install Node.js

## Documentation

### Inputs

| Input          | Description                                                            | Required | Default |
| -------------- | ---------------------------------------------------------------------- | -------- | ------- |
| `node-version` | Version spec of the version to use                                     | false    |         |
| `cache`        | Used to specify a package manager for caching in the default directory | false    |         |

### Outputs

| Output         | Description                                     |
| -------------- | ----------------------------------------------- |
| `cache-hit`    | A boolean value to indicate if a cache was hit. |
| `node-version` | The installed node version.                     |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Node
        id: setup_node
        uses: stacks-sbtc/actions/setup-node@main
        with:
          node-version: ${{ env.NODE_VERSION }}
          cache: "pnpm"
```
