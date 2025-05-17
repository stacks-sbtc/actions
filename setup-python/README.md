# Setup Python Action

Download and install python

## Documentation

### Inputs

| Input            | Description                                     | Required | Default |
| ---------------- | ----------------------------------------------- | -------- | ------- |
| `python-version` | Version range or exact version of Python to use | false    |         |

### Outputs

| Output           | Description                                                                       |
| ---------------- | --------------------------------------------------------------------------------- |
| `python_version` | The installed Python or PyPy version. Useful when given a version range as input. |
| `cache_hit`      | A boolean value to indicate a cache entry was found                               |
| `python_path`    | The absolute path to the Python or PyPy executable.                               |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Python
        id: setup_python
        uses: stacks-sbtc/actions/setup-python@main
        with:
          python-version: ${{ env.PYTHON_VERSION }}
```
