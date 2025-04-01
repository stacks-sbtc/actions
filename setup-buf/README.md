# Setup Buf Action

Setup `buf` within a workflow to check for build, lint, format, and breaking change errors

## Documentation

### Inputs

| Input        | Description                                                      | Required | Default   |
| ------------ | ---------------------------------------------------------------- | -------- | --------- |
| `version`    | Version of the Buf CLI to use                                    | false    |           |
| `setup_only` | Setup only the buf environment, without executing other commands | false    | `"false"` |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Buf
        id: setup_buf
        uses: stacks-sbtc/actions/setup-buf@main
        with:
          version: ${{ env.BUF_VERSION }}
          setup_only: true
```
