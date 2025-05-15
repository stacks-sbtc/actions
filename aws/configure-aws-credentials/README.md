# Configure AWS Credentials Action

Configure the AWS credentials and region environment variables for use in other GitHub Actions

## Documentation

### Inputs

| Input            | Description                                           | Required | Default |
| ---------------- | ----------------------------------------------------- | -------- | ------- |
| `role-to-assume` | The Amazon Resource Name (ARN) of the role to assume. | true     |         |
| `aws-region`     | AWS Region                                            | true     |         |

### Outputs

| Output                  | Description                                            |
| ----------------------- | ------------------------------------------------------ |
| `aws-account-id`        | The AWS account ID for the provided credentials        |
| `aws-access-key-id`     | The AWS access key ID for the provided credentials     |
| `aws-secret-access-key` | The AWS secret access key for the provided credentials |
| `aws-session-token`     | The AWS session token for the provided credentials     |

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
