# Wait Other Jobs Action

Wait for all or specific jobs, even if they are running in other workflows. If any of those jobs fail, this action will fail as well.

## Documentation

### Inputs

| Input                               | Description                                             | Required | Default              |
| ----------------------------------- | ------------------------------------------------------- | -------- | -------------------- |
| `wait-seconds-before-first-polling` | Wait this seconds before first polling                  | false    | `"10"`               |
| `min-interval-seconds`              | Wait this interval or the multiplied value (and jitter) | false    | `"15"`               |
| `retry-method`                      | How to wait for next polling                            | false    | `"equal_intervals"`  |
| `wait-list`                         | Wait only these jobs                                    | false    | `"[]"`               |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Wait Other Jobs
        id: wait_other_jobs
        uses: stacks-sbtc/actions/wait-other-jobs@main
        with:
          retry-method: 'equal_intervals'
          wait-seconds-before-first-polling: 1
          min-interval-seconds: 5
          wait-list: |
            [
              {
                "workflowFile": "on-push.yaml",
                "jobName": "Build Test Artifacts",
                "optional": false,
                "startupGracePeriod": {
                  "minutes": 5
                }
              }
            ]
```
