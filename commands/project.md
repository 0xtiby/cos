---
description: Manage project
---

# Project Entry Manager

This command helps you to start a new project. Each project is stored as a folder in ./projects.

## Usage:

- `/project new project name - content` - Initialize a new project with the given name. Create a folder in ./projects and add an `About.md` file with the project name and creation date. Try to find matching ideas in ./ideas and link it in `About.md`.
- `/project add filename - content` - Add a new markdown file to the current project with the given filename and content. If the filename already exists, append the content to the existing file instead of creating a new one.

## Content

Always add frontmatter fields name, created-at, updated-at.
For the About.md file add this frontmatter when possible: idea-link (link to related idea in ./ideas), repos-link (link to related repo in ./repos if any).

**Don't think** you just need to append the content.

## Output Format

Output the filename only.

### Exemple of content

`/project awesome application - this applcation is designed to solve problems.`

file `About.md`

```markdown
---
name: Awesome Application
created-at: 2024-06-10
updated-at: 2024-06-10
idea-link: ../ideas/awesome-application-idea.md
repos-link: ../repos/awesome-application-repo
---

# Awesome Application

This application is designed to solve problems.
```

`/project add requirements - The application should have a user-friendly interface and support multiple languages.`
file `requirements.md`

```markdown
---
name: requirements
created-at: 2024-06-10
updated-at: 2024-06-10
---

# Requirements

The application should have a user-friendly interface and support multiple languages.
```