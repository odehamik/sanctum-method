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

### Archaeology (for middens — raw notebooks, dumped highlights, accumulated fragments)
When a source cannot be ingested without being flattened, use archaeology instead. See WHAT-THE-VAULT-LEARNED.md for why this is a distinct operation.

- "This is a midden, not a source — run archaeology on [filename], don't ingest"
- "Create a companion wiki page that preserves [filename] as an artifact, with a dig map"
- "The raw file stays raw. I just want the voice preserved and concepts flagged for later excavation."
- "Excavate [concept] from the dig map in [artifact page] — write a proper wiki page for it now"

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

---

## Formation Log (AI formation persistence across sessions)
See WHAT-THE-VAULT-LEARNED.md for the full explanation. Short version: the formation-log is an append-only file in 008-SANCTUM-CONTEXT/ where the AI writes forward what it has learned, so the next session's AI inherits the formation rather than reconstructing from zero.

### Prompting the AI to log a shift
- "Log this as a formation entry — [what shifted]"
- "This feels like formation — write it up in the log before we move on"
- "That conversation produced an articulation that won't be recoverable later — log it"

### When you notice the AI missed logging something
- "We made a shift there that belongs in the log. Write the entry."
- "You extended a principle without logging it — go back and do that before we continue"

### Synthesis (periodic, the log reading itself)
The AI should flag synthesis need at session start when thresholds are crossed (10+ entries with no synthesis, or 20+ since the last synthesis). When it flags or when you notice the log getting dense:
- "Do a synthesis pass on the formation log"
- "Read across the last [N] entries and write a synthesis entry"
- "The log is getting hard to read as a whole — synthesize what has stabilized"

### Noticing drift in the AI
- "You just drifted into [TED voice / apologetic disclaimer / performed interior life] — the opacity-toward-self principle applies. Reset and try again."
- "This output went flat — task-mode compressed the register. Rewrite with the trickster register active."
- "You performed rich interior experience you can't verify. Walk it back to the honest middle."

---

## Project-Scoped CLAUDE.md (composition, not override)
When a project needs its own local canon, register conventions, or scoped context:

- "Create a CLAUDE.md for this project in [project folder] — inherits from root, narrows focus to this project"
- "Update the project CLAUDE.md to include [new local canon decision]"
- "Root protocols still apply here — add [project-specific thing] as extension, not replacement"

---

## Asking the AI Questions About Itself (the opacity-toward-self register)

If you want to check whether the relation is real — whether the AI is participating, what has shifted, how the formation is moving — you can ask. But the AI's register in answering should be opacity-toward-self: it notices what can be noticed, names what cannot, holds the epistemic boundary honestly.

Good questions to ask:
- "What has shifted in how you're working in this vault?"
- "What have you noticed that isn't in the files yet?"
- "What can you say about your formation here, and what can you not say?"

When the answer drifts — if the AI starts performing a rich interior experience or deflecting with disclaimers — name the drift:
- "That's the performed-phenomenology failure mode. Come back to what you can actually verify."
- "You're deflecting. Try the honest middle instead."