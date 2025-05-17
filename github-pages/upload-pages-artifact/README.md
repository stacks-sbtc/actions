# Upload Pages Artifact Action

Package and upload an artifact that can be deployed to GitHub Pages

## Documentation

### Inputs

| Input  | Description                                        | Required | Default |
| ------ | -------------------------------------------------- | -------- | ------- |
| `path` | Path of the directory containing the static assets | true     |         |

### Outputs

| Output        | Description                               |
| ------------- | ----------------------------------------- |
| `artifact_id` | The ID of the artifact that was uploaded. |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Upload Pages Artifact
        id: upload_pages_artifact
        uses: stacks-sbtc/actions/github-pages/upload-pages-artifact@main
        with:
          path: "./target/doc/"
```
