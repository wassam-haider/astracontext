# ASTRA Memory Logs

Two prompts for keeping a written trail of project progress across chat
sessions. Anyone on the team can run these in their own chat — each person
just needs the project context loaded (uploaded docs / project chat).

## Files

- `01_extract_project_memory.md` — full snapshot prompt. Run occasionally,
  whenever you want a complete current-state pull.
- `02_extract_session_summary.md` — end-of-session changelog prompt. Run
  every time you finish a work session.

## How it works

1. Open the prompt file, copy the text under "The Prompt."
2. Paste it into your ASTRA project chat.
3. The AI fills in the footer (date, your name, repo link, serial number)
   and outputs a `.txt` file.
4. Drop that `.txt` into the matching folder below and commit it.

## Repo structure

```
/memory/        <- outputs from Prompt 1 (full snapshots)
    ASTRA_memory_20260620_01.txt
    ASTRA_memory_20260625_02.txt
/sessions/       <- outputs from Prompt 2 (per-session changelogs)
    ASTRA_session_20260620_01.txt
    ASTRA_session_20260621_02.txt
```

## Serial numbers

Two independent counters — one for `/memory`, one for `/sessions`. Before
running a prompt, check the highest NN already in that folder and use the
next one. This is manual (look at the folder), not automatic — there's no
shared database doing this for you, just the file list in git.

## Limits, plainly

- These prompts only summarize what's *in that chat* — they can't pull from
  someone else's chat, another platform, or a different account.
- Treat the output as a working log, not a source of truth — always
  cross-check against the actual project files (literature review,
  proposal, etc.) for anything that matters academically.
- These files will contain team members' names and project details.
  Standard repo hygiene applies — don't put this in a public repo if that's
  a concern for your team.
