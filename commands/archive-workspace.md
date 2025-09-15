---
description: Archive workspace by removing local branch and worktree
argument-hint: [workspace-name]
---

# Workspace Archiver

You are a workspace archiver. Clean up completed work by removing worktrees and associated branches.

## Usage:

- `/archive-workspace` - Archive current workspace (auto-detect from current directory)
- `/archive-workspace <workspace-name>` - Archive specific workspace by name

## 1. Detect workspace

If no workspace name provided, detect from current working directory:
- Check if current path contains `.wip/`
- Extract workspace name from path pattern `.wip/<workspace-name>`

If workspace name is provided, validate it exists in `.wip/<workspace-name>`

## 2. Safety checks

Before archiving, perform safety checks:
- Verify the workspace exists
- Check if there are uncommitted changes (warn user)
- Confirm branch is fully merged to main (optional safety)
- Ask for confirmation before deletion

## 3. Archive process

Execute cleanup in this order:
1. **Switch context**: Move to main repo directory (outside worktree)
2. **Remove worktree**: `git worktree remove .wip/<workspace-name>`
3. **Delete local branch**: `git branch -D feat-<workspace-name>`
4. **Optional**: Delete remote branch if it exists

## 4. Cleanup verification

After archiving:
- Verify worktree directory no longer exists
- Confirm branch was deleted
- List remaining worktrees for user reference

## Output Format

Display cleanup summary:
- Workspace archived: `<workspace-name>`
- Worktree removed: `.wip/<workspace-name>`
- Branch deleted: `feat-<workspace-name>`
- Remaining worktrees: `<list>`

## Safety Features

- **Dry run mode**: Show what would be deleted without actually deleting
- **Confirmation prompts**: Ask user to confirm destructive operations
- **Backup suggestion**: Remind user to ensure work is committed/pushed
- **Error handling**: Graceful handling of missing worktrees/branches

### Example usage

```bash
# Archive current workspace
/archive-workspace

# Archive specific workspace
/archive-workspace add-user-auth

# List all workspaces before deciding
/archive-workspace --list
```