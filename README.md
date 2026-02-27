# Custom Action Challenge

A GitHub custom action that reports details about the repository where the action is being run.

## Description

This action displays information about:
- **Actor**: The GitHub actor (user) that triggered the action
- **Commit SHA**: The commit hash that triggered the action
- **Event Type**: The type of GitHub event that triggered the action
- **Visibility**: Whether the repository is public or private

## Usage

Add the action to your GitHub workflow:

```yaml
uses: ./
```

## What it Does

The action logs the following information:
- 👤 Actor: The GitHub username
- 🆔 Commit SHA: The commit hash
- ▶️ Event type: The GitHub event type (push, pull_request, etc.)
- 🔎 Visibility: Shows if the repository is PUBLIC or PRIVATE

## Technical Details

- **Runtime**: Docker
- **Base Image**: Ubuntu 22.04
- **Dependencies**: bash, jq

## Original Source

This project is based on the original work by @automate6500:
https://github.com/automate6500/create-a-custom-action

Credit goes to the original author for creating this custom action challenge.

## Structure

- `entrypoint.sh` - The main script that runs inside the Docker container
- `Dockerfile` - Container definition for the action
- `action.yml` - GitHub action metadata file
- `.github/workflows/` - Workflow files for testing the action
