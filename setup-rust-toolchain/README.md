# Setup Rust Toolchain Action

Installs a Rust toolchain using rustup, with an option of adding extra components

## Documentation

### Inputs

| Input        | Description                                                         | Required | Default |
| ------------ | ------------------------------------------------------------------- | -------- | ------- |
| `components` | Comma-separated list of components to be additionally installed     | false    |         |
| `cache-key`  | Additional cache key that can be used to further differentiate jobs | false    |         |

### Outputs

| Output           | Description                                                            |
| ---------------- | ---------------------------------------------------------------------- |
| `rustc-version`  | Version as reported by `rustc --version`                               |
| `cargo-version`  | Version as reported by `cargo --version`                               |
| `rustup-version` | Version as reported by `rustup --version`                              |
| `cachekey`       | A short hash of the rustc version, appropriate for use as a cache key. |

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
