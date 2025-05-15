# Attest Build Provenance Action

Generate signed build provenance attestations for workflow artifacts

## Documentation

### Inputs

| Input              | Description                                                    | Required | Default |
| ------------------ | -------------------------------------------------------------- | -------- | ------- |
| `subject-name`     | Subject name as it should appear in the attestation            | true     |         |
| `subject-digest`   | Digest of the subject for which provenance will be generated   | true     |         |

### Outputs

| Output            | Description                                             |
| ----------------- | ------------------------------------------------------- |
| `bundle-path`     | The path to the file containing the attestation bundle. |
| `attestation-id`  | The ID of the attestation.                              |
| `attestation-url` | The URL for the attestation summary.                    |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Generate Artifact Attestation
        id: generate_artifact_attestation
        uses: stacks-sbtc/actions/attest-build-provenance@main
        with:
          subject-name: index.docker.io/${{ env.docker-org }}/sbtc
          subject-digest: ${{ steps.docker_build.outputs.digest }}
```
