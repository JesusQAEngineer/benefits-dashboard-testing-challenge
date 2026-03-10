# BUG-002 - Employee Modal Remains Open After Submission

## Severity
- Severity: Medium
- Priority: P2

## Environment
- URL: Benefits Dashboard application
- Browser: Chromium (observed during Playwright-driven execution)
- Date: Add execution date here

## Summary
After submitting a new employee, the employee modal sometimes remains open instead of closing and returning the user to the updated dashboard state.

The employee record may still be successfully persisted, but the UI does not always reflect completion of the action correctly.

## Steps to Reproduce
1. Open the Benefits Dashboard application.
2. Navigate to the employee creation flow.
3. Open the Add Employee modal.
4. Complete the employee form with valid data.
5. Submit the form.
6. Observe the modal behavior after submission.

## Expected Result
After successful submission, the modal should close automatically and the dashboard should return to its normal state with the newly created employee visible.

## Actual Result
The modal sometimes remains open after submission, even when the employee record has already been created successfully.

## Evidence
- Screenshot: Add screenshot path showing modal remaining open after submit
- Video: Add execution video if available
- Playwright report notes: UI BUG-002 validation identified modal persistence after submit
- Any extra logs: API validation for `GET /api/Employees/{id}` confirmed that the employee exists despite the modal remaining visible

## Notes
This issue may confuse users into thinking submission failed, which increases the risk of repeated clicks or duplicate attempts.

Cross-validation with the API suggests the persistence layer succeeds, while the frontend completion state is not updated reliably.
