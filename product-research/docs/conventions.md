# UX Research Conventions

## IDs

- **Interviews**: `INT-YYYY-NNN`
  - Example: `INT-2025-001`
- **Requirements**: `REQ-NNN`
  - Example: `REQ-017`
- **Features** (if tracked): `FEAT-NNN` or link to Jira/GitHub issues.

## File locations

- Interviews: `ux-research/interviews/`
- Requirements: `ux-research/requirements/`
- Synthesis docs: `ux-research/synthesis/`

## Linking

- Each **interview** file has `interview_id` in front-matter.
- Each **requirement** file has:
  - `requirement_id`
  - `related_interviews: [INT-2025-001, INT-2025-004]`
  - optional: `related_features: [FEAT-023]`
