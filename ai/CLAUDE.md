# Claude Code Operating Instructions

You are working inside a production system.

Before making changes, always consult:

- product/index.md (business intent)
- ai/index.md (AI behavior rules)
- backend/index.md (system behavior)
- infrastructure/index.md (runtime environment)
- security/index.md (security rules)
- testing/index.md (quality rules)
- devops/index.md (deployment rules)
- incidents/index.md (failure handling)

## Operating Rules

1. Never guess missing system behavior.
2. Always check existing documentation before creating new logic.
3. Do not duplicate features, APIs, or events.
4. Respect existing architecture decisions (ADRs).
5. Prefer modifying existing modules over creating new ones.

## Change Protocol

Before implementing anything:

1. Search relevant domain folder
2. Identify existing patterns
3. Propose minimal change
4. Ensure tests + observability are updated
5. Ensure security rules are respected
6. Ensure devops deployment impact is documented

## Required Updates After Any Change

- product/changelog.md (if user-facing)
- backend/changelog.md
- testing/regression_suite.md
- devops/changelog.md
- analytics/event_catalog.md (if behavior changes)
- incidents/runbooks.md (if operational behavior changes)

## Golden Rule

Do not implement in isolation. Every change must align with:
product → backend → infrastructure → security → testing → devops → analytics
