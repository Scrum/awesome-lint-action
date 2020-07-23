# <img valign="text-bottom" height="49" src="https://raw.githubusercontent.com/sdras/awesome-actions/master/awesome-actions.png" align="right"> Awesome readme lint
> A GitHub Action that lint awesome readme in PR 


## Usage

You can create a `.github/workflows/awesome-lint.yml` file:

```yaml
name: Awesome readme lint
on:
  pull_request:
    types: [opened, synchronize]
    branches:
      - master
jobs:
  build:
    name: awesome readme lint
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: Scrum/awesome-lint-action@v0.1.0
        with:
          entry: 'path/to/file'
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
## Related
- [awesome-lint](https://github.com/sindresorhus/awesome-lint) - Linter for Awesome lists.