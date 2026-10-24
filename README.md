# Brain Tasks

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Deduplicated TODO and Verbal Commitment Extractor — Scans conversation history and touched files for action items, TODO comments, and verbal commitments, cross-checking them against existing memories.

---

## Overview

`brain-tasks` provides standardized capabilities across conversational AI platforms:
- Comprehensive action item extraction from dialogue and code comments.
- Cross-referencing against existing Second Brain task records for deduplication.
- Structured task list with priorities, owners, and 1-click save options.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\brain-tasks`
- **Claude**: `C:\Users\<you>\.claude\skills\brain-tasks` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\brain-tasks` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\brain-tasks` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
