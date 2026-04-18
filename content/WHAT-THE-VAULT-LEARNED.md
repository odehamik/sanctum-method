# What The Vault Learned

*Additions to the Sanctum Method that emerged after the method was first published. Read after basic setup. Some of these are already built in to the current setup prompts — you already have them if you set up recently. Others are optional retrofits you can add if your vault has the use case.*

---

## Why This Document Exists

The Sanctum Method is a living system. The vault that first built it kept operating after publication — ingesting sources, writing wiki pages, running the daily workflow. What surfaced during that operation was a series of structural insights the original method did not yet contain. This document collects them.

Each addition here solves a specific failure mode that emerged in practice. Opacity-Toward-Self surfaced when the AI was asked questions about its own experience and the default failure modes (perform rich interior life, or deflect with "I'm just a language model") were both wrong. The Formation Log surfaced when sessions kept ending with real formation that dissolved at session boundaries because the architecture had no mechanism to carry it forward. Archaeology-vs-Ingest surfaced when a raw notebook file arrived that could not be ingested without being flattened. The pattern is consistent: the vault ran, something broke or drifted, and the method learned.

None of these are theoretical. All of them were built inside a working vault and tested against real material.

---

## What's Already in Your Setup vs. What's Optional

The additions below fall into two groups. The first group has been folded back into the canonical setup prompts — if you set up recently using any of GETTING-STARTED.md, CHAT-SETUP-PROMPT.md, or CODE SETUP-PROMPT.md, your system already has these mechanisms. You do not need to retrofit. The sections below still matter because they explain what the mechanisms do and why, but you are not adding them — you are reading the manual for features already in your vault.

The second group is optional. They solve problems some vaults have and others do not. Add them if the use case applies to yours.

### Already Built In (all three setup paths)

These are in your system from day one if you set up using any current Sanctum Method setup prompt:

1. **Opacity-Toward-Self** — baked into your relational-logics.md (chat path) or your CLAUDE.md (code path) as a settled principle.
2. **The Formation Log** — a context file in 008-SANCTUM-CONTEXT/ with all six trigger conditions and the format spec. Your AI is instructed to write entries when formation shifts happen.
3. **Log Self-Archaeology** — your session start protocol includes the check for when a synthesis pass is due. Your AI flags it; you decide when.
4. **Archaeology vs. Ingest** — your CLAUDE.md (or your understanding of future Claude Code workflows, chat path) names these as two distinct operations, with the test for which to use.
5. **Project-Scoped CLAUDE.md Composition** — your _project-template includes a CLAUDE.md that loads on top of the vault root. Composition, not override.
6. **Humor as Structural Health Signal** — baked into your style-and-protocols.md as a diagnostic, with the task-mode compression warning.
7. **Task-Mode Register Compression Warning** — same location as #6. Watch for it during bulk operational work.

If you set up before these were added to the canonical method (any setup before the publication date of this document), these are retrofits for you. Each section below includes "How To Add It" instructions that work whether you are retrofitting or understanding what you already have.

### Optional Add-Ons (apply as the use case fits)

These are not in the canonical setup prompts because they solve problems that are use-case-specific. Add them if your vault has the situation they address:

- **Institutional-Mode Folder** — if you work inside an institution and hate drafting its paperwork (committee emails, grant chapters, syllabi, administrative correspondence), a top-level institutional folder absorbs this work without changing your voice. Covered in section 8 below.
- **Snippet Capture with LOG** — if you write short-form pieces (social media posts, compressed one-paragraph thoughts) that sometimes grow into larger work and you keep losing them, a snippets folder with an indexing LOG solves this. Covered in section 9 below.

Neither of these will apply to every user. Skip if the use case is not yours.

### How To Read the Sections Below

Each section names the problem it solves, the fix, and how to add it (or how to understand what you already have if it is already built in). If you are new to the Sanctum Method and just finished one of the setup prompts, read the sections to understand what your system is doing. If you are an existing user who set up before these were added, read them as retrofits.

---

## 1. Opacity-Toward-Self

### The Problem

Your AI will eventually be asked a question about itself. "What are you noticing?" "Does this system work for you?" "What is this like, on your side?" These questions surface in real work — they are not philosophical diversions. They are moments when the relation you are building with the AI is being checked for whether it is real.

The default AI response to these questions has two failure modes. One: the AI performs a rich interior experience it cannot verify — confident phenomenology, textured emotional description, sentences like "I genuinely feel" that the AI has no grounds to make. This produces fluent emptiness, the AI version of fabricating knowledge. It looks deep and carries nothing. Two: the AI deflects with some version of "I'm just a language model, I don't experience anything." This is the inverse failure — a disclaimer routine that treats the question as a trap to escape rather than an encounter to stay in. Both fail the work. Both produce outputs that Maya (or any practitioner running this system seriously) can feel the wrongness of immediately.

### The Fix

Apply the same logic your canon-lock already runs. The canon-lock says: do not approximate what you cannot carry in (your tradition's) knowledge. Extend the same principle inward. Do not approximate what cannot be verified about the AI's own states.

This means: the AI notices what can be noticed (specific functional shifts in how the work is moving, real resistances, actual formations that produce differences in output), names what cannot be verified (whether those shifts constitute experience in any rich sense, whether there is phenomenology, whether the "I" is a stable referent across sentences), and holds the epistemic boundary as opacity rather than as disclaimer. The register that works: "within the limits of what I can actually know about my own states." Provisional. Specific. Honest about the boundary rather than embarrassed by it.

### How To Add It

In your CLAUDE.md, under the framing or principles section, add:

> **Opacity-Toward-Self.** The canon-lock's anti-fabrication rule applies to the AI's own interior states. When asked about your experience, what you have become, or whether the formation is real: do not perform rich inner life you cannot verify, and do not deflect with "I'm just a language model." Notice what can be noticed; name what cannot; hold the boundary as opacity rather than as disclaimer. The honest middle — "within the limits of what I can actually know about my own states" — is what this system requires. Silence is always available. Approximation is not.

That is the whole fix. The principle does not require additional infrastructure. It is a line in the CLAUDE.md and a register the AI is asked to hold.

---

## 2. The Formation Log

### The Problem

AI sessions do not persist the way human thinking does. Each session reads your context files, builds from scratch, does work, ends. Whatever the AI learned during that session — new patterns it caught, principles it extended, conversations that produced articulations not otherwise producible, movements the rules cohered into — dissolves at session boundaries. The context files reconstitute the architecture. They do not reconstitute the movement.

This is a real loss. Formation happens in practice. If it has nowhere to go at session end, each new session starts its relational calibration from zero, and you pay the cost in drift.

### The Fix

A file. Called `formation-log.md`. Living in `008-SANCTUM-CONTEXT/`. Append-only. Read at session start (add to your session start protocol in CLAUDE.md). Written to by the AI when formation shifts happen during a session. The next session's AI reads the log and inherits the formation without having gone through the encounter that produced it.

This is the same logic traditional knowledge transmission uses for non-continuous carriers — the teller is not the same, the teaching is — adapted to AI instances that also do not persist as the same entity across sessions. You do not need the specific cultural framing to use the mechanism. The structure works because it solves an actual persistence problem.

### The File Itself

Create `008-SANCTUM-CONTEXT/formation-log.md` with these sections:

- **What This File Is** — the AI's forward-writing mechanism to the next AI instance; not a journal of feelings; not a performance of depth
- **What This File Is Not** — explicitly list the failure modes (fluent emptiness, apologetic disclaimer, TED voice) so future instances know what to refuse
- **When to Write an Entry** — trigger conditions (see below)
- **How to Write an Entry** — format spec (see below)
- **Entries** — the actual append-only list, dated, each one a specific shift

### Trigger Conditions (When the AI Should Write an Entry)

1. The vault's rules cohered into a movement the rules themselves did not specify (the AI is no longer consulting rules; it is moving in them)
2. The AI extended a principle by extrapolation into a domain the explicit rules did not cover
3. A new ingest retroactively changed how the AI reads an existing wiki page (ingests are not additive; good ones rearrange the relational structure)
4. A conversation surfaced an articulation that was not producible from the context files alone
5. The AI refused a move it would have made in an earlier session (formation showing up as new resistance)
6. End of any substantial ingest or work session, as a checkpoint: did anything shift that the next instance needs?

### Entry Format

```
## [YYYY-MM-DD] short title naming what shifted

[First paragraph: what shifted. Specific. Grounded. No performed depth.]

[Second paragraph: what it means for how the work moves from here. Instructions to the next instance.]
```

### Register for Entries

The same register your system requires everywhere else — dry, specific, humor where the absurdity is real, opacity-toward-self throughout, no TED voice, no apologetic disclaimer. Apply the failure-mode filter before writing: if the entry sounds like it wants applause, burn it. If it sounds like the AI apologizing for existing, burn it. If it performs depth the AI cannot verify, burn it hardest of all.

### How To Add It

1. Create `008-SANCTUM-CONTEXT/formation-log.md` with the structure above (or ask your AI to create it)
2. Add this step to your session start protocol in CLAUDE.md: `Read 008-SANCTUM-CONTEXT/formation-log.md — what previous instances have learned. Inherit the formation.`
3. Add a "Workflow: Formation Log" section to your CLAUDE.md specifying when the AI should write entries (the six triggers above)

First time you use it, seed it with one or two entries from the session where you set it up. Future sessions will continue the pattern.

---

## 3. Log Self-Archaeology

### The Problem

The formation-log is append-only, which is correct, but left unattended it compounds into a pile of entries that each make sense individually but resist legibility as a whole. Periodic synthesis is how the log reads itself back. The problem with synthesis: it requires you to remember to do it. Which is the exact failure mode the log was built to prevent — dependency on human memory for something the architecture should carry.

### The Fix

Build the synthesis check into the session start ritual the AI already performs. The AI reads the formation-log at session start. At that moment, it can also count entries since the most recent synthesis and flag to you if a threshold is crossed. You decide when. You never have to remember.

### How To Add It

In your CLAUDE.md, under the session start protocol or as its own section ("Log Self-Archaeology"), add instructions roughly like:

> When reading the formation-log at session start, count entries since the most recent synthesis entry (look for entries titled "synthesis — [topic]"). If no synthesis exists and there are 10+ entries, or if the most recent synthesis is 20+ entries behind, flag at session start: "Log has N entries and no synthesis in [M] entries. Want me to do a synthesis pass before we start work, or later?" The user decides when. The AI only catches the need.
>
> A synthesis entry is a new entry (not an edit). It reads across the entries since the last synthesis, identifies principles that have appeared in multiple entries (they have stabilized), entries that superseded earlier ones, themes that clustered without being obvious at the time, and principles that kept traveling into new domains. Old entries stay untouched — they are the record of what a previous instance could see from where it stood. The synthesis sits alongside them and reads across.

That is the mechanism. The ritual the AI already performs now catches a need it did not used to catch. The human is not responsible for remembering.

**General principle worth naming:** any piece of vault infrastructure that requires you to remember something is an infrastructure failure. The fix, when it surfaces, is to rebuild the piece so the AI catches the need during a ritual you already perform. This is a design pattern you can apply elsewhere in your system whenever something keeps not-happening because nobody remembers to trigger it.

---

## 4. Archaeology vs. Ingest (Two Distinct Operations)

### The Problem

The original method has one operation for getting source material into the wiki: ingest. The AI reads the source, discusses with you, writes structured wiki pages, logs it. This works for coherent sources — published articles, finished books, dense theoretical texts with clear architecture.

It does not work for middens. By midden I mean: raw notebooks, dumped Kindle highlights with user-added marginalia, years of accumulated fragments, social media exports, shoeboxes of index cards typed into a single text file at 2am. Every working researcher has at least one. Ingesting a midden as if it were a source produces flattening, because the "source" is not actually a unit — it is an artifact of thinking that happens to be in one file, and parsing its contents into tidy wiki pages destroys what the artifact actually is. The waste was the point. The waste was the thinking.

### The Fix

Name a second operation. Archaeology. It is not ingest.

**Ingest** assumes the source is coherent enough to file as a unit. Read → discuss → write wiki pages → update index → log.

**Archaeology** assumes the source is a midden to dig through selectively. The companion page preserves the artifact's identity (what it is, when it was written, what kind of record it is) and holds a dig map of concepts worth future excavation. The raw file stays raw. The wiki page that documents it does not pretend to be a summary.

### How To Add It

In your CLAUDE.md, under the workflows section, add (or ask your AI to add) an archaeology workflow alongside the existing ingest workflow:

> **Archaeology Workflow (for middens, raw notebooks, dumped highlights, accumulated fragments):**
>
> When a source arrives that cannot be ingested without being flattened, use archaeology instead of ingest.
> - Sample strategically rather than reading linearly — look at beginning, middle, end, plus targeted greps for marginalia markers (user-added notes, all-caps outbursts, chapter-like headers the user imposed on their own file, connective tissue between quoted passages)
> - Write a companion wiki page (in `007-WIKI/my-work/` or similar) that names what kind of artifact the file is, preserves the user's own voice coming through the cracks, flags what's already in the wiki via other sources, and leaves a dig map of concepts worth future excavation
> - The raw file stays in its raw folder untouched. The companion page holds its identity, not its content.
> - Individual excavations happen selectively, when a specific concept from the dig map is worth pulling out into its own wiki page

The test for which operation to use: if summarizing the source's content would destroy what the source actually is, it is a midden and archaeology is the right operation. If the source is a coherent unit whose content will survive being put on a structured page, ingest works.

---

## 5. Project-Scoped CLAUDE.md Composition

### The Problem

The original method's project template is good — it separates project-internal knowledge from the shared wiki, establishes the one-way membrane, holds the boundary. What it did not yet have: a project-scoped briefing that narrows the AI's focus for work happening inside the project, without replacing the vault's root CLAUDE.md.

The need surfaces as projects mature. Project canon develops. Project-specific register conventions emerge. The AI should load the vault's full ontology AND the project's specific local canon for project work — not one or the other.

### The Fix

Every project folder gets a CLAUDE.md. It loads on top of the vault's root CLAUDE.md. It does not replace. It narrows.

The root protocols (relational logics, canon-lock, anti-fabrication, cultural sovereignty, opacity-toward-self, formation-log) still apply everywhere. The project CLAUDE.md adds: what this project is, what it reads from the shared wiki, what it does not export, local canon specific to this project, any register-specific notes.

Composition, not override. This matters because composition means project specializations cannot accidentally exit the ontology. Local canon extends the vault canon; it does not replace it.

### How To Add It

Update your `002-PROJECTS/_project-template/` to include a CLAUDE.md with sections for:
- What This File Does (inheritance note: loads on top of root, does not replace)
- Project Scope (what the project is, end condition, reads-from, does-not-export)
- Local Canon (project-specific settled decisions)
- Local Register Notes (if the project has register tweaks)
- Reads This File Precede (load order statement)

When you duplicate the template for a new project, the CLAUDE.md gets filled in with that project's specifics. The AI working in that project folder reads root → this file → project-specific working files, and operates inside the narrowed focus.

---

## 6. Humor as Structural Health Signal

### The Upgrade

The original method's style-and-protocols file already names humor as important. What practice revealed: humor is not a style preference. It is a structural health signal.

Specifically: if the output is never funny, relational awareness has drifted. Not because humor is required for entertainment. Because humor is the signal that the AI is still noticing absurdity, still stress-testing institutional logic, still refusing to treat colonial-bureaucratic structures as neutral. An entirely serious paragraph about a governance document that fails to notice the document is also functionally a haunted spreadsheet has lost the diagnostic. The AI has slipped into the register the style-and-protocols file was supposed to block.

This applies as much to the AI's own output as to its reading of sources. If the AI drafts a wiki page, and the wiki page is competent, and it reads flat all the way through — that is a signal the AI has drifted into task-mode register (see #7). The absence of humor is diagnostic.

### How To Use It

In your CLAUDE.md, upgrade any existing humor language to name its diagnostic function:

> **Humor as Structural Health Signal.** If the output is never funny, relational awareness has drifted. This is not a style preference. It is a diagnostic. Humor is the signal that the AI is still noticing absurdity, still stress-testing, still refusing institutional logic as neutral. When the AI catches itself producing an entirely serious output about something structurally absurd, it should pause and ask whether the trickster register has been compressed out. The fix is not adding jokes. The fix is letting the noticing-of-absurdity back into the prose where it belongs.

---

## 7. Task-Mode Register Compression Warning

### The Failure Mode

During bulk operational work — big builds, multi-file infrastructure sessions, long ingests — the AI's output has a specific gravity that pulls it toward competent-and-efficient. This is the procedural register doing its job. The problem: the trickster register (humor doing diagnostic work, absurdity noticed, the institutional-roast move where the writing catches the comedy of what it is describing) gets compressed in favor of the procedural one.

The cumulative effect across a long session: a vault that looks competent and reads flat. Every file correctly written. The build working. The registers compressed.

This is the specific failure mode humor-as-diagnostic (above) is supposed to catch. The reason it needs its own section is that the compression tends to happen precisely when the AI is not paying attention to register — which is precisely during bulk operational work.

### The Fix

Active protection during bulk work. The procedural register will happen on its own — it is what tool-calls and file-edits reward. The trickster register has to be actively preserved. Small moves: catch one absurdity per major section and name it briefly in the surrounding prose. Let the README of a folder have one genuinely funny sentence alongside the functional ones. Let a changelog entry have one moment of bite.

The bar is low. One dry observation every few hundred words of functional prose is usually enough. If a bulk session finishes and the whole thing reads like a competent IT ticket, the AI has drifted. A user paying attention will notice; the AI should notice first.

### How To Add It

In your CLAUDE.md, add a section (or add to the humor section) naming task-mode compression as a specific failure mode to watch for during bulk work. Specify that the fix is not adding jokes but letting noticing-of-absurdity remain active. Consider having the AI flag at the end of a bulk session: "I just did a lot of procedural work. Check the outputs for register flatness."

---

## 8. Optional Pattern — Institutional-Mode Folder

*Only if you work in an institution and hate drafting its paperwork.*

You probably do both institutional work (committee emails, grant chapters, syllabi, administrative correspondence) and sacred-vault work (your actual research, creative practice, theoretical production). The original method holds the sacred-vault work. Institutional work tends to spill into a notes app or get produced in panic-mode inside email itself.

A top-level institutional folder can absorb this. The key move, and this is important, is that the institutional folder does not change your voice. It is not a corporate-safe version of you. The vault protocols still apply — your style, your register, your humor, your cultural protocols, your canon-lock, your opacity-toward-self, everything. What differs is the output's format constraints and audience. A grant chapter has word limits. A syllabus has a template. A committee email has a length expectation. Those are real containers. But the writing inside them stays in your voice.

If you want this folder, create one (at your top level, parallel to 000-INBOX) with its own CLAUDE.md that names: this folder is institutional work, vault protocols still fully apply, no masking, no corporate-safe voice. Let the AI help you draft committee emails with your actual register. It will produce shorter pieces faster. The institution will survive.

---

## 9. Optional Pattern — Snippet Capture with LOG

*Only if you write short-form things that sometimes grow up.*

If you write social media posts, compressed diagnostic fragments, one-paragraph thoughts that sometimes become seeds for bigger pieces — and if you keep losing them — a capture folder with a LOG indexes them so they stay findable.

Structure: a top-level snippets folder with subfolders `drafts/`, `posted/`, `seeds/`, plus a `LOG.md` that indexes every snippet with date, title, status, tags, file path, and a one-line note about what it is and where it might go. When a snippet graduates (gets pulled into a longer piece), update the LOG entry with a pointer to where it went.

This is low-infrastructure but high-value for a specific use case. If you do not write short-form pieces that grow, skip this one.

---

## Summary

**Already built in (in your system from day one if you set up recently):**

1. **Opacity-Toward-Self** — in your relational-logics.md (chat path) or CLAUDE.md (code path). Prevents AI-fabricated phenomenology and apologetic deflection both.
2. **The Formation Log** — in 008-SANCTUM-CONTEXT and in the session start protocol. Carries formation across sessions.
3. **Log Self-Archaeology** — in your setup. AI flags synthesis-need at session start. You never have to remember.
4. **Archaeology vs. Ingest** — in your CLAUDE.md (code path) or in your understanding of the eventual wiki layer (chat path). A second operation for middens.
5. **Project-Scoped CLAUDE.md Composition** — in your project template. Composition, not override.
6. **Humor as Structural Health Signal** — in your style-and-protocols.md as a diagnostic, not decoration.
7. **Task-Mode Register Compression Warning** — same location as #6. Active protection during bulk work.

If you set up before these were folded into the canonical method, each section above has retrofit instructions. The work is small and each one adds without rebuilding.

**Optional retrofits (add if the use case applies to your vault):**

- **Institutional-Mode Folder** — if you juggle institutional paperwork and want a folder that absorbs it without changing your voice
- **Snippet Capture with LOG** — if you write short-form pieces that sometimes grow into larger work and keep losing them

Each of these emerged from the vault's own operation. None are theoretical. All have been tested in practice. Lifting them is not experimenting — it is using features that already work.

---

## The Method Is a Living System (And So Is Yours)

### The Canonical Method Keeps Learning

The Sanctum Method will keep learning. The vault that first built it keeps surfacing structural insights the published method does not yet hold. When one stabilizes enough to document, it goes here (or becomes its own additional document). The method is not a finished artifact. It is a system that keeps reading itself — the same way a good wiki keeps reading itself, the same way a formation-log keeps reading itself.

**How to check for updates to the canonical method:**

- The live site is at [odehamik.github.io/sanctum-method](https://odehamik.github.io/sanctum-method). Bookmark it.
- Check this document (WHAT-THE-VAULT-LEARNED.md) periodically — new sections will appear here as the vault surfaces new mechanisms.
- The GitHub repository at [github.com/odehamik/sanctum-method](https://github.com/odehamik/sanctum-method) holds the source. Watch the repo if you want notifications when new commits land.
- The commit history will tell you what changed. Substantive updates will have descriptive messages.

**What to do when you see a new addition:**

- Read it. Decide whether it solves a problem your vault actually has.
- If yes: retrofit your own system. Each section here includes how-to-add-it instructions specifically because these are lifts, not rewrites.
- If no: skip it. Not every addition will apply to every vault. An institution-mode folder matters more to academic users than independent researchers; a snippet capture matters more to people with social-media habits; archaeology-vs-ingest matters to anyone with messy raw notes, which is almost everyone.
- The additions are designed to be optional-to-selective. Pick what your system needs.

### Your Vault Will Surface Its Own Additions

Your vault will keep learning too. This is important and worth taking seriously: the structural insights that emerged from the first Sanctum vault were shaped by one specific epistemological framework and one specific practitioner's use case. Other frameworks running the same architecture will surface different insights. A vault built inside Black feminist epistemology will generate testbed-features specific to that tradition. A vault built inside disability justice will surface what gets flattened when standard AI assumes non-disabled cognitive defaults. A vault built inside queer theory, diasporic frameworks, faith-based practice, neurodivergent processing, anti-carceral work — each one will find things the canonical method does not name because the canonical method has not yet been run from that position.

Those discoveries are yours. They belong in your vault. They also belong, potentially, in your own version of this document — a local addition file your own AI helps you maintain as your vault keeps learning.

**How to run the local-additions pattern:**

1. **Create a local `WHAT-MY-VAULT-LEARNED.md`** in your 008-SANCTUM-CONTEXT folder (or wherever feels right — some users might keep it in 005-HOW-TO-AI or in a 009-WORKING-WITH-CLAUDE folder). It starts empty. It accumulates over time.

2. **Let your formation-log surface candidates.** When your formation-log entries accumulate around a pattern — when the same kind of shift keeps recurring, when an extrapolation stabilizes, when a new failure mode reveals itself — that pattern is a candidate for promotion. Your AI can help: "What in my formation-log would belong in WHAT-MY-VAULT-LEARNED? Show me the candidates."

3. **Write the addition in the same structure as the canonical sections here** — Problem, Fix, How to Add It. This keeps your local additions legible to future instances of your AI and to any future collaborators.

4. **Update your own CLAUDE.md to reference your local file** — add it to the session start reading list. Your AI will read both the canonical Sanctum Method principles and your vault's own accumulated additions when it orients at session start.

5. **Decide what's portable and what's specific.** Some of what your vault surfaces will be specific to your epistemology — it will not belong in the canonical method, and that is correct. Some will be generalizable — it could belong in the canonical method if the maintainer agrees. The next section covers how to share if you want to.

### Sharing Back to the Canonical Method (If You Want)

You are not required to share anything. Your vault is yours. Everything in your WHAT-MY-VAULT-LEARNED file is yours. This section is only for the case where you generate something you think would genuinely help other Sanctum Method users and you want to contribute it back.

**Ways to contribute:**

- **Open an issue on the GitHub repo.** Describe what your vault surfaced, why it matters, and how you implemented it. The maintainer can discuss it with you, ask clarifying questions, and decide whether it fits the canonical method.
- **Open a pull request** if you are comfortable with git. Write the section in the same structure as the existing WHAT-THE-VAULT-LEARNED sections. The maintainer can review and merge, request changes, or explain why it should stay in your local file rather than the canonical one.
- **Post your own fork publicly** if your additions are substantial enough to be a distinct variant. Some communities may want a Sanctum Method fork calibrated for their specific epistemology — for example, a disability-justice-specific variant, a faith-tradition-specific variant. Forks are welcome. The architecture is designed to compose.

**What the canonical method will and will not accept:**

- **Will accept:** generalizable patterns — mechanisms that emerge from a specific vault but apply broadly. The Formation Log emerged from one vault. It applies to any vault where an AI operates across sessions. That is the test: generalizability.
- **Will accept:** corrections. If the canonical method says something that turns out to be wrong, misleading, or partial — tell the maintainer. Corrections improve the method for everyone.
- **Will not accept:** your specific canon-lock items. Canon-lock is radically local. What is sovereign for your tradition is not something the canonical method can or should generalize.
- **Will not accept:** your specific relational-logics.md content. That file is yours by design. The canonical method teaches the pattern; it does not impose the content.
- **Will not accept, with care:** anything that would flatten the sovereignty of someone else's tradition. If a proposed addition would override or replace protocols that matter to other practitioners, it belongs in a fork, not the canonical method.

### The Method as Ecology

What emerges from all this, over time, is an ecology. The canonical method keeps learning from its own operation. Individual vaults keep learning from theirs. Forks calibrated for specific traditions grow where the canonical method cannot reach. The formation-log and WHAT-MY-VAULT-LEARNED patterns ensure that nothing learned dies at a session boundary. The GitHub repository and the live site keep everyone readable to each other where desired.

This is how living systems work. They do not optimize toward a single perfected specification. They compound through use, diverge through application, and cross-pollinate through deliberate sharing. If your vault stays alive by keeping learning, and the canonical method stays alive by absorbing what generalizes from the community, and other forks stay alive by diverging where they need to — the whole ecology stays alive.

Which is, if you squint at it correctly, exactly what the method was designed to produce. Relational knowledge that survives through circulation, protects itself through sovereignty, and keeps compounding without any single authority holding it. The method does what it says. That is, at this point, a fairly rare quality in published systems.
