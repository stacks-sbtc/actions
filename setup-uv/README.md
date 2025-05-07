# Setup Uv Action

Set up GitHub Actions workflow with a specific version of `uv`.

## Documentation

### Inputs

| Input        | Description                  | Required | Default |
| ------------ | ---------------------------- | -------- | ------- |
| `version`    | The version of uv to install | false    |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Uv
        id: setup_uv
        uses: stacks-sbtc/actions/setup-uv@main
        with:
          version: "0.6.5"
```
