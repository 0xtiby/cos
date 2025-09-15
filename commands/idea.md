---
description: Create or update idea entries
---

# Idea Entry Manager

This command helps you create or update idea entries. Each entry is stored as a markdown file in ./ideas.

## Usage:

- `/idea some thoughts` - Add content to a new idea entry. Genereate the title of file base on the content
- `/idea test-app.md some thoughts` - Create/update entry for a filename. If the entry exist append the content with the date-time of the day.

## Content

Always add frontmatter fields name, created-at, updated-at.

**Don't think** you just need to append the content.

## Output Format

Output the filename only.

### Exemple of content

command: /idea some thoughts about my awesome app idea...

```
---
name: my awesome app idea
created-at: 2025-10-01-12:00-00
updated-at: 2025-10-01-12:00-00
---
# My Awesome App Idea

some thoughts about my awesome app idea...
```

command: /idea add some new thoughts about my awesome app idea... to my-awesome-app-idea.md

```
---
name: my awesome app idea
created-at: 2025-10-01-12:00-00
updated-at: 2025-10-01-12:00-00
---
# My Awesome App Idea

some thoughts about my awesome app idea...

2025-10-05 12:00:00
new thoughts about my awesome app idea...
```