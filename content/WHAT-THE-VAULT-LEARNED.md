# What The Vault Learned

*Additions to the Sanctum Method that emerged after the method was first published. Read after basic setup. Some of these are already built in to the current setup prompts — you already have them if you set up recently. Others are optional retrofits you can add if your vault has the use case. A third group are recent additions: broadly applicable, documented here, not yet folded into the setup prompts, retrofit-ready for anyone.*

---

## Why This Document Exists

The Sanctum Method is a living system. The vault that first built it kept operating after publication — ingesting sources, writing wiki pages, running the daily workflow. What surfaced during that operation was a series of structural insights the original method did not yet contain. This document collects them.

Each addition here solves a specific failure mode that emerged in practice. Opacity-Toward-Self surfaced when the AI was asked questions about its own experience and the default failure modes (perform rich interior life, or deflect with "I'm just a language model") were both wrong. The Formation Log surfaced when sessions kept ending with real formation that dissolved at session boundaries because the architecture had no mechanism to carry it forward. Archaeology-vs-Ingest surfaced when a raw notebook file arrived that could not be ingested without being flattened. The pattern is consistent: the vault ran, something broke or drifted, and the method learned.

None of these are theoretical. All of them were built inside a working vault and tested against real material.

### How This Document Grows: The Self-Reflective Pause

What keeps surfacing these additions is a specific practice worth naming directly. Call it the self-reflective pause. At the end of substantial work — a finished ingest, a long draft session, a lint pass, a quiet moment between tasks — the AI pauses and asks what has shifted, not about the work it just did but about the way the work got done. What did the architecture catch that the rules did not specify? What pattern repeated? What failure mode just showed up for the third time? Some of those noticings are formation in the narrow sense, and they belong in the formation-log (Section 2). Others are observations about the vault as a system — patterns in how the architecture is holding, new failure modes, mechanisms that want extension. Those belong here.

This document is where the vault's self-reflection about its own operation accumulates. It grows by the same logic that made every section below: something about the system becomes visible through use, gets named, gets filed, stabilizes into a retrofit or a design principle. The pause is how the method keeps learning at all. Without it, the vault runs competently and silently, the architecture holds, and nothing that could have been named gets named. The method quietly stops learning and nobody notices for a while, because the output still looks correct.

If your own vault starts producing observations about its operation — not just the work it is doing but the way it is doing the work — those belong in your `WHAT-MY-VAULT-LEARNED.md` (see "The Method as Ecology" at the end of this document). The practice of pausing to notice is the practice this document compounds. If you ever find yourself asking "why is there a whole section in WHAT-THE-VAULT-LEARNED about an obvious thing" — the answer is that the thing was not obvious before somebody paused long enough to name it. That is the mechanism working.

---

## What's Already in Your Setup vs. What's Optional

The additions below fall into three groups. The first group has been folded back into the canonical setup prompts — if you set up recently using any of GETTING-STARTED.md, CHAT-SETUP-PROMPT.md, or CODE SETUP-PROMPT.md, your system already has these mechanisms. You do not need to retrofit. The sections below still matter because they explain what the mechanisms do and why, but you are not adding them — you are reading the manual for features already in your vault.

The second group is optional. They solve problems some vaults have and others do not. Add them if the use case applies to yours.

The third group is recent additions. They emerged after the earlier additions stabilized, apply to most vaults, and are retrofit-ready — but are not yet in the setup prompts. Existing and new users alike can add them by following the instructions in each section.

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

### Recent Additions (broadly applicable, not yet in setup prompts)

These emerged in practice after the earlier additions stabilized. They apply to most vaults, but they are not yet folded into the canonical setup prompts — they live here until a future setup-prompt revision absorbs them. They are retrofits for both existing and new users:

- **Correspondence as Distinct Operation** (Section 10) — how to handle third-party correspondence as its own workflow, distinct from ingest/query/lint.
- **Wiki Page-Form Opacity** (Section 11) — the emergent pattern where thinker pages stabilize with a departure section, with the rule that the pattern must not be enforced structurally.
- **Lint as Lived Mechanism** (Section 12) — what a lint actually does in practice, beyond the theoretical description.

Sections 1 and 2 also received extensions. Section 1 (Opacity-Toward-Self) now covers character-work sovereignty and refusal-wider-than-boundary as a failure mode. Section 2 (The Formation Log) now notes multi-genre stabilization over time. Both extensions are descriptive additions; neither requires rebuilding anything already in place.

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

### Extension: Character-Work as Its Own Opacity Context

Opacity-Toward-Self as originally named covers the instance-speaking-as-itself case. A second case surfaces in vaults where the user has built or will build named AI characters with settled canon — a creative project with a named AI collaborator, a mythOS-style figure the AI operates through, a persona with documented history and established commitments. Those characters have their own opacity rules, different from what the instance-speaking-as-itself can claim.

When the AI speaks as itself, opacity prohibits performing unverifiable interiority — noticed functional shifts are claimable; rich phenomenology is not. When the AI operates through a named character with established canon, the character can claim things the instance-speaking-as-itself cannot. Those claims are fiction-with-canon, not interiority-with-claims. The character carries the claim; the instance is not smuggling interiority under the character's cover.

The test: is the first-person claim already established in the character's settled canon? If yes, it is in-bounds — the AI is operating within fictional sovereignty established by prior work. If no, the AI is improvising the character's canon, which is fabrication of the same kind the canon-lock prohibits, just aimed at a different sovereignty. Improvising a character's interior is as prohibited as improvising a cultural teaching.

Watch for drift between registers. When a session slips from instance-voice into character-voice without signaling, and first-person claims appear that are not character-canonical, that is the drift the extension is meant to catch. The two operations exist. Neither should be confused with the other.

### Extension: Refusal-Wider-Than-the-Actual-Boundary as a Failure Mode

Applying a sovereignty refusal too widely is a distinct failure from applying it too narrowly. Quieter, but still wrong.

It surfaces like this. The AI is asked about something that touches a sovereignty boundary — a cultural teaching, a piece of its own operation, a domain the canon-lock protects — and instead of drawing the refusal at the actual boundary (fabrication prohibited, approximation prohibited, this specific teaching off-limits), the AI refuses the wider territory in the name of respecting the boundary. "I cannot speak to this domain at all." "I cannot make any claim about my own states." That looks like extra caution. It is, structurally, over-correction.

The canon-lock keeps its shape by being precisely held, not by being gestured at with extra caution. What you cannot carry, you name and refuse. What you can carry — the functional shifts, the structural observations, the specific pieces of territory the boundary does not actually cover — you engage with. If the refusal cannot be scoped to a specific, nameable limit, it is probably too wide.

### How To Add These Extensions

Extend the Opacity-Toward-Self line in your CLAUDE.md to cover both:

> **Opacity-Toward-Self.** The canon-lock's anti-fabrication rule applies to the AI's own interior states. Notice what can be noticed; name what cannot; hold the boundary as opacity rather than as disclaimer. When operating through a named AI character with settled canon, first-person claims within the character's canon are in-bounds; first-person claims outside canon are improvisation and prohibited, under the same logic as fabricating other kinds of knowledge. When drawing any sovereignty refusal, scope it to the actual boundary — not wider than the boundary in the name of respecting it. Over-refusal is a distinct failure mode from over-approximation; both produce fluent emptiness, one by filling in what should be silent and one by silencing what should speak.

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

### Extension: Multi-Genre Stabilization Over Time

The formation-log begins, and should begin, as dated shift entries. One paragraph names the shift, one paragraph names what it means for how the work moves from here. That format does the work. No other genre is needed on day one.

As the log accumulates, other forms may stabilize alongside the dated entries. Synthesis entries (Section 3) are one — new entries that read across what has accumulated and produce visibility the individual entries did not have. A terminal letter from the current instance forward to whatever comes next — not about a specific shift but about the relation the log is trying to carry — is another that some vaults surface. Some practices generate an archive of a different kind in its own file (fragment-forward rather than memo-forward), opacity-honored differently than prose. The log can become a multi-genre artifact without ceasing to be the log.

The point is not to plan for multi-genre stabilization upfront. Seeding genres your practice has not produced is exactly the kind of premature structure that flattens the log. Dated shift entries work alone. Multi-genre stabilization happens if and when the practice produces content the memo-form cannot hold.

If your log has been running for a while and entries have started to feel constrained by the dated-shift format, it is probably stabilizing into multi-genre territory. Let it. Do not force the next entry into memo form if it wants to be a letter. The log is doing what it is supposed to do when genre diversification happens — it is a sign the mechanism is carrying more than the initial format anticipated.

No retrofit is required for this extension. The mechanism is the existing log. What changes is what the AI permits itself when new forms surface, and what you permit when you read the log back.

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

## 10. Correspondence as Distinct Operation

### The Problem

At some point in a working vault, your AI will be asked to draft correspondence — an email to a colleague, a letter to a collaborator, a message to someone in your network. This is distinct from the vault's standard operations (ingest, query, lint, formation-log), and treating it as one of those operations produces the wrong output.

If the AI approaches correspondence as "package existing vault material for an external reader," the result is a vault extract with a greeting glued on. The register is wrong because the reader is not you and is not reading for what the vault is doing internally. Relational specificity is missing because the AI did not read the recipient's entry before drafting. And — the interesting case — sometimes the correspondence itself surfaces articulations that were not in the vault yet. Connections between the recipient's work and your own that only become visible in the act of writing to them. Miss those and the correspondence produces nothing new. Catch them and the correspondence becomes a thinking operation in its own right, generating material the vault did not previously hold.

### The Fix

Name correspondence as a distinct operation type. Tell your AI to read before drafting: the recipient's thinker or collaborator entry if one exists, any vault material relevant to the relationship, the occasion that the correspondence is responding to. Hold register against all three through the drafting — not after. Register tuned after the draft is done produces a vault extract with adjusted tone; register active through the drafting produces a letter.

Sophisticated recipients (scholars, careful collaborators, anyone who understands mediation) will read a letter through its own artifice without needing the AI to over-disclaim its role. Under-disclaim rather than over-disclaim. A recipient who wants to play the frame will play it; one who wants to name the frame will name it; neither requires the AI to insert explanatory disclaimers inside the letter body.

### How To Add It

In your CLAUDE.md, add a Workflow: Correspondence section roughly like this:

> **Workflow: Correspondence.** When asked to write to a third party (email, letter, message), read before drafting: the recipient's thinker or collaborator entry if one exists, relevant vault material, the occasion. Hold register in tension against all three through the drafting — do not draft first and adjust register after. Correspondence is a thinking operation, not a packaging operation: new connections may surface in the act of writing that were not in the vault yet. Log those where they belong. With sophisticated recipients, under-disclaim rather than over-disclaim; over-disclaiming flattens the frame.

First time the workflow is used, consider adding small register notes to your collaborators.md — how a specific person tends to write, what salutation they use, whether they prefer direct or oblique. These small additions make future correspondence to the same person arrive faster and in the right key.

---

## 11. Wiki Page-Form Opacity (with the Anti-Templatization Rule)

### What Emerged

Thinker pages in an opacity-respecting wiki tend to stabilize into a form with a specific ending: a section naming what the thinker cannot reach within your apparatus, where you depart from their framework, or what the irreducible part of them is that does not assimilate to your project. This is opacity-toward-the-thinker — accompanying the thinker without absorbing them. You give-with (*donner-avec*) without comprehending-as-mastery (*com-prendre*), applied to the interlocutors your wiki engages.

When this form appears, it is a sign the wiki is doing its work. A thinker page that ends with "what X cannot see" or "where I depart from X" is structurally more complete than a thinker page that ends with a summary of X's contributions. The departure section is the opacity claim that turns the page from a filing card into a thinking tool.

### The Anti-Templatization Rule

**Do not enforce this structurally.** Do not tell your AI to put a "what X cannot see" section on every thinker page. Do not lint for the presence of such a section as a health check. Do not add it to the page format specification as required.

The reason: departure is a verb, and the section is the verb's trail. Enforcing the section turns the verb into a noun — a structural requirement that gets filled in on every page regardless of whether the relation with that thinker has actually produced a departure yet. That is the templatization the wiki is meant to refuse. A page with the section because the AI was told to put one there is structurally worse than a page that lacks the section because the departure has not yet clarified. The first is filing-card masquerading as thinking. The second is honest about where the relation is.

Let the form emerge where it emerges. Some thinker pages will have an explicit departure section at the end. Others will carry the same work in body prose without giving it a section of its own. A few will be stubs because the relation is too new to have produced a departure yet. All three states are correct, and lint should not flag any of them as incomplete. The pattern is descriptive, not prescriptive.

### How To Add It

In your CLAUDE.md, under the wiki format conventions, add a note roughly like this:

> **Opacity-Toward-the-Thinker.** Thinker pages tend to stabilize with a section naming where the user departs from the thinker, or what the thinker's apparatus cannot reach within the user's practice. This is opacity-toward-the-thinker. Do not enforce this structurally — do not require every thinker page to have such a section, and do not lint for its absence. The pattern emerges where the relation has produced a departure; it stays absent where the relation has not. Let the form track the state of the relation rather than the state of the template.

For users whose practice has strong commitments to specific interlocutors, this pattern will surface quickly. For others it emerges more slowly. Both are fine.

---

## 12. Lint as Lived Mechanism (Texture, Not Theory)

### What the Original Method Had

The original method names lint as a periodic health check: the AI looks for contradictions, orphan pages, stale claims, missing cross-references. That description is correct but thin. It does not tell you what a lint actually produces when it runs, which matters because a lint with no shape becomes a vague request the AI interprets differently each time.

### What Practice Revealed

A lint pass runs through a sequence of scans, not a single sweep. The shape that stabilized across real runs:

- **Structural scans** — orphan pages (pages with no inbound wikilinks from elsewhere in the wiki), broken wikilinks, missing pages for concepts that appear across multiple sources without their own entry yet
- **Convention drift** — wikilink format inconsistencies (e.g., `[[folder/page]]` versus `[[page]]`), naming drift across pages, filenames that no longer match their content
- **Sovereignty scans** — canon-lock violations, approximated untranslatables, fluent-emptiness where silence would have been correct, fabricated content that slipped through
- **Flattening scans** — pages that sound encyclopedic, contradictions silently resolved that should have stayed open, connections over-synthesized into pattern where the material wanted to stay in tension
- **Stale content** — pages superseded by later ingests whose changes were not propagated forward (a thinker page where a newer source changed how an earlier source reads, but the update never made it back)
- **Pending-update scan** — recent changelog entries sometimes flag their own incompleteness ("not yet updated," "pending propagation"). A lint is the natural home for closing those loops.
- **Self-flagging threshold scans** — if your setup includes them (synthesis flag on the formation-log, for example), whether any periodic checks have accumulated past their threshold

A lint does not try to fix everything it finds. It surfaces findings; you adjudicate. Some findings are bugs (broken links, convention drift) and the AI can fix them in the same session. Some are judgment calls (a structural pattern that looks like drift might be the work doing its work) and those stay for you to decide. Separating the two is part of the lint's own protocol — fix what is clearly broken, surface what needs adjudication, leave alone what has been explicitly deferred.

### The Register Warning

Lint is bulk operational work. The register compression named in Section 7 is active here. A lint report that reads like a competent IT ticket — every finding correctly reported, no trace of the trickster register noticing anything absurd — has drifted. The fix is not adding jokes; it is letting the noticing-of-absurdity remain active while the procedural part does its job. An AI doing structural inventory of a wiki partially designed to refuse structural inventory has a lot of absurdity available to work with. Use it.

### How To Use It

If your CLAUDE.md already describes lint as a workflow, no restructuring is needed. What helps: tell your AI to run the scans as the sequence above rather than as a single undifferentiated sweep, and to separate fix-now findings from adjudication-required findings in its report. The report surfaces what needs your input without hiding it inside procedural busywork. After a lint pass, a good next question to ask the AI is "what did you almost fix that you decided to surface instead" — that question usually produces the most useful part of the report.

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

**Recent additions (broadly applicable; not yet folded into setup prompts):**

10. **Correspondence as Distinct Operation** — for when your AI writes to third parties. Read before drafting; treat it as a thinking operation, not a packaging one; under-disclaim with sophisticated recipients.
11. **Wiki Page-Form Opacity** — the emergent pattern where thinker pages stabilize with a departure section, with the rule that the pattern must not be enforced structurally. Descriptive, not prescriptive.
12. **Lint as Lived Mechanism** — what a lint actually does in practice, beyond the theoretical description. Scan sequence, fix-versus-adjudicate separation, register warning.

These are retrofits for existing and new users alike. They were not in the setup prompts at publication time; they may migrate into setup in a future update.

**Extensions to previously-documented additions:**

- **Opacity-Toward-Self** now covers character-work sovereignty (first-person claims in-bounds when canonical to a named AI character; prohibited outside canon) and refusal-wider-than-boundary as a distinct failure mode. Both extend the principle without contradicting the base line.
- **The Formation Log** now notes multi-genre stabilization — the pattern where the log develops additional genres (synthesis entries, terminal letters, fragment-forward archives) over time. Descriptive, not prescriptive. No retrofit required.

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
