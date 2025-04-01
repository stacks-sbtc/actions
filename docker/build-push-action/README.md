# Docker Build Push Action

Build and push Docker images with Buildx

## Documentation

### Inputs
| Input        | Description                                      | Required | Default |
| ------------ | ------------------------------------------------ | -------- |---------|
| `build-args` | List of build-time variables                     | false    |         |
| `file`       | Path to the Dockerfile                           | false    |         |
| `labels`     | List of metadata for an image                    | false    |         |
| `platforms`  | List of target platforms for build               | false    |         |
| `push`       | Push is a shorthand for `--output=type=registry` | false    | `false` |
| `tags`       | List of tags                                     | false    |         |
| `target`     | Sets the target stage to build                   | false    |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Build And Push
        id: build_and_push
        uses: stacks-sbtc/actions/docker/build-push-action@main
```
