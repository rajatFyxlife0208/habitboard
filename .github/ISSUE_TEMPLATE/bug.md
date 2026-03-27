---
name: "🐛 Bug"
about: "Something is broken or behaving incorrectly"
title: "[BUG] "
labels: "type:bug, status:todo"
assignees: ""
---

## Bug Description
<!-- Clear description of what is broken -->

## Steps to Reproduce
1.
2.
3.

## Expected Behavior
<!-- What should happen -->

## Actual Behavior
<!-- What actually happens -->

## Environment
- **Repo:** <!-- habitboard-api / habitboard-web -->
- **Branch:**
- **Node version:**
- **Error logs:** <!-- paste relevant error output -->

## Priority
<!-- P0-Critical (prod down) / P1-High (major feature broken) / P2-Medium / P3-Low -->

## Agents Required
<!-- security / qa / architect -->

---
## Claude Code Instructions

**Workflow:**
1. Read the error logs and reproduce the bug locally
2. Identify root cause — read all affected files before touching anything
3. Invoke `security` agent if the bug is auth/data related
4. Write a failing test that reproduces the bug FIRST
5. Fix the bug
6. Confirm the test now passes
7. Invoke `qa` agent to check for related edge cases
8. Run `/ship-it` to commit
9. Open PR: `fix/{issue-number}-{short-slug}` → `develop`
10. Link PR to this issue

**Branch naming:** `fix/{issue-number}-{short-slug}`
**Target branch:** `develop`
**Merge strategy:** Squash and merge
