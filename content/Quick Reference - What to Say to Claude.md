# Quick Reference — What to Say to Claude when it is all set up
*The actual prompts for every part of the workflow.* Adjust to your specifics. 

---

## Claude Chat (Daily Workflow)

### INBOX
- "Dump this in my inbox" + paste whatever
- "Add this to my inbox under Ideas & Fragments" + paste
- "Add this to my inbox under Tasks" + paste
- "Add this to Today's Chaos" + paste

### Weekly Processing
- "Let's process my inbox"
- "Go through my inbox and help me decide what each item is"
- "What's in my inbox that needs attention?"

### Active Work
- "Open [filename] and keep going from here"
- "What's missing from this argument?"
- "Read this draft and ...."
- "Continue this in ..."

### Moving Things Around
- "This is ready to move from ACTIVE to PROJECTS — it's going to [journal/conference/destination]"
- "Move this to ARCHIVE, it's done"
- "This belongs in REFERENCE, I'll come back to it"

### General
- "Read my [filename] and tell me what you see"
- "What's in my ACTIVE folder right now?"
- "What have I been working on lately?" (reads changelog + active)

---

## Claude Code (Wiki Workflow)

### Starting a Session
If Claude Code has a CLAUDE.md at the vault root, it reads that first and follows its session start protocol (which reads all context files). If starting fresh or Claude seems disoriented, say:
- "Read CLAUDE.md and all files in 008-SANCTUM-CONTEXT/ before doing anything."

If continuing a multi-pass ingest from a previous session:
- "We finished the structural mapping pass on [source] last session. Do concept extraction now."
- "We're on the second pass of [source] — concept extraction. Pick up from there."

### Ingest
- "Ingest [filename]"
- "Ingest [filename] — structural mapping pass only, discuss before writing"
- "Ingest [filename] — concept extraction pass"
- "Ingest [filename] — connections pass"
- "Ingest [filename] from [Dropbox path]"

### When Sources Conflict

Claude is instructed to flag contradictions, not silently resolve them. When a new source contradicts an existing wiki page, Claude should surface both positions and let you decide. Some contradictions are errors to correct. Some are epistemologically productive tensions to preserve. You adjudicate.

- "Flag this as a contradiction — keep both positions on the page"
- "Source B is right — update the concept page"
- "This tension is productive — create a connections page for it"
- "These aren't actually contradicting — [explain why]"

### Query
- "What do I have on [concept]?"
- "Where does my work connect to [thinker]?"
- "What are the gaps about [topic]?"
- "What does the wiki say about [concept] across multiple sources?"
- "Find everywhere [concept] appears in the wiki"
- "What thinkers in the wiki deal with [topic]?"
- "What have I written that connects to [thinker]?"

### Filing a Good Answer Back
- "That's worth keeping — file it as a connections page"
- "Save that as a wiki page in concepts/"
- "Add that synthesis to the wiki"

### Lint

**When to lint:** After every 5 ingests, when the wiki exceeds 30 pages, or when query results start feeling stale or contradictory. If you're not sure whether to lint: lint.

**What a clean result looks like:** Zero canon violations. Zero orphan pages. Contradictions flagged (not silently resolved). Missing pages identified. If all of that comes back clean, the wiki is healthy.

- "Run a lint pass"
- "Health check the wiki"
- "What are the orphan pages?"
- "Find contradictions between pages"
- "What concepts keep coming up that don't have their own page yet?"
- "What sources should I ingest next based on the gaps?"

### Checking In
- "What have we done recently?" (reads last 10 changelog entries)
- "What's in the wiki index?"
- "What pages exist about [topic]?"
- "What was ingested last session?"

---

## Setting Up a Project with Its Own Knowledge System

When a project outgrows a simple folder — it's generating its own terms, building its own internal logic, compounding knowledge through its own workflows — use this prompt to set up the project-scoped structure:

> "This project needs its own knowledge system. Create the following structure in 002-PROJECTS/[project name]/: 01-ROOTS/ for the project's foundations, 02-WORKING/ for active development, 03-REGISTRY/ for the project's own compounding knowledge base with an index.md inside it, and 04-ARCHIVE/ for raw material and logs. Then write a README.md at the project root that describes what this project is, what it reads from the shared wiki, and what stays contained inside the project. The shared wiki feeds this project. This project does not write back to the shared wiki unless I say so."

After setup, tell Claude what the project's categories are so it can structure the registry index:

> "The registry categories for this project are: [e.g., characters, terminology, world rules, findings, subroutines — whatever the project generates]"

### Promoting Project Knowledge to the Shared Wiki
When something generated inside a project belongs in the commons:

- "Promote [concept/term] from [project] to the shared wiki — it's bigger than this project now"
- "This belongs in 007-WIKI/concepts/, not just in the project registry"

---

## Multi-Pass Ingest Sequence (for dense sources)

Use this for anything over 50 pages or conceptually dense (thesis, Gizzard, major theory texts):

**Pass 1 — Structural Mapping**
> "Ingest [source] — structural mapping pass. What is the form doing? What are the major moves? What contradictions does it hold open? Discuss with me before writing anything."

**Pass 2 — Concept Extraction**
> "Second pass on [source] — concept extraction. What concepts does this work generate or transform? Each gets its own page. Don't collapse them."

**Pass 3 — Connections**
> "Third pass on [source] — connections. Where does this depart from, extend, or complicate existing wiki pages? Update thinker pages, concept pages, connections pages."

**Between passes:** Claude Code surfaces findings, you discuss, THEN it writes. The discussion is where the good pages come from.

---

## Troubleshooting: When Pages Go Flat

The CLAUDE.md schema encodes anti-flattening as a default constraint — wiki pages should preserve argumentative tension, not resolve it. But LLMs drift. When a page reads like an encyclopedia entry instead of a thinking tool:

- "This page is too flat — rewrite it to think with the concept, not just define it"
- "Show the trickster moves in this argument, don't just describe them"
- "This resolves a contradiction the work holds open — put the tension back"
- "Rewrite this from inside the argument, not from outside it"
- "The humor is part of the argument — it's not in this page. Fix that."
- "Run the anti-flattening check on this page"

---

## Annoying Words to Add
When a word starts appearing too often and feeling like AI filler:
- "Add [word] to the annoying words list in style-and-protocols.md"

---

## Canon Management
- "Add this to canon-lock — [what and why]"
- "Is [element] in canon-lock?"
- "Check the wiki for anything that might violate canon-lock"

---

## When the Context Window Gets Full
Signs: responses feel less sharp, it's losing track of earlier discussion.

Start a fresh Code window and say:
> "Read all files in 008-SANCTUM-CONTEXT/ and the last 10 entries in 007-WIKI/changelog.md. We were [brief description of where you left off]."

That's it. One sentence. The files do the rest.