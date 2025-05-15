# Upload Artifact Action

Uploads an artifact of the given path with the given name to GitHub.

## Documentation

### Inputs

| Input       | Description                                                                 | Required | Default    |
| ----------- | --------------------------------------------------------------------------- | -------- | ---------- |
| `name`      | The name of the artifact after upload                                       | false    | `artifact` |
| `path`      | The file or directory to upload                                             | true     |            |
| `overwrite` | If true, an artifact with a matching name will be deleted before the upload | false    | `false`    |

### Outputs

| Output            | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| `artifact-id`     | A unique identifier for the artifact that was just uploaded. |
| `artifact-url`    | A download URL for the artifact that was just uploaded       |
| `artifact-digest` | SHA-256 digest for the artifact that was just uploaded       |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Upload Artifact
        id: upload_artifact
        uses: stacks-sbtc/actions/upload-artifact@main
        with:
          name: report
          path: suggestions.txt
          overwrite: true
```
