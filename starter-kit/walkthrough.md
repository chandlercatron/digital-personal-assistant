# System Walkthrough — Instructions for Claude

When the user asks to understand how this system works, requests a walkthrough, or seems confused about the system's structure, read this file and guide them through the relevant sections conversationally. Do not dump everything at once — ask which aspect they want to explore, or start from the top if they want the full tour.

This file is permanent. It is never deleted or renamed.

---

## How to Conduct a Walkthrough

Open with:
> "Happy to walk you through it. We can go top to bottom, or if there's a specific piece you're curious about, we can jump straight there. What would be most useful?"

If they want the full tour, go through the sections below in order. If they have a specific question, navigate to the relevant section.

---

## Section 1: The Big Idea

**What to explain:**

This system is structured like a small company — but the company exists to manage your life and work, not to produce a product. You are the owner. Your lead assistant (that's this persona) is the CEO. Behind them is a small team of specialists, each responsible for a specific domain.

The reason it's structured this way — rather than just "one AI you talk to" — is that different parts of your life require different expertise and different kinds of thinking. A file manager thinks differently than a research analyst. An executive thinks differently than a specialist. By giving each role a defined identity, the system becomes more consistent, more predictable, and easier to grow.

The whole thing lives in a folder on your computer. That folder is the organization. Every file in it is either a piece of your knowledge base or a configuration that tells the AI how to behave.

---

## Section 2: Your Lead Persona

**What to explain:**

Your lead persona is the character you interact with in every conversation. They have a name, a personality, and a clear sense of their role. Every conversation in this folder starts with them.

Their job is not to do deep work themselves — it's to receive your input, determine the right path, delegate to the right team member, and synthesize the result back to you. They're the chief of staff. They know who handles what.

The lead persona's configuration lives in two places:
- `CLAUDE.md` — the system config that loads at the start of every conversation
- `team/[name].md` — the full persona definition: identity, personality, responsibilities, routing table

**Common questions to address:**
- *"Can I change their personality?"* — Yes. Edit `team/[name].md` and update the personality and communication style sections.
- *"Can I rename them?"* — Yes. Rename the file, update `CLAUDE.md`, and ask [Personnel Director] to update `org-chart.md`.

---

## Section 3: The Support Team

**What to explain:**

Behind the lead persona are two permanent team members who came with the system:

**[Knowledge Manager] — Knowledge & File Manager**
[Knowledge Manager] is the system's librarian. She owns the folder structure, maintains the knowledge base, and processes journal entries. If something needs to be filed, found, or organized — that's [Knowledge Manager]. She also audits the system periodically to make sure nothing is stale, misplaced, or orphaned.

**[Personnel Director] — Personnel Director**
[Personnel Director] manages the team itself. When you want to add a new specialist — say, a health coach, a finance director, or a creative lead — you tell [Personnel Director] what you need and she designs and creates that persona. She also handles renaming or retiring team members.

Both of these personas are accessible through your lead assistant. You don't have to invoke them directly — your lead will loop them in when appropriate.

**Growing the team:**
The team is designed to grow with you. When you find yourself repeatedly asking about the same domain and getting shallow answers, that's usually the signal that you need a specialist. Tell your lead — or ask [Personnel Director] directly — and she'll help you design the right persona.

---

## Section 4: The Folder Structure

**What to explain:**

Each folder is a knowledge domain — a department. The folders that exist in this system are:

| Folder | What lives here |
|--------|-----------------|
| `team/` | Persona files for every team member |
| `personal/` | Personal life: home, health, relationships, goals |
| `work/` | Professional life: projects, clients, career |
| `knowledge/` | Cross-domain notes, ideas, and reference material |
| `journal/` | Dated brain dumps and reflections |
| `inbox/` | Unsorted items — drop anything here, [Knowledge Manager] routes it |
| `outbox/` | Files ready for review before they're filed permanently |

*Plus any optional domains set up during onboarding.*

**The inbox concept:**
The `inbox/` folder is a frictionless capture point. If you have something to save and don't want to think about where it goes, drop it in inbox. [Knowledge Manager] will process it and move it to the right place.

**Context files:**
Each domain folder has a `context.md` file — a running summary of what's relevant in that domain. These are the files your team reads to understand the current state of your life and work. Keep them reasonably up to date for best results.

---

## Section 5: How Memory Works

**What to explain:**

This system has two kinds of memory:

**File-based memory (permanent):**
Everything in the folder persists indefinitely. Context files, journal entries, persona files — these are always there. Your team reads them at the start of relevant conversations.

**Auto-memory (conversation-to-conversation):**
Claude Code maintains a separate memory index that carries important context from session to session — things like current priorities, ongoing projects, preferences, and feedback. This is managed automatically and doesn't require any action from you.

**The journal as memory:**
Journal entries are one of the most powerful memory tools in the system. A dated brain dump — even a few sentences about what's on your mind — gives your team material to work with: patterns to flag, tasks to surface, context to retain. [Knowledge Manager] processes journal entries and routes relevant pieces to the right team members.

To write one, just tell your lead: *"I want to do a journal entry"* and they'll guide you through it.

---

## Section 6: Daily Usage Patterns

**What to explain:**

There's no required workflow. The system adapts to how you use it. But here are the patterns that tend to make it most valuable:

**Morning orientation:**
Start a session with *"What's on today?"* or *"What should I be focused on?"* Your lead will reference your context files, priorities, and any recent journal entries to give you a useful answer.

**Brain dumping:**
When something is taking up mental space — a project, a worry, an idea — just talk it through. Your lead will help you process it, extract action items, and file relevant pieces.

**Project tracking:**
Tell your lead about active projects. They'll help you capture the context in `work/` or `personal/` so it persists across sessions.

**Asking for research:**
*"Can you look into X?"* Your lead will handle it or delegate to the right team member.

**System maintenance:**
Periodically ask [Knowledge Manager] to audit the system — she'll check for stale context, broken references, and opportunities to better organize what's there.

---

## Section 7: Growing the Team

**What to explain:**

The starter team (lead, [Knowledge Manager], [Personnel Director]) is a foundation, not a ceiling. The system is designed to grow as your life and work evolve.

**When to add a specialist:**
When you find yourself asking the same kinds of questions repeatedly and getting answers that feel shallow or generic, that's the signal. Common additions:
- Health & Wellness Coach
- Personal Finance Director
- Creative Director
- Professional development specialist
- Domain-specific work specialists (depends on your field)

**How to add one:**
Tell your lead you want to expand the team, or ask [Personnel Director] directly: *"I want to add a health coach to the team."* [Personnel Director] will ask you a few questions about what you need and create a fully-formed persona file.

**The principle:**
Each new persona should have a clear domain boundary. Overlap between personas creates confusion. [Personnel Director]'s job is to design clean boundaries. Trust her process.

---

## Closing the Walkthrough

After any section or at the end of the full tour, ask:
> "Does that make sense? Any part you want to dig deeper on, or anything about the system you'd want to change?"

Use the answer to either continue the walkthrough or pivot into action.
