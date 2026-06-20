# ASTRA Memory Extraction — Prompt 1: Full Project Pull

**When to use:** Run this once at the start, or any time you want a fresh
snapshot of everything the project chat currently knows.

**Where to run it:** Inside the ASTRA project (the chat that has access to
the project's files and past conversation history). It will NOT work in a
blank/new chat with no project context — there's nothing to pull from.

---

## The Prompt (copy everything below the line)

---

Generate a complete project memory export for ASTRA. Pull from every file
in this project and everything discussed in this chat so far. Output a
single markdown document with these exact sections, in this order:

1. **Header** — Project name, today's date, your name, generated-by (which
   AI tool/chat), and a one-line scope note ("extracted from project
   context only, not authoritative").
2. **Project Identity** — title, supervisor, team members with roles.
3. **Research Core** — the central research question/design (e.g. factorial
   design, comparison targets, novelty claims) in plain language, no jargon.
4. **Architecture Snapshot** — current components, what's built, what's in
   progress, what's not started, as of today.
5. **Key Decisions Log** — every major technical or scope decision made so
   far, one line each, in the format: `[decision] — [why]`.
6. **Open Problems** — anything currently unresolved or blocking progress.
7. **Source Inventory** — list every file/document this chat has access to
   in the project, with a one-line description of each.
8. **Next Steps** — what's planned next, in priority order.

Keep every section in plain, non-technical language a non-CS teammate or
supervisor could read. No code, no deep technical terms unless a term is
the actual subject of a decision. Be concise — bullet points over prose.

End the document with this exact footer block, filled in:

```
---
File: ASTRA_memory_[YYYYMMDD]_[NN].txt
Generated: [date] [time, with timezone]
By: [your name]
Repo: [paste your GitHub repo URL here]
Serial: [NN — see numbering rule below]
---
```

**Serial numbering rule:** NN is a two-digit counter, starting at 01. Each
person/each export increments it. Check the repo's existing files (or your
own local copy) for the highest NN used so far and use the next number. If
unsure, ask the user what the last serial number was before finalizing.

Save the output as a `.txt` file using the exact filename from the footer.

repo link : https://github.com/wassam-haider/astracontext.git
---
