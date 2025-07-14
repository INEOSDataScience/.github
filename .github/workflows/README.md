# GitHub Actions Workflows

This directory contains GitHub Actions workflows that apply to all repositories in the organization.

## Workflows

### Auto Draft PR (`auto-draft-pr.yml`)

Automatically converts all pull requests to draft state when they are opened. This ensures that developers must manually mark their PRs as "Ready for review" when they are actually ready for review.

**Triggers:**
- When a PR is opened
- When a PR is reopened
- When a PR is marked as "Ready for review"

**Behavior:**
- Converts non-draft PRs to draft state
- Only runs if the PR is not already in draft state
- Requires `pull-requests: write` permission

**Benefits:**
- Prevents accidental PR reviews on incomplete work
- Encourages developers to be intentional about when their code is ready for review
- Reduces noise in review queues
- Improves code review quality by ensuring PRs are actually ready

## Usage

These workflows are automatically applied to all repositories in the organization. No additional configuration is required.

## Permissions

The workflows use minimal required permissions:
- `pull-requests: write` - Only for the auto-draft PR workflow 