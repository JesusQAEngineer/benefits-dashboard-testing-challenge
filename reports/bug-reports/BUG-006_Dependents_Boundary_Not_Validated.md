# BUG-006 - Dependents Boundary Validation Not Strictly Enforced

## Severity

* Severity: Medium
* Priority: P2

## Environment

* URL: Benefits Dashboard Application
* Browser: Chromium
* Date: Observed during boundary testing scenarios

## Summary

The system does not clearly enforce strict boundary validation for the **maximum allowed number of dependents**.

This could lead to incorrect financial calculations if invalid values are processed.

## Steps to Reproduce

1. Open the **Add Employee** modal.
2. Enter a dependents value above the expected maximum (32).
3. Submit the form.

## Expected Result

The system should reject values above the maximum allowed boundary.

Validation should occur either:

* at the UI layer
* or via backend validation.

## Actual Result

The UI allows entry of large numeric values without visible boundary restriction.

## Evidence

* Screenshot: High dependent values allowed in input field.
* Playwright report notes: Boundary validation not enforced in UI.
* Extra logs: Financial calculations rely on user input without strict limits.

## Notes

While backend validation may still exist, the UI does not clearly enforce this boundary, creating potential risk for incorrect financial computations.
