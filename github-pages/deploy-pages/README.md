# Deploy Pages Action

Deploy action artifacts to GitHub Pages

## Usage

```yaml
name: Action
on: push
jobs:
  job:
    name: Job
    runs-on: ubuntu-latest
    steps:
      - name: Deploy Pages
        id: deploy_pages
        uses: stacks-sbtc/actions/github-pages/deploy-pages@main
```
