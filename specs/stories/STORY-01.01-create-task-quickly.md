# User Story Template

## 1. Story ID and Title
- Story ID: STORY-01.01
- Title: Create a task in To Do quickly

## 2. User Story
As a solo developer, I want to create a new task in the To Do column so that I can capture work immediately when it appears.

## 3. Acceptance Criteria (3-5 Specific, Testable Conditions)
1. Given the board is loaded, when I submit a valid task title, then a new task appears at the top of To Do.
2. Given I submit an empty title, when validation runs, then the task is not created and an inline error is shown.
3. Given I create a task with a project label, when saved, then the label is displayed on the task card.
4. Given a task is created, when localStorage is inspected, then the new task is persisted with a unique ID.

## 4. Technical Notes (Optional Implementation Hints)
- Use a controlled input form with required title validation.
- Generate deterministic IDs (for example via timestamp + random suffix).
- Write localStorage update through a shared persistence utility.

## 5. Estimation
- Estimate Type: DAYS
- Estimate Value: 1
- Confidence: HIGH

## 6. INVEST Validation
- Independent: Pass
- Negotiable: Pass
- Valuable: Pass
- Estimable: Pass
- Small: Pass
- Testable: Pass
