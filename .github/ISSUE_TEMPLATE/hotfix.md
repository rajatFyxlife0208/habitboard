---
name: "🚨 Hotfix"
about: "Critical fix needed directly on production (main branch)"
title: "[HOTFIX] "
labels: "type:hotfix, status:todo, P0-Critical"
assignees: ""
---

## Critical Issue
<!-- What is broken in production RIGHT NOW? -->

## User Impact
<!-- How many users affected? What is broken for them? -->

## Root Cause
<!-- If known -->

## Fix Description
<!-- What needs to change to resolve this -->

## Repo Affected
<!-- habitboard-api / habitboard-web / both -->

## Rollback Plan
<!-- How to revert if the hotfix makes things worse -->

---
## Claude Code Instructions

⚠️ **HOTFIX — branch from `main`, NOT `develop`**

**Workflow:**
1. Read and understand the issue fully before touching any code
2. Invoke `security` agent first if it's auth/data related
3. Make the minimal change needed — do NOT refactor or clean up
4. Write a test that proves the fix works
5. Invoke `qa` agent to confirm no regressions
6. Run `/ship-it` to commit
7. Open PR: `hotfix/{issue-number}-{short-slug}` → `main`
8. After merging to `main`, immediately open a second PR: `main` → `develop` to backport

**Branch naming:** `hotfix/{issue-number}-{short-slug}`
**Source branch:** `main`
**Target branch:** `main` (then backport to `develop`)
**Merge strategy:** Merge commit (preserve history)
