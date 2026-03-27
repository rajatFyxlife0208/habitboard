---
name: "✨ Feature"
about: "New feature or enhancement"
title: "[FEATURE] "
labels: "type:feature, status:todo"
assignees: ""
---

## Summary
<!-- One sentence: what does this feature do for the user? -->

## Problem It Solves
<!-- What pain point or gap does this address? -->

## Acceptance Criteria
<!-- Checkboxes that define "done". Be specific. -->
- [ ]
- [ ]
- [ ]

## Scope
**Repos affected:** <!-- [ ] habitboard-api  [ ] habitboard-web  [ ] both -->
**Priority:** <!-- P0-Critical / P1-High / P2-Medium / P3-Low -->
**Agents required:** <!-- product-manager / architect / security / qa / devops -->

## Technical Notes
<!-- Any constraints, existing patterns to follow, or decisions already made -->

## Out of Scope
<!-- What this ticket explicitly does NOT include -->

---
## Claude Code Instructions
<!-- These instructions tell Claude exactly how to execute this ticket -->

**Workflow:**
1. Run `/new-feature "<title>"` to trigger the product-manager → architect pipeline
2. Wait for spec confirmation before writing any code
3. Implement following the architect's plan exactly
4. Invoke `security` agent after implementation
5. Invoke `qa` agent to write and run tests
6. Run `/ship-it` to commit
7. Open PR: `feature/{issue-number}-{slug}` → `develop`
8. Link PR to this issue

**Branch naming:** `feature/{issue-number}-{short-slug}`
**Target branch:** `develop`
**Merge strategy:** Squash and merge
