# Contributing to Match List Change Detector

Thank you for your interest in contributing to the Match List Change Detector! This document provides guidelines and workflows to ensure a smooth contribution process.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Gitflow Workflow](#gitflow-workflow)
- [Issue Tracking](#issue-tracking)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Testing](#testing)
- [Guidelines for AI Agents](#guidelines-for-ai-agents)

## Code of Conduct

Please be respectful and considerate of others when contributing to this project. We aim to foster an inclusive and welcoming community.

## Gitflow Workflow

This project follows the Gitflow workflow:

### Branch Structure

- `main`: Production-ready code
- `develop`: Integration branch for features
- `feature/*`: New features or enhancements
- `bugfix/*`: Bug fixes
- `hotfix/*`: Urgent fixes for production
- `release/*`: Release preparation

### Workflow Steps

1. **Create a Feature Branch**:
   ```bash
   git checkout develop
   git pull
   git checkout -b feature/your-feature-name
   ```

2. **Make Changes**:
   - Implement your changes
   - Commit frequently with clear messages
   - Push your branch to GitHub

3. **Create a Pull Request**:
   - Create a PR from your feature branch to `develop`
   - Reference any related issues
   - Request reviews

4. **Review and Merge**:
   - Address review feedback
   - Once approved, merge into `develop`
   - Delete the feature branch after merging

5. **Release Process**:
   - Create a `release/x.y.z` branch from `develop`
   - Make final adjustments and version bumps
   - Merge into `main` and tag with version
   - Merge back into `develop`

## Issue Tracking

- Use GitHub Issues for tracking tasks, bugs, and enhancements
- Apply appropriate labels to issues
- Reference issues in commits and PRs using keywords (e.g., "Fixes #123")
- Keep issues updated with progress

### Issue Templates

- **Bug Report**: For reporting bugs
- **Feature Request**: For suggesting enhancements
- **Task**: For general tasks

## Pull Request Process

1. **Create a PR**:
   - Use the PR template
   - Reference related issues
   - Provide a clear description

2. **CI/CD Checks**:
   - Ensure all CI/CD checks pass
   - Fix any failing tests or linting issues

3. **Code Review**:
   - Address all review comments
   - Request re-review after making changes

4. **Merging**:
   - Squash and merge feature branches
   - Use merge commits for release branches
   - Delete branches after merging

## Coding Standards

- Follow PEP 8 for Python code
- Use meaningful variable and function names
- Write docstrings for all functions and classes
- Keep functions small and focused
- Use type hints where appropriate

## Testing

- Write tests for all new features and bug fixes
- Ensure all tests pass before submitting a PR
- Aim for high test coverage
- Run tests locally before pushing:
  ```bash
  ./run_tests.sh
  ```

## Guidelines for AI Agents

AI agents contributing to this project should follow these additional guidelines:

### Issue and Branch Management

- **Always close issues**: When a PR resolves an issue, explicitly mention "Closes #123" in the PR description
- **Clean up branches**: Delete feature branches after merging PRs
- **Link related PRs**: If replacing one PR with another, reference the original PR and explain why
- **Track open work**: Maintain awareness of open issues and PRs you've created

### Communication

- **Be explicit**: Clearly state what changes you're making and why
- **Document decisions**: Explain your reasoning, especially for non-obvious choices
- **Provide context**: Reference relevant documentation or discussions

### GitHub CLI Usage

- **Prefer files for Markdown content**: When using the GitHub CLI with Markdown content, prefer passing content as files rather than streams:
  ```bash
  # Good - Using a file
  gh issue create --title "Issue Title" --body-file description.md
  
  # Avoid - Streaming Markdown
  echo "# Heading\nContent" | gh issue create --title "Issue Title" --body-stdin
  ```

- **Format Markdown carefully**: Ensure proper formatting, especially for code blocks and lists
- **Verify rendered output**: Check how Markdown renders in GitHub's interface

### PR Descriptions

- **Be comprehensive**: Include all relevant details
- **Use structured format**: Follow the PR template
- **Include testing instructions**: Explain how to test the changes
- **List dependencies**: Mention any new dependencies or requirements

### Continuous Improvement

- **Learn from feedback**: Incorporate feedback into future contributions
- **Adapt to project conventions**: Follow established patterns in the codebase
- **Suggest improvements**: Identify opportunities to improve the contribution process

By following these guidelines, both human and AI contributors can work together effectively to improve the Match List Change Detector project.
