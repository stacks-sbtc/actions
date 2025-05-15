# Github Script Action

Execute a snippet of JavaScript in the GitHub runner

## Documentation

### Inputs

| Input    | Description       | Required | Default |
| -------- | ----------------- | -------- | ------- |
| `script` | The script to run | true     |         |

### Outputs

| Output   | Description                                                       |
| -------- | ----------------------------------------------------------------- |
| `result` | The return value of the script, stringified with `JSON.stringify` |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Github Script
        id: github_script
        uses: stacks-sbtc/actions/github-script@main
        with:
          script: |
            console.log("Hello world!");
```
