# Epic Template

## 1. Epic Title
Keyboard Productivity Controls

## 2. Description (2-3 sentences)
Provide keyboard shortcuts for high-frequency actions: create task, move task left/right, and mark task done. Ensure discoverability and predictable behavior so power users can operate the board without constant pointer use. This epic increases throughput and supports usability goals for daily workflows.

## 3. Primary Persona (Who Benefits Most)
- Persona: Sam (Solo Full-Stack Developer)
- Why this persona: Sam benefits from reduced context-switch friction and faster control during focused coding sessions.

## 4. Success Criteria (Measurable Outcomes)
- Shortcut Coverage - Target: 3 core flows supported (create, move, complete).
- Shortcut Adoption - Target: >=40% of task transitions performed via keyboard by end of week 2.
- PRD Metric Mapping - Target: Supports Metric 2 (Task Update Efficiency <=3 seconds in 90% of changes).

## 5. Scope/Complexity (S/M/L Estimate)
- Size Estimate: M
- Scope Notes: Includes keybinding map, focused-task model, shortcut handlers, and shortcut help text; excludes full remappable hotkeys in v1.

## 6. Dependencies (What Must Exist First)
- EPIC-01 task selection state and CRUD actions.
- EPIC-02 move logic API for programmatic left/right transitions.
- Basic focus management strategy across task cards.

## 7. User Stories Placeholder (To Be Filled Later)
- Story 1: [STORY-03.01-create-task-with-keyboard-shortcut]
- Story 2: [STORY-03.02-move-selected-task-with-keyboard]
- Story 3: [STORY-03.03-mark-task-done-with-keyboard]
