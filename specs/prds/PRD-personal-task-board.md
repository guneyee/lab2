# Product Requirements Document (PRD)

## 1. Overview

### Purpose
Deliver a lightweight personal task board that helps a solo developer plan, track, and complete work across 2-3 concurrent projects without using heavyweight project-management software.

### Problem Statement
The primary user currently spends 10-20 minutes per day reorganizing tasks across notes or bulky tools that are designed for teams, not individuals. Existing options introduce unnecessary setup and navigation overhead, causing slower daily planning and reduced execution focus. The product must reduce daily planning overhead to under 5 minutes while preserving visibility across all active work.

### Goals
- Enable the user to create, view, and manage tasks in a 3-column Kanban flow (To Do, In Progress, Done).
- Minimize friction in task updates via drag and drop and keyboard shortcuts.
- Persist board data locally so tasks remain available across refreshes and browser restarts.

## 2. User Personas

### Persona 1: Sam (Solo Full-Stack Developer)
- Role: Individual contributor shipping features across 2-3 personal/client projects.
- Needs: A fast, no-admin board to prioritize and move tasks through execution states.
- Pain Points: Team-focused tools feel heavy; task updates are too slow for rapid context switching.

### Persona 2: Alex (Indie Builder)
- Role: Single-person product builder balancing feature work, bug fixes, and experiments.
- Needs: Immediate clarity on what to start next and what is blocked or completed.
- Pain Points: Fragmented notes create duplicated or forgotten tasks; lacks a single execution view.

## 3. Use Cases

### Use Case 1: Capture and Prioritize Work
- Actor: Sam (Solo Full-Stack Developer)
- Trigger: Start of day planning or incoming new task.
- Main Flow:
  1. User opens the task board and reviews existing tasks by column.
  2. User adds a new task to To Do and assigns a project label.
  3. User reorders tasks in To Do to set execution priority.
- Expected Outcome: User has a prioritized, visible list of actionable tasks for all active projects.

### Use Case 2: Update Task Progress During Development
- Actor: Alex (Indie Builder)
- Trigger: Task status changes during coding session.
- Main Flow:
  1. User moves a task from To Do to In Progress via drag and drop or keyboard shortcut.
  2. User completes work and moves task to Done.
  3. System persists updated task state to localStorage immediately.
- Expected Outcome: Board accurately reflects real-time progress and remains consistent after refresh.

## 4. Functional Requirements

- FR-1: The system must render a Kanban board with exactly three columns: To Do, In Progress, and Done.
- FR-2: The system must allow users to create, edit, and delete tasks with at minimum a title and optional project label.
- FR-3: The system must support drag-and-drop movement of tasks within and across columns.
- FR-4: The system must provide keyboard shortcuts for core actions: create task, move selected task left/right, and mark selected task done.
- FR-5: The system must persist all task data and ordering in browser localStorage on every create/update/delete/move action.
- FR-6: On app load, the system must hydrate board state from localStorage and gracefully initialize empty state if no saved data exists.

## 5. Non-Functional Requirements

- NFR-1 (Performance): Initial board render must complete within 1.5 seconds on a typical developer laptop with up to 200 tasks stored.
- NFR-2 (Security): The app must not transmit task data over network calls; all task data remains local in the browser.
- NFR-3 (Reliability): Data persistence operations to localStorage must succeed for 99.9% of standard actions under normal browser conditions.
- NFR-4 (Scalability): The app must remain usable with up to 300 tasks total without noticeable interaction lag (>200 ms for move/create feedback).
- NFR-5 (Usability): Keyboard-accessible actions must cover at least 3 core flows (create, move, complete), and basic interactions should be learnable in under 10 minutes.

## 6. Success Metrics

- Metric 1: Daily Planning Time Reduction - Target: median planning time reduced from 10-20 minutes baseline to <=5 minutes within 2 weeks of use.
- Metric 2: Task Update Efficiency - Target: 90% of task state changes completed in <=3 seconds per action during normal use.
- Metric 3: Data Persistence Reliability - Target: >=99% of sessions retain board state accurately after refresh/reopen over a 30-day period.

## 7. Scope

### In Scope
- Single-user, frontend-only React + Vite application.
- 3-column Kanban workflow (To Do, In Progress, Done).
- Drag and drop interactions for task movement.
- Keyboard shortcuts for high-frequency actions.
- localStorage-based persistence and retrieval.

### Out of Scope
- Multi-user collaboration, shared boards, or real-time sync.
- Backend services, authentication, APIs, or cloud storage.
- Advanced analytics, reporting dashboards, or sprint planning modules.

## Assumptions
- The user operates primarily on modern desktop browsers.
- Typical active task count is under 100, with occasional spikes up to 300.
- Accessibility requirements include keyboard support but do not currently mandate full WCAG audit scope in this iteration.

## Open Questions
- Which exact keyboard shortcut mappings should be default (for example, Ctrl+N for new task, Ctrl+Arrow for movement)?
- Should project labels be free text or constrained to a predefined project list?
- Is task due date support needed in v1 or deferred to a future iteration?
