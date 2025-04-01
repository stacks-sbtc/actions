# Docker Login Action

Login to dockerhub

## Documentation

### Inputs
| Input      | Description          | Required | Default |
| ---------- | -------------------- | -------- | ------- |
| `username` | Docker repo username | true     |         |
| `password` | Docker repo password | true     |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Docker Login
        id: docker_login
        uses: stacks-sbtc/actions/docker/login-action@main
        with:
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_PASSWORD }}
```
