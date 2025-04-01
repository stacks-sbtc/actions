# Setup Pnpm Action

Install pnpm package manager

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
