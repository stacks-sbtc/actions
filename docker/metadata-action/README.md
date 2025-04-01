# Docker Metadata Action

Extract metadata from GitHub

## Documentation

### Inputs
| Input    | Description                                        | Required | Default |
| -------- | -------------------------------------------------- | -------- | ------- |
| `images` | List of Docker images to use as base name for tags | false    |         |
| `tags`   | List of tags as key-value pair attributes          | false    |         |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Docker Metadata
        id: docker_metadata
        uses: stacks-sbtc/actions/docker/metadata-action@main
        with:
          images: ${{ env.docker-org }}/sbtc
          tags: |
            type=raw,value=${{ matrix.docker_target }}-${{ github.ref_name }}-${{ matrix.dist }}
            type=raw,value=${{ matrix.docker_target }}-${{ github.ref_name }},enable=${{ matrix.dist == 'debian' }}
```
