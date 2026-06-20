# ASTRA Memory Extraction — Prompt 2: End-of-Session Summary

**When to use:** Run this at the end of any work session, right before you
close the chat.

**Where to run it:** Same chat you just worked in — it needs the
conversation history to summarize.

---

## The Prompt (copy everything below the line)

---

This work session is ending. Summarize everything accomplished in THIS
chat session only (not the whole project history — just today). Output a
single concise document, plain language, non-technical where possible:

1. **Header** — date, time, your name, which AI tool/chat this is.
2. **Worked On Today** — 3-6 bullets max, what was actually done.
3. **Decisions Made** — any choices locked in this session, one line each.
4. **Outputs Produced** — files, code, diagrams, or documents created or
   changed today, named specifically.
5. **Still Open** — anything started but not finished, or anything that
   came up but wasn't resolved.
6. **For Next Session** — one or two lines on where to pick up.

Keep it short — this is a changelog entry, not a report. If nothing
substantial happened this session, say so in one line instead of padding.

End with this exact footer block, filled in:

```
---
File: ASTRA_session_[YYYYMMDD]_[NN].txt
Generated: [date] [time, with timezone]
By: [your name]
Repo: [paste your GitHub repo URL here]
Serial: [NN — see numbering rule below]
---
```

**Serial numbering rule:** NN is a two-digit counter, starting at 01,
separate from the memory-export counter in Prompt 1. Check the repo's
`/sessions` folder (or wherever these are kept) for the highest NN used and
increment from there. If unsure, ask before finalizing.

Save the output as a `.txt` file using the exact filename from the footer.

---
