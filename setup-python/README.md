# Setup Python Action

Download and install python

## Documentation

### Inputs

| Input            | Description                                     | Required | Default |
| ---------------- | ----------------------------------------------- | -------- | ------- |
| `python-version` | Version range or exact version of Python to use | false    |         |

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
