---
name: "♻️ Refactor"
about: "Code quality improvement with no behavior change"
title: "[REFACTOR] "
labels: "type:refactor, status:todo"
assignees: ""
---

## What to Refactor
<!-- Which files, modules, or patterns need improvement -->

## Why
<!-- What problem does the current code have? (readability, performance, duplication) -->

## Proposed Approach
<!-- How should it look after the refactor? -->

## Repo Affected
<!-- habitboard-api / habitboard-web / both -->

**Priority:** <!-- P2-Medium / P3-Low -->
**Agents Required:** <!-- architect / qa / security -->

## Definition of Done
- [ ] Behavior is identical before and after
- [ ] Existing tests still pass
- [ ] Code is measurably simpler or faster

---
## Claude Code Instructions

**Workflow:**
1. Run existing tests first — establish the baseline: `npm test`
2. Invoke `architect` agent to validate the approach before touching code
3. Refactor incrementally — one file or function at a time
4. Run tests after each change to catch regressions immediately
5. Do NOT change behavior — if you find a bug, open a separate fix ticket
6. Invoke `qa` agent to verify test coverage hasn't dropped
7. Run `/ship-it` to commit
8. Open PR: `refactor/{issue-number}-{short-slug}` → `develop`

**Branch naming:** `refactor/{issue-number}-{short-slug}`
**Target branch:** `develop`
**Merge strategy:** Squash and merge
