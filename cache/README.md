# Cache Action

Create and use caches for dependencies and other commonly reused files.

## Documentation

### Inputs

| Input  | Description                                                              | Required | Default |
| ------ | ------------------------------------------------------------------------ | -------- | ------- |
| `path` | A list of files, directories, and wildcard patterns to cache and restore | true     |         |
| `key`  | An explicit key for restoring and saving the cache                       | true     |         |

### Outputs

| Output      | Description                                                              |
| ----------- |------------------------------------------------------------------------- |
| `cache_hit` | A boolean value to indicate an exact match was found for the primary key |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Cache
        id: cache
        uses: stacks-sbtc/actions/cache@main
        with:
          path: ${{ runner.tool_cache }}/cargo-vet
          key: cargo-vet-bin-${{ env.CARGO_VET_VERSION }}
```
