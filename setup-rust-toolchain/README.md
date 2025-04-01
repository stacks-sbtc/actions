# Setup Rust Toolchain Action

Installs a Rust toolchain using rustup, with an option of adding extra components

## Documentation

### Inputs

| Input        | Description                                                         | Required | Default |
| ------------ | ------------------------------------------------------------------- | -------- | ------- |
| `components` | Comma-separated list of components to be additionally installed     | false    |         |
| `cache-key`  | Additional cache key that can be used to further differentiate jobs | false    |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Rust Toolchain
        id: setup_rust_toolchain
        uses: stacks-sbtc/actions/setup-rust-toolchain@main
        with:
          components: clippy, rustfmt
          cache-key: "rust-tests"
```
