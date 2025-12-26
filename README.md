# unpublish a specified version package


## Example of usage

```
on:
  release:
    types: [deleted]

jobs:
  example:
    runs-on: ubuntu-latest
    permissions:
      packages: write
    steps:
      - uses: o3co/github-action-unpublish-package@v1
        with:
          package-type: "npm"
          version: ${{github.event.release.tag_name}}
          name: "github-action-example"
          token: ${{secrets.GITHUB_TOKEN}}
```
