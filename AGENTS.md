# AGENTS.md

## Project Overview
Renovate configuration validator action is a Github action that you can add to the CI workflow to validate the renovate configurations in your repository.
Stack: Github Action.

## Architecture
Uses Mintmaker-renovate-image as the base image to validate your renovate.json file. 
- **Entry Point**: `action.yaml`
- **Type:** Docker
- **Setup**: Add the action as a step in Github CI workflow

## Agent Directives
- **Formatting**: Exact YAML Indentation, and use exactly 2 spaces to satisfy the strict GitHub Actions YAML parser.
- **Path Variables**: Always rely on $GITHUB_WORKSPACE rather than hardcoding paths or assuming the current working directory.
- **Boolean Values**: Write true or false rather than yes or no to prevent parsing ambiguities.
- **Action Inputs**: Remember that inputs defined in action.yaml are passed to the the script as uppercase environment variables.