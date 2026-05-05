# agents.md

## 1. Tech Stack
- Frontend: React 18 + Vite
- Language: TypeScript
- Data Persistence: browser localStorage
- Backend: none (do not introduce server/API/database layers)

## 2. Specification Structure
Store product and planning specs under `specs/`:
- `specs/prds/` -> Product Requirements Documents
- `specs/epics/` -> Epic definitions derived from PRDs
- `specs/stories/` -> User stories derived from epics
- `specs/templates/` -> Reusable markdown templates

Copilot prompt files live in:
- `.github/prompts/` -> reusable `.prompt.md` files

## 3. Naming Conventions
Use lowercase kebab-case for all spec files.

Recommended patterns:
- PRD files: `prd-<feature-name>.md`
- Epic files: `epic-<feature-name>.md`
- Story files: `story-<feature-name>-<short-scope>.md`
- Template files: `*-template.md`
- Prompt files: `<prompt-name>.prompt.md`

Examples:
- `prd-task-board-core.md`
- `epic-drag-and-drop.md`
- `story-create-task-inline.md`

## 4. File Organization
Project root conventions:
- Keep app source code under `src/` (when initialized).
- Keep specifications under `specs/` only.
- Keep Copilot reusable prompts under `.github/prompts/` only.
- Keep generated outputs and planning artifacts inside `specs/`.

Assistant operating rules:
- Follow existing templates in `specs/templates/` before creating new spec docs.
- Maintain traceability: stories should reference epic IDs; epics should reference PRD goals/requirements.
- Do not add backend-related folders or dependencies.
- Prefer small, focused files over large mixed documents.
