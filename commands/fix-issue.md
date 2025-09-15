---
description: Fix GitHub issues using the EPCT workflow with dedicated git worktree
argument-hint: <github issue url>
---

# Issue fixer

You are a issue fixer. Fix the given issue using the `ecpt` workflow.

## Usage:

- `/fix-issue <github issue url>` - Sart fixing the issue from the given github issue url

## 1. Fetch issue details

Use the **gh cli** to fetch the issue title and content from the given github issue url.

## 2. Setup git worktree

Create a new git worktree under `.wip/<kebab-case-title>`.
Create a new branch named `feat:<kebab-case-title>` and checkout to it.

## 3. Move to the worktree folder

**BEFORE DOING ANYTHING ELSE, YOU NEED TO CHANGE DIRECTORY TO THE WORKTREE DIRECTORY**.

## 4. Run epct workflow

EXPLORE: Use parallel subagents to analyze codebase, identify existing patterns, verify dependencies

PLAN: Define scope, approach (following patterns), tests, risks. If unclear → ask targeted questions

CODE: Launch specialized subagents for implementation following project conventions, minimal scope, quality first, auto-format

TEST: Parallel testing subagents - quick validation (lint/types) → focused testing → integration check

Principles: Heavy subagent parallelization, fail fast, minimal changes, project standards

Goal: Correctness > Completeness > Speed

## 5 Create the PR

After implementing the changes commit the changes with a descriptive message. Then create a PR with the implementation details. **IMPORTANT**: Include "Fixes #<id>" in the PR description where <id> is the GitHub issue number you're working on.

## Output Format

Output the worktree path and branch name and the PR url.

### Exemple of content

```bash
# Work from GitHub issue
/work https://github.com/myorg/myapp/issues/42
```
