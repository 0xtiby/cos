# 🧠 COS - Claude Operating System

A shareable workspace configuration system for Claude Code that organizes your development workflow with commands, agents, memories, ideas, and projects.

## Overview

COS provides a structured approach to managing your Claude interactions with:

- **Commands**: Custom slash commands for specific workflows
- **Agents**: Specialized sub-agents for different tasks
- **Output Styles**: Communication style configurations
- **Memories**: Persistent information for Claude to remember
- **Ideas**: Creative thoughts and project concepts
- **Projects**: Structured project management
- **Repos**: Source code repositories and development projects

## Quick Start

### 1. Clone or Download

```bash
git clone [your-repo-url] ~/your-workspace-name
cd ~/your-workspace-name
```

### 2. Customize Configuration

1. Edit `CLAUDE.md` with your personal information and preferences
2. Modify `output-styles/example-style.md` to match your communication style
3. Update directory paths if needed

### 3. Create setup claude

1. Create a `.claude` directory in your personal workspace
2. Move the `agents`, `commands`, `memories`, and `output-styles ` directories into `.claude`
3. Restart Claude Code to load the new configuration

### 4. Start Using COS

Always start claude in this workspace to access COS features.

## Directory Structure

```
cos/
├── README.md                    # This file
├── CLAUDE.md                    # Main configuration (customize this)
├── .gitignore                   # Ignore patterns
├── agents/                      # Specialized sub-agents
│   ├── explore-codebase.md      # Code exploration specialist
│   ├── web-search.md            # Web research specialist
│   └── code-modifier-fast.md    # Fast code modification agent
├── commands/                    # Custom slash commands
│   ├── epct.md                  # Explore-Plan-Code-Test methodology
│   ├── manage-agent.md          # Agent creation and management
│   ├── manage-command.md        # Command creation and management
│   ├── remember.md              # Add entries to memories
│   ├── project.md               # Project management
│   ├── idea.md                  # Idea management
│   └── run-deep-search.md       # Deep research workflow
├── output-styles/               # Communication styles
│   └── example-style.md         # Template communication style
├── memories/                    # Persistent information
│   └── example-memory.md        # Template memory entry
├── ideas/                       # Creative concepts
│   └── example-idea.md          # Template idea entry
├── projects/                    # Active projects
│   └── example-project/         # Template project structure
│       └── About.md
└── repos/                       # Source code repositories (create as needed)
    └── (your actual code projects)
```

## Command Reference

### Core Commands

- `/epct` - Explore-Plan-Code-Test development methodology
- `/remember <content>` - Store important information in memories
- `/idea <content>` - Capture and develop ideas
- `/project new <name> - <content>` - Start a new project
- `/project add <filename> - <content>` - Add files to current project

### Management Commands

- `/manage-agent <action> <name>` - Create/update specialized agents
- `/manage-command <action> <name>` - Create/update custom commands
- `/run-deep-search <topic>` - Comprehensive research workflow

## Agent Reference

### Available Agents

- **explore-codebase**: Code exploration and pattern identification
- **web-search**: Web research and information gathering
- **code-modifier-fast**: Rapid code modifications with minimal overhead

### Using Agents

Agents are automatically available when commands reference them, or you can invoke them directly through the Task tool in conversations.

## File Formats

### Memory Entries (`./memories/`)

```markdown
---
name: memory title
created-at: YYYY-MM-DD-HH:MM:SS
updated-at: YYYY-MM-DD-HH:MM:SS
---

# Memory Title

Content that Claude should remember...
```

### Idea Entries (`./ideas/`)

```markdown
---
name: idea title
created-at: YYYY-MM-DD-HH:MM:SS
updated-at: YYYY-MM-DD-HH:MM:SS
---

# Idea Title

Description and development of the idea...
```

### Project Structure (`./projects/`)

```markdown
---
name: Project Name
created-at: YYYY-MM-DD
updated-at: YYYY-MM-DD
idea-link: ../ideas/related-idea.md
repos-link: ../repos/project-repo
---

# Project Name

Project overview, goals, and progress tracking...
```

## Customization

### Personal Configuration

1. **CLAUDE.md**: Update with your personal information, preferences, and working style
2. **Output Styles**: Modify or create new communication styles in `output-styles/`
3. **Directory Structure**: Adjust paths in commands if you prefer different organization

### Adding Custom Commands

1. Create a new `.md` file in `commands/`
2. Use the command template structure (see `commands/manage-command.md`)
3. Include required frontmatter: `description` and `argument-hint`

### Creating New Agents

1. Create a new `.md` file in `agents/`
2. Include YAML frontmatter with `name`, `description`, `color`, and `tools`
3. Define clear objectives, capabilities, and usage patterns

## Integration with Personal Workspace

COS is designed to be:

1. **Shareable**: Contains no personal information by default
2. **Customizable**: Easy to adapt to your workflow
3. **Separate**: Keeps your personal data in your private workspace

### Recommended Setup

- **Public COS Repository**: Version-controlled, shareable configuration
- **Private Personal Workspace**: Your actual work, memories, ideas, and projects
- **Symlinks or Copies**: Link COS commands/agents to your personal workspace

## Contributing

When contributing to COS:

1. Keep all examples generic and non-personal
2. Use placeholder values like `[Your Name]` in templates
3. Test commands and agents work with relative paths
4. Update documentation for any new features

## Migration from Personal Workspace

If migrating from an existing personal Claude workspace:

1. Back up your personal files
2. Copy COS structure to a new location
3. Customize the configuration files
4. Migrate your personal data separately
5. Update path references as needed

## License

This workspace configuration is provided as-is for personal and educational use. Customize freely for your own needs.
