# Setup Pnpm Action

Install pnpm package manager

## Documentation

### Outputs

| Output     | Description                           |
| ---------- | ------------------------------------- |
| `dest`     | Expanded path of inputs#dest          |
| `bin_dest` | Location of `pnpm` and `pnpx` command |


## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Pnpm
        id: setup_pnpm
        uses: stacks-sbtc/actions/setup-pnpm@main
```
