# Configure AWS Credentials Action

Configure the AWS credentials and region environment variables for use in other GitHub Actions

## Documentation

### Inputs

| Input            | Description                                           | Required | Default |
| ---------------- | ----------------------------------------------------- | -------- | ------- |
| `role-to-assume` | The Amazon Resource Name (ARN) of the role to assume. | false    |         |
| `aws-region`     | AWS Region                                            | true     |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Configure AWS Credentials
        id: configure_aws_credentials
        uses: stacks-sbtc/actions/aws/configure-aws-credetials@main
        with:
          role-to-assume: ${{ secrets['AWS_ROLE_ARN'] }}
          aws-region: ${{ vars['AWS_REGION'] }}
```
