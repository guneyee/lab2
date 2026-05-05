# User Story Template

## 1. Story ID and Title
- Story ID: STORY-01.02
- Title: Edit task title and project label

## 2. User Story
As a solo developer, I want to edit a task's title and project label so that my board stays accurate as priorities evolve.

## 3. Acceptance Criteria (3-5 Specific, Testable Conditions)
1. Given an existing task, when I enter edit mode and update the title, then the new title is shown on save.
2. Given an existing task, when I update the project label, then the new label appears on the card.
3. Given I attempt to save an empty title, when validation runs, then changes are rejected and the prior title remains.
4. Given I save valid edits, when the page refreshes, then updated values remain visible.

## 4. Technical Notes (Optional Implementation Hints)
- Reuse create-form validation logic for edits.
- Persist edits using immutable update by task ID.
- Consider inline edit mode for minimal interaction cost.

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
