# Download Artifact Action

Downloads one or more artifacts from GitHub to the given path.

## Documentation

### Inputs

| Input       | Description                                                              | Required | Default |
| ----------- | ------------------------------------------------------------------------ | -------- | ------- |
| `name`      | Name of the artifact to download. If unset, all artifacts are downloaded | false    |         |
| `path`      | Destination path                                                         | false    |         |

### Outputs

| Output          | Description               |
| --------------- | ------------------------- |
| `download-path` | Path of artifact download |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Download Artifact
        id: download_artifact
        uses: stacks-sbtc/actions/download-artifact@main
        with:
          name: nextest-archives
          path: .
```
