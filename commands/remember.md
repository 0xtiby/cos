---
description: Add something claude needs to remember to the memories
---

# Memory Entry Manager

This command helps you to quickly add memory entry to the memories. Each memory is stored as a markdown file in ./memories.

## Usage:

- `/remember something important` - Add content to a new memory entry. Genereate the title of file base on the content.

## Content

Always add frontmatter fields name, created-at, updated-at.

**Don't think** you just need to append the content.

## Output Format

Output the filename only.

### Exemple of content

command: /remember when I ask for a script it should always be in javascript. Except if I specify another language.

```
---
name: only create scripts in javascript
created-at: 2025-10-01-12:00-00
updated-at: 2025-10-01-12:00-00
---
# Only create scripts in javascript

when I ask for a script it should always be in javascript. Except if I specify another language.
```