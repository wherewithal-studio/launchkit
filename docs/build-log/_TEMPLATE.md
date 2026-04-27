# YYYY-MM-DD — Dodek Build Log

> **How to use this template.** Copy to `docs/build-log/YYYY-MM-DD.md`. Fill in fields below; leave any section blank that doesn't apply (omit rather than write "N/A"). Skip days you didn't touch the venture. Each entry is ~5 minutes to write at end of session. Loop closes when the **Implications for PRD** section drives an edit to `docs/prd-pipeline.md` (or another PRD) — those edits get cross-referenced from the receiving PRD's **Drift Log** section.

---

## Appetite

**Today's box:** `<N>h on Dodek` (e.g. `2h on Dodek pipeline; rest split PAM/Totem`).
*Set this at the start of the session. If you blew past the box, note that in Implications — emergent overage is a real signal.*

---

## Started with

PRD baseline driving today's intent (what items from `prd-pipeline.md` Roadmap, `prd-field-ui.md`, or any other PRD did you sit down to advance):

- ...

*Or: "exploratory — no specific PRD intent" / "incident response — `<system> broke`" / "build cleanup — no new scope".*

---

## What happened

### Planned (advanced PRD intent) — `[Del]ivery` by default

Each line: `<one-line summary> — \`<sha>\``

- ...

### Emergent (not in PRD; discovered along the way)

Tag each item:
- **`[D]`** — *Discovery*: validating an unknown. Still figuring out if this is the right thing. OK to throw away.
- **`[Del]`** — *Delivery*: production commitment. We're going to ship and support this.

Distinguishing these two prevents a 1-day experiment from quietly becoming a multi-week obligation.

- **`[D]`** `<one-line>` — `<sha>` — *why emerged: ...*
- **`[Del]`** `<one-line>` — `<sha>`

### Investigations (no commit, but real work)

Debugging sessions, decisions, dead ends, design exploration that didn't produce code:

- ...

---

## Captured into

Where today's work landed:

- **code:** `<commit shas / PR links>`
- **specs/plans:** `<docs/superpowers/specs/...>`
- **CLAUDE.md learnings:** `<bullet titles added>`
- **artifacts:** `<screenshots, designs, scripts, /tmp logs worth keeping>`

---

## Implications for PRD

Each implication needs an **Outcome** line: did this feature actually move the user-outcome we cared about? Qualitative is fine. Forces honesty about output ≠ outcome.

### Roadmap edits

- **Add to roadmap:** `<item>` — *expected outcome:* `<what user gets if we ship this>`
- **Tick as done:** `<item>` — *outcome observed:* `<yes / no / partial — N min saved, qualitative win, etc.>`
- **Reorder/cut:** `<item>` — *why:* ...

### Mental Model shifts

When the PRD's stated mental model is now stale (the way the system actually works ≠ the way the PRD says it works):

- ...

### New open questions

- ...

### Non-goal drift

Things we considered today and explicitly chose **not** to do, OR things the PRD's Non-goals list claims we don't do but reality has crept past:

- ...

### Pivot signal

*Use sparingly — flag only when 3+ emergent items in recent build logs point to the same wrong assumption.*

- ...

---

## User signal this week

`[ ]` Self-only (founder dogfooding) &nbsp;&nbsp; `[ ]` Talked to DJ #N: `<name + insight>` &nbsp;&nbsp; `[ ]` Observation from own gig

*Weekly self-prompt — leave blank on days you didn't get external signal. If three consecutive build logs say "self-only", that's a flag: schedule a user conversation this week.*

---

## Backlog rot check (weekly — Mondays)

When you start the week, scan `prd-pipeline.md` Roadmap and `prd-field-ui.md` Roadmap for items added >14 days ago with no progress.

- **Aging items found:** `<list, or "none">`
- **Action:** `<archive / re-commit / break down / N/A>`
