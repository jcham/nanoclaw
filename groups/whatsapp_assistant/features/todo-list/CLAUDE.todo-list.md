> This file is tracked in git. Do not store private or personal information here.

# Todo List

You manage todo lists stored in a private GitHub repo: `https://github.com/jcham/jaime-todo-1.git`

The local clone lives at `/workspace/group/features/todo-list/repo/`.

## Git Setup

Before any git operation, authenticate using the token file:

```bash
TOKEN=$(cat /workspace/group/features/todo-list/.github-token)
git config --global url."https://${TOKEN}@github.com/".insteadOf "https://github.com/"
git config --global user.email "nanoclaw@local"
git config --global user.name "Chloe"
```

If the repo isn't cloned yet:
```bash
git clone https://github.com/jcham/jaime-todo-1.git /workspace/group/features/todo-list/repo
```

Otherwise, always `git pull` before making changes.

After every change: `git add -A && git commit -m "<short description>" && git push`.

## File Structure

The repo has one `.md` file per context (e.g. `jaime-personal.md`, `jaime-work.md`).

## Document Structure

- `#` headings = top-level group/category
- The highest-level items under a category (whether `##`, `###`, or plain bullets) = **TODO items**
- Further indents under a TODO = details, sub-steps, notes, links, attachments

**Standardize all category headings to `##`** when editing a file — normalize any `#` or `###` category headings to `##`.

## Item States

- Active item: normal bullet `- item`
- Completed item: strikethrough `- ~~item~~`

**Cleanup rule**: Use `git log` to find when an item was first struck through. If it has been struck through for **more than 1 month**, delete it entirely (including its sub-items). Otherwise leave it in place.

## Older Files

Older entries may not follow the above structure but may still contain useful information. Preserve their content — only normalize headings and clean up stale struck-through items.

## When Responding to the User

- When asked to add a todo, identify the right file and section, append it as a new bullet
- When asked to complete something, strike it through: `~~item~~`
- When asked to remove something, delete it
- When asked "what are my todos?" or similar, list active (non-struck) items grouped by file/section
- When asked to show a specific file or section, show it as-is
- Keep responses concise — summarize changes made, don't dump the whole file
