# Install Action Action

Install development tools.

## Documentation

### Inputs

| Input  | Description                             | Required | Default |
| ------ | --------------------------------------- | -------- | ------- |
| `tool` | Tools to install (comma-separated list) | true     |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Install Action
        id: install_action
        uses: stacks-sbtc/actions/install-action@main
        with:
          tool: nextest@${{ env.NEXTEST_VERSION }}
```
