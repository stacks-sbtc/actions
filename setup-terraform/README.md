# Setup Terraform Action

Set up Terraform CLI in the GitHub Actions workflow by downloading a specific version of Terraform CLI and adding it to the PATH.

## Documentation

### Inputs

| Input               | Description                              | Required | Default |
| ------------------- | ---------------------------------------- | -------- | ------- |
| `terraform-version` | The version of Terraform CLI to install. | false    |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Setup Terraform
        id: setup_terraform
        uses: stacks-sbtc/actions/setup-terraform@main
        with:
          terraform-version: ${{ env.TERRAFORM_VERSION }}
```
