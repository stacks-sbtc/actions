# Setup Uv Action

Set up GitHub Actions workflow with a specific version of `uv`.

## Documentation

### Inputs

| Input          | Description                      | Required | Default   |
| -------------- | -------------------------------- | -------- | --------- |
| `version`      | The version of uv to install     | false    |           |
| `enable-cache` | Enable uploading of the uv cache | false    | `"false"` |

### Outputs

| Output       | Description                                         |
| ------------ | --------------------------------------------------- |
| `uv-version` | The installed uv version. Useful when using latest. |
| `uv-path`    | The path to the installed uv binary.                |
| `uvx-path`   | The path to the installed uvx binary.               |
| `cache-hit`  | A boolean value to indicate a cache entry was found |

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
          enable-cache: true
```
