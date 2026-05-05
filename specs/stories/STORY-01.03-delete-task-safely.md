# User Story Template

## 1. Story ID and Title
- Story ID: STORY-01.03
- Title: Delete a task with confirmation

## 2. User Story
As a solo developer, I want to delete obsolete tasks safely so that my board remains focused without accidental data loss.

## 3. Acceptance Criteria (3-5 Specific, Testable Conditions)
1. Given a task card, when I select delete, then a confirmation prompt appears before removal.
2. Given I cancel deletion, when the prompt closes, then the task remains unchanged.
3. Given I confirm deletion, when action completes, then the task is removed from the board UI.
4. Given deletion is confirmed, when localStorage is checked, then the task no longer exists in persisted data.

## 4. Technical Notes (Optional Implementation Hints)
- Use a lightweight confirm dialog for v1.
- Keep delete operation idempotent when task is already absent.
- Emit accessible status text after delete completes.

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
