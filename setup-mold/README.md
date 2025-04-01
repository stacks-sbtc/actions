# Setup Mold Action

Download and install the mold linker as the default linker.

## Documentation

### Inputs

| Input          | Description                  | Required | Default |
| -------------- | ---------------------------- | -------- | ------- |
| `make-default` | Make mold the default linker | false    | `true`  |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Mold
        id: setup_mold
        uses: stacks-sbtc/actions/setup-mold@main
        with:
          make-default: true
```
