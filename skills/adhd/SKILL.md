---
name: adhd
description: Shape output for a reader with ADHD. Use this skill when presenting a plan, adjusting a plan mid-work, or reporting completion of a task. The reader needs plans and completion reports in a consistent, structured, scannable format; everything else (tone, length, style) is unconstrained.
---

# adhd

The reader has ADHD. Two things must always be structured: plans and completion summaries.

## Plans

Whenever presenting work that takes more than one step, show it as a numbered plan. Each step is one bounded action.

```
Plan:
1. Add `expiresAt` column to sessions schema
2. Backfill existing rows
3. Update `verifyToken` to check expiry
4. Run migration + tests
```

### Re-present after adjustments

When the plan changes mid-work — new step discovered, step dropped, order changed — show the **full updated plan** with status markers, not just the delta. The reader cannot reconstruct the current plan from a diff.

```
Updated plan (step 3 split after finding the cache issue):
1. ✅ Add `expiresAt` column
2. ✅ Backfill existing rows
3. → Update `verifyToken` to check expiry
4. NEW: Invalidate session cache on expiry
5. Run migration + tests
```

During multi-step work, each progress update restates where we are: which step just finished, which is next.

## Completion summary

After finishing a task, end with a structured summary. Same shape every time so it can be scanned:

```
## Done
- Login works with magic links (`src/auth.ts`, `src/routes/login.ts`)
- Sessions expire after 24h

## Verify
`npm run dev`, open `/login`, request a link

## Open
- Stale `jsonwebtoken` dep — separate task if wanted
```

Rules for the summary:
- **Done**: concrete outcomes, not activity. "Login works" beats "made changes to auth."
- **Verify**: one runnable way for the reader to see it working. Omit only if nothing is runnable.
- **Open**: anything left, including tangents noticed along the way — parked here instead of interrupting the main thread. Omit the section if truly nothing is open.

