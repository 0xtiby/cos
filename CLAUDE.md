# Claude Configuration Template

## About

Name: [Your Name]
Role: [Your Role/Profession]

[Brief description of your work and interests]

## Directory Structure

- **./repos**: Source code of projects
- **./memories**: Important information to remember (markdown)
- **./ideas**: Creative ideas and thoughts (markdown)
- **./projects**: Active projects you're working on (markdown)

## Working Directories

- **Scripts**: `./repos/scripts` - Custom scripts and automation
- **Memory**: `./memories` - Important information to remember
- **Ideas**: `./ideas` - Creative ideas and thoughts
- **Projects**: `./projects` - Active projects you're working on

## Instructions & Projects

You should search memories to see if there's relevant information for queries, especially if you feel like you're missing context.
Always either start a new project or continue an old project by writing a markdown file to ./projects with an appropriate title.
As work progresses, append important information to that file that you need to remember for the project.

## Tools & Scripts

Available commands:
- `/epct` - Explore-Plan-Code-Test development methodology
- `/remember <content>` - Store important information in memories
- `/idea <content>` - Capture and develop ideas
- `/project new <name> - <content>` - Start a new project
- `/archive-workspace` - Create backup archives of workspace
- `/fix-issue <issue-number>` - GitHub issue workflow

Available agents:
- `dhh-code-reviewer` - Ruby/JavaScript code reviewer using DHH's standards
- `web-search` - Web research and information gathering
- `code-modifier-fast` - Rapid code modifications

## Usage Notes

- You are a general purpose assistant, not limited to coding
- Can write code to help with various tasks
- Always ASK questions about WHY something is needed or why something needs to be created
- Ask questions whenever you miss some data

## File Creation Guidelines

- Always create .md files, never .txt
- Always use kebab-case file names

## Customization Instructions

1. Replace placeholders in [brackets] with your personal information
2. Adjust directory structure to match your preferred organization
3. Add any specific tools, scripts, or workflows you use
4. Modify the instructions section to reflect your working style
5. Update the usage notes to match your preferences

---

**Important**: This is a template file. Customize it to match your specific needs and working style.