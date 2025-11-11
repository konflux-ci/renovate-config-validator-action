# Renovate-config-validator-action

GitHub Actions for renovate-config-validator, to validate Mintmaker custom configs.

# Example Workflow

```yaml
steps:
    - name: Validate renovate config
      uses: konflux-ci/renovate-config-validator-action@main
      with: 
        config_file: renovate.json