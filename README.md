# Task Board Lab

AI-as-Copilot workflow for creating a spec toolkit, then using that toolkit to generate project specifications.

## What This Repository Contains
- AI-generated templates for PRD, Epic, and User Story authoring.
- AI-generated reusable Copilot prompt files for PRD, Epic, and Story decomposition.
- Generated specifications for the Personal Task Board project.
- Project-level assistant conventions in `agents.md`.

## Project Context
- Product: Personal Task Board
- Stack target: React 18 + Vite + TypeScript
- Persistence: browser localStorage
- Backend: none
- Source brief: `project-brief.md`

## Directory Map
- `.github/prompts/`: Reusable Copilot prompt files (`*.prompt.md`)
- `specs/templates/`: Reusable markdown templates
- `specs/prds/`: Generated PRD documents
- `specs/epics/`: Generated epic documents
- `specs/stories/`: Generated user story documents
- `agents.md`: Project conventions and constraints
- `project-brief.md`: Input brief used to generate specs

## Prompt Library
Run these in GitHub Copilot Chat:
1. `/generate-prd`
2. `/decompose-epics`
3. `/decompose-stories`

Prompt files:
- `.github/prompts/generate-prd.prompt.md`
- `.github/prompts/decompose-epics.prompt.md`
- `.github/prompts/decompose-stories.prompt.md`

## End-to-End Workflow
1. Create templates in `specs/templates/`.
2. Create reusable prompts in `.github/prompts/`.
3. Generate PRD from `project-brief.md`.
4. Decompose PRD into 3-4 epics.
5. Decompose the most critical epic into 5-7 stories.
6. Validate quality (measurable goals, clear scope, INVEST-ready stories).

## Generated Outputs In This Repo
- PRD:
   - `specs/prds/PRD-personal-task-board.md`
- Epics:
   - `specs/epics/EPIC-01-core-board-and-persistence.md`
   - `specs/epics/EPIC-02-drag-and-drop-flow.md`
   - `specs/epics/EPIC-03-keyboard-productivity-controls.md`
   - `specs/epics/EPIC-04-multi-project-prioritization-view.md`
- Stories:
   - `specs/stories/STORY-01.01-create-task-quickly.md`
   - `specs/stories/STORY-01.02-edit-task-details.md`
   - `specs/stories/STORY-01.03-delete-task-safely.md`
   - `specs/stories/STORY-01.04-persist-task-changes.md`
   - `specs/stories/STORY-01.05-restore-board-on-load.md`
   - `specs/stories/STORY-01.06-handle-empty-and-corrupt-state.md`

## Quality Rules Used
- Requirements are specific and testable.
- Metrics are measurable and time-bounded where possible.
- Scope explicitly separates in-scope and out-of-scope.
- Story acceptance criteria use Given/When/Then.
- Story sizing targets 1-3 day scope and INVEST alignment.

## Team Usage Notes
- Keep file naming in lowercase kebab-case where defined in `agents.md`.
- Create new specs with existing templates before inventing new formats.
- Keep traceability: PRD -> Epics -> Stories.
- Do not introduce backend assumptions for this project.
