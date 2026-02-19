# agentic-workflow-sandbox

A sandbox repository for testing GitHub Agentic Workflows.

## Setup

### Required Secrets

To run the agentic workflows in this repository, you need to configure the following secret:

- **`COPILOT_GITHUB_TOKEN`**: Required for workflows using the GitHub Copilot CLI engine. This should be a GitHub token with appropriate permissions.

### Setting Up Secrets

1. Go to your repository Settings
2. Navigate to Secrets and variables → Actions
3. Click "New repository secret"
4. Add the secret name and value

## Workflows

### Agentic Workflow Test

The main workflow is defined in `.github/workflows/agentic-workflow-test.md` and compiled to `.github/workflows/agentic-workflow-test.lock.yml`.

**Engine**: GitHub Copilot CLI

**Purpose**: Tests the agentic workflow functionality by investigating the project structure and creating an issue with a summary.

## Troubleshooting

### Workflow fails with "secret is not set" error

If you see an error like:
```
Error: Neither CODEX_API_KEY nor OPENAI_API_KEY secret is set
```

This typically means the workflow file is out of sync. The `.lock.yml` file should be recompiled from the `.md` file using `gh aw compile`.

If you see:
```
Error: COPILOT_GITHUB_TOKEN secret is not set
```

You need to configure the `COPILOT_GITHUB_TOKEN` secret in your repository settings.