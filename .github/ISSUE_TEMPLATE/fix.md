---
name: "🔧 Fix"
about: "Non-critical fix for a known issue (goes through develop)"
title: "[FIX] "
labels: "type:fix, status:todo"
assignees: ""
---

## What Needs Fixing
<!-- Describe the issue clearly -->

## Current Behavior
<!-- What is happening now -->

## Desired Behavior
<!-- What should happen after the fix -->

## Repo Affected
<!-- habitboard-api / habitboard-web / both -->

**Priority:** <!-- P1-High / P2-Medium / P3-Low -->
**Agents Required:** <!-- qa / security / architect -->

---
## Claude Code Instructions

**Workflow:**
1. Reproduce the issue locally first
2. Read all files related to the fix before making changes
3. Write a failing test that captures the broken behavior
4. Implement the fix — minimal change, no scope creep
5. Confirm test passes
6. Invoke `qa` agent to check for regressions
7. Run `/ship-it` to commit
8. Open PR: `fix/{issue-number}-{short-slug}` → `develop`

**Branch naming:** `fix/{issue-number}-{short-slug}`
**Target branch:** `develop`
**Merge strategy:** Squash and merge
