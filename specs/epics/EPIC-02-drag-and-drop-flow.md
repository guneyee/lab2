# Epic Template

## 1. Epic Title
Drag-and-Drop Workflow Across Columns

## 2. Description (2-3 sentences)
Enable intuitive drag-and-drop movement of tasks within and across To Do, In Progress, and Done columns. Preserve task ordering and immediately persist move operations so users can rapidly update status during coding sessions. This epic delivers the core interaction flow for reducing task update friction.

## 3. Primary Persona (Who Benefits Most)
- Persona: Alex (Indie Builder)
- Why this persona: Alex frequently switches contexts and needs fast visual state changes without editing forms.

## 4. Success Criteria (Measurable Outcomes)
- Move Interaction Speed - Target: 90% of task moves completed in <=3 seconds.
- Order Consistency - Target: 100% of successful moves preserve intended target column and relative order.
- PRD Metric Mapping - Target: Supports Metric 2 (Task Update Efficiency).

## 5. Scope/Complexity (S/M/L Estimate)
- Size Estimate: M
- Scope Notes: Includes drag sensors, drop zones, move/reorder logic, persistence on move, and basic keyboard fallback messaging; excludes advanced animations.

## 6. Dependencies (What Must Exist First)
- EPIC-01 core board and persisted task model.
- Stable task IDs and deterministic ordering model.
- Column components capable of receiving drop events.

## 7. User Stories Placeholder (To Be Filled Later)
- Story 1: [STORY-02.01-drag-task-between-columns]
- Story 2: [STORY-02.02-reorder-tasks-within-column]
- Story 3: [STORY-02.03-persist-drop-position-and-order]
