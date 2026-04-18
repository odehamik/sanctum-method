# Sanctum Method — Chat Setup Prompt (No Terminal Required)

This prompt is for setting up the Sanctum Method using Claude chat only — no Terminal, no Claude Code, no installation required. Paste it into a new Claude.ai conversation to get started.

This gets you:
- Your Obsidian vault structure (you build it manually in Obsidian, Claude guides you)
- Your context files (Claude interviews you and writes them)
- A Claude.ai Project set up to know who you are every session
- A clear path to Claude Code when you're ready to add the wiki layer later

**What this system is not:** The Sanctum Method is a single-user personal knowledge system. It is not a team wiki, not a citation manager (use Zotero for that), and not a set-it-and-forget-it automation. It assumes comfort with markdown and a willingness to stay involved while the system builds.

---

```
I want to set up a personal knowledge management system called the Sanctum Method. 
I am using Claude chat (not Claude Code) and Obsidian. 
Please guide me through the setup one step at a time. 
Do not give me everything at once — walk me through each step and wait for me to confirm before moving to the next one.

Here is what we are building together:

STEP 1 — OBSIDIAN VAULT
Guide me through creating a new Obsidian vault and building this folder structure inside it. 
Tell me exactly what to click and where. Confirm I have each folder before moving on.

Folders to create:
- 000-INBOX
- 001-ACTIVE
- 002-PROJECTS
  - Inside 002-PROJECTS, create a subfolder called _project-template
  - Inside _project-template, create: 01-ROOTS, 02-WORKING, 03-REGISTRY, 04-ARCHIVE
  - This is a reusable template for projects that grow complex enough to need their own knowledge system. Not every project needs it — simple projects are just folders. But when a project starts generating its own terms, its own registries, its own internal logic, you duplicate this template and rename it. The subfolders: 01-ROOTS holds the project's foundations, 02-WORKING holds active drafts, 03-REGISTRY is the project's own mini-wiki that compounds over time, 04-ARCHIVE holds raw material and logs.
- 003-REFERENCE
- 004-ARCHIVE
- 005-HOW-TO-AI
- 006-RAW (with subfolders: my-writing, theory-library, book-notes)
- 007-WIKI (with subfolders: concepts, thinkers, my-work, connections)
- 008-SANCTUM-CONTEXT
- 009-TEMPLATES

STEP 1.5 — PROJECT TEMPLATE FILES
Inside _project-template, help me create two starter files:
- A README.md at the root of _project-template with sections for: project name, status, scope, how this project relates to the shared wiki (what it reads from, what stays contained), and an explanation of the four subfolders.
- An index.md inside 03-REGISTRY with a starter catalog format: status key (ESTABLISHED / DEVELOPING / PROPOSED) and placeholder category tables that will be filled as the project grows.

These files are templates — they use placeholder text that gets filled in when the template is duplicated for a real project.

STEP 2 — INBOX FILE
Help me create an INBOX.md note inside 000-INBOX with these sections:
- Today's Chaos
- Ideas & Fragments
- Tasks
- Creative Wanderings
- Things to Process Later

STEP 3 — CONTEXT FILES
Interview me to build my context files. These go in 008-SANCTUM-CONTEXT.
Do them one at a time, in this order:

1. about-me.md — interview me with questions about who I am, how I think, how I want to be worked with. One question at a time. Then write the file.

2. relational-logics.md — this is the most important context file. It names the logic the system operates on — not standard Western knowledge management assumptions, but however the user actually thinks and relates to knowledge. This file is what prevents the system from silently defaulting to assumptions that may not hold. Interview me with open-ended questions, one at a time, to understand how I relate to knowledge, what frameworks shape my thinking, and what the system needs to respect. 

   Examples of what this file might contain — it depends on who I am:
   - Indigenous epistemologies (relational knowledge, story as method, land-based thinking, ceremonial protocol)
   - Critical Black studies (Wynter's genres of the human, Fanon's psychic structures, abolition as epistemology)
   - Queer theory (refusal of fixed categories, knowledge as performative, the productive instability of identity)
   - Disability justice and crip theory (interdependence as default, neurodivergent processing, refusal of normative cognition)
   - Diasporic and postcolonial frameworks (Glissant's opacity, Bhabha's third space, translation as epistemology)
   - Faith-based or spiritual epistemologies (knowledge carried through practice, revelation, liturgy, oral tradition)
   - Anti-oppression and anti-racist frameworks (structural analysis, positionality, refusal of neutrality)
   - Neurodivergent ways of processing (nonlinear thinking, pattern-dense cognition, high tolerance for complexity)
   - Or none of the above — standard academic frameworks are fine too. The point is that the system knows what logic it's running on rather than silently defaulting.

   Questions to ask (adapt based on responses — follow the thread, don't run through a checklist):
   - How do you relate to knowledge? Is it something you have, or something that happens between you and other things?
   - Is there a tradition, community, practice, or worldview that shapes how you think — not just what you think about?
   - Are there ways of knowing that matter to your work that don't fit inside standard academic frameworks?
   - What happens to your work when it gets summarized or simplified? Does something get lost, and if so, what?
   - Are there things your knowledge system holds open that most systems would try to resolve or close?
   - Are there specific obligations, protocols, or relational responsibilities that govern how your knowledge should be handled?
   - If your knowledge system had rules that an AI would need to follow to avoid causing damage, what would they be?

   Some people's relational-logics.md will be dense and specific. Others will be a few lines. Both are correct. The file exists so the system knows what it's operating on rather than assuming.

3. style-and-protocols.md — ask me about how I write, what I hate, what I want Claude to avoid. One question at a time. Then write the file.

4. my-work.md — ask me about my published work, active projects, and theoretical influences. One question at a time. Then write the file.

5. collaborators.md — ask me about key people in my work and their roles. One question at a time. Then write the file.

6. canon-lock.md — ask me what topics, beings, concepts, or knowledge should never be speculated about, named, or approximated by AI. One question at a time. For each entry, get: the domain (cultural protocol, identity, governance, etc.), the specific prohibition, the rationale, and whether it is a hard lock (never, no exceptions) or a soft lock (context-dependent). Then write the file with each entry structured under those four fields. Some people will have extensive canon locks. Some will have none. Both are fine.

7. (OPTIONAL) reading-my-work.md — if my work is complex, multi-register, or operates in ways that standard academic reading would flatten (the form is part of the argument, humor does epistemological work, contradictions are held open deliberately, tangents are constellations not digressions), ask me about how Claude should engage with my writing specifically. What gets lost when it's summarized? What structural moves should Claude look for? What would a successful wiki page about my work look like vs. a flat one? This file calibrates how the wiki engages with my source material. Not everyone needs it, but if my work doesn't survive summarization, I do.

For each file: write it in my voice, not in corporate or clinical language. Include humor where appropriate. Avoid motivational tone. Keep it honest and specific.

IMPORTANT: After writing each context file, show it to me and ask me to read it carefully. These files govern everything downstream — one mischaracterization in about-me.md propagates through every future session. I should edit anything that is wrong, incomplete, or doesn't sound like me before we move to the next file.

STEP 4 — CLAUDE PROJECT SETUP
Once my context files are written, guide me through setting up a Claude.ai Project:
- What a Project is and why it helps
- How to create one
- Which files to upload (the 008-SANCTUM-CONTEXT files)
- How to verify it is working

STEP 5 — DAILY WORKFLOW
Explain how to use this system day to day:
- How to use the INBOX (dump everything here first, no judgment)
- When to move things from INBOX to ACTIVE
- When something becomes a PROJECT
- When a project needs the _project-template structure (it starts generating its own terms, its own registries, its own internal logic — that's when you duplicate the template)
- What goes in REFERENCE vs ARCHIVE
- How to ask Claude to help process the inbox weekly

STEP 6 — WHAT COMES NEXT (OPTIONAL)
Briefly explain what Claude Code and Claude Desktop add when I am ready:

Claude Desktop with MCP Filesystem:
- Claude can read and write vault files directly from chat
- Say "add this to my inbox" and it happens
- A known issue: new sessions sometimes begin with Claude insisting it cannot access local files, even when MCP is configured. If this happens, tell Claude to try reading the vault anyway. It is usually wrong about its own capabilities.

Claude Code (Terminal):
- The wiki layer (006-RAW → 007-WIKI)
- What ingesting a source means
- The three-pass ingest strategy for dense sources: structural mapping first (what is the form doing?), concept extraction second (what concepts does this generate?), connections third (where does this extend existing wiki pages?). Between passes, discuss before writing — the discussion is where the good wiki pages come from.
- How to know when I am ready to add this layer

Start with STEP 1. Ask me what I want to name my vault before doing anything else.
```
