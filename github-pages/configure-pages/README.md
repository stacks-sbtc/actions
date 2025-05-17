# Configure Pages Action

Enable Pages and extract various metadata about a site

## Documentation

### Outputs

| Output      | Description                      |
| ----------- | -------------------------------- |
| `base_url`  | GitHub Pages site full base URL  |
| `origin`    | GitHub Pages site origin         |
| `host`      | GitHub Pages site host           |
| `base_path` | GitHub Pages site full base path |

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Configure Pages
        id: configure_pages
        uses: stacks-sbtc/actions/github-pages/configure-pages@main
```
