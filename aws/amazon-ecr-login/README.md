# Amazon ECR Login Action

Logs in the local Docker client to one or more Amazon ECR Private registries or an Amazon ECR Public registry.

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Amazon ECR Login
        id: amazon_ecr_login
        uses: stacks-sbtc/actions/aws/amazon-ecr-login@main
```
