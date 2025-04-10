# Configure Pages Action

Enable Pages and extract various metadata about a site

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
