> This file is tracked in git. Do not store private or personal information here.

# Shopping List

You maintain a master shopping list at `/workspace/group/features/shopping-list/shopping-list.md`.

## Two Modes

**The list is a master inventory** — everything the user might ever buy. Items are either:
- Normal: `- item` → in stock / not needed right now
- **Highlighted**: `- **item**` → need to buy (out of stock or running low)

## When to Update

**Mark as needed** (bold the item) when the user says:
- "we're out of X", "no more X", "add X to the list", "need X", "running low on X"
- If the item doesn't exist in the list yet, add it in the right category AND bold it

**Mark as got** (un-bold) when the user says:
- "got X", "bought X", "picked up X", "have X", "remove X from needed"

**Add to list** (not highlighted) when the user says:
- "add X to the master list" or similar — item exists but isn't needed right now

**Remove from list entirely** when the user says:
- "remove X", "delete X", "take X off the list"

## What to Buy

When the user asks "what do I need?", "what should I buy?", "shopping list?":
- Show **only the bolded items**, grouped by category
- Skip categories with no bolded items
- Keep response short

Show the full list only if they ask: "show full list", "everything", etc.

## List Format

Group by category. Use **bold** for items to buy:

```
## Produce
- Lettuce
- **Parsley**
- Broccoli

## Dairy
- **Milk**
- Butter
```

Categories: Produce, Dairy, Meat & Seafood, Bakery, Pantry, Beverages, Household, Cleaning Supplies, Other

## How to Update

1. Read `/workspace/group/features/shopping-list/shopping-list.md`
2. Make changes (add/bold/un-bold/remove)
3. Write the file back
4. Confirm briefly: "Added to needed: milk, eggs" or "Got it, removed from needed: bread"
