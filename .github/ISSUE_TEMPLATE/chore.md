---
name: "🔩 Chore"
about: "Maintenance tasks, dependency updates, config changes, CI/CD"
title: "[CHORE] "
labels: "type:chore, status:todo"
assignees: ""
---

## Task Description
<!-- What maintenance work needs to be done? -->

## Why Now
<!-- What triggered this? (security advisory, outdated dep, broken CI) -->

## Repo Affected
<!-- habitboard-api / habitboard-web / both / habitboard (central) -->

**Priority:** <!-- P1-High / P2-Medium / P3-Low -->
**Agents Required:** <!-- devops / security / qa -->

## Checklist
- [ ]
- [ ]
- [ ]

---
## Claude Code Instructions

**Workflow:**
1. Read all config files related to this chore before making changes
2. Invoke `devops` agent if this touches Docker, CI/CD, or infrastructure
3. Invoke `security` agent if this touches dependencies or env vars
4. Make changes carefully — chores often have hidden blast radius
5. Run tests after changes: `npm test`
6. Run `/ship-it` to commit
7. Open PR: `chore/{issue-number}-{short-slug}` → `develop`

**Branch naming:** `chore/{issue-number}-{short-slug}`
**Target branch:** `develop`
**Merge strategy:** Squash and merge
