---
name: brain-tasks
description: >-
  Scans conversation history and modified files for action items, TODO/FIXME comments,
  unresolved edge cases, and verbal commitments, cross-checks them against existing Second Brain tasks,
  and presents an organized task list with 1-click save options.
---

# Brain Tasks — Action Item & TODO Miner (`/brain-tasks`)

Use this skill to extract all pending work items, follow-ups, and open questions from your current conversation and codebase without letting tasks slip through the cracks.

---

## What Happens When Invoked

When `/brain-tasks` is triggered, execute these steps:

### Step 1: Extract Potential Tasks
1. Search workspace files for `TODO`, `FIXME`, `HACK`, `BUG`, `NOTE`, or `PENDING` comments in recently modified files.
2. Review conversation history for:
   - Verbal commitments ("let's fix this tomorrow", "we should also support X", "need to test on Windows 11")
   - Unresolved errors or edge cases noted during testing
   - Deferred refactors or cleanup requests

### Step 2: Cross-Check with Existing Second Brain Tasks
1. Call `recall` on `second-brain` with: `"User tasks, action items, and pending follow-ups for [project]" --tag task`.
2. Deduplicate: Identify which tasks are already logged vs which are newly discovered.

### Step 3: Present Prioritized Task Dashboard
Output a clean, prioritized markdown checklist:
- 🔴 **High Priority / Blocking**: Immediate next bugs or blockers
- 🟡 **Medium Priority / Features**: Enhancements, refactors, secondary tests
- 🟢 **Already Tracked in Brain**: Existing `#task` memories (with IDs)

### Step 4: Ready-to-Save Action Items
Provide pre-formatted commands to record the new tasks in the Second Brain:
```
/brain-save Fix UDP socket leak on rapid client disconnect #live-actions #task !state
```
If the user says "save all" or confirms specific items, execute the saves immediately.

---

## Syntax

```
/brain-tasks [optional project name]
```

## Examples

```
/brain-tasks
/brain-tasks Live Actions
```
