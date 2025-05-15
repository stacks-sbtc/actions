# Checkout Action

Checkout the parsed repository without persisting credentials.

## Documentation

### Inputs

| Input        | Description                        | Required | Default                    |
| ------------ | ---------------------------------- | -------- | -------------------------- |
| `repository` | The repository to checkout         | false    | `${{ github.repository }}` |
| `ref`        | The branch, tag or SHA to checkout | false    | Default repository branch  |

### Outputs

| Output   | Description                                 |
| -------- | ------------------------------------------- |
| `ref`    | The branch, tag or SHA that was checked out |
| `commit` | The commit SHA that was checked out         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        id: checkout_repository
        uses: stacks-sbtc/actions/checkout@main
        with:
          repository: sbtc
          ref: v1.0.0
```
