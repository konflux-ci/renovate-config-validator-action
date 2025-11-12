# Renovate-config-validator-action

GitHub Actions for renovate-config-validator, to validate Mintmaker custom configs.

## Input
### `config_file`

required: false

Renovate Configuration file path.
By default, the action fetches all `renovate.json` files in the repo.

## Example Workflow

```yaml
name: "Validate renovate.json config file"

on:
  push:
    branches: 
      - main
   
jobs:
  renovate-config-file-validation:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: ./
        with:
          config_file: test/renovate.json