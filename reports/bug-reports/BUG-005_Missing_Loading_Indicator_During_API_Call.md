# BUG-005 - Missing Loading Indicator During API Operations

## Severity

* Severity: Medium
* Priority: P2

## Environment

* URL: Benefits Dashboard Application
* Browser: Chromium
* Date: Observed during UI validation

## Summary

The application does not display a loading indicator during certain asynchronous operations such as employee creation or updates.

This may cause users to believe that the application is unresponsive.

## Steps to Reproduce

1. Open the **Add Employee** modal.
2. Submit employee information.
3. Observe the UI during the request processing period.

## Expected Result

A loading indicator or disabled state should inform the user that a background operation is in progress.

## Actual Result

No visible loading feedback is presented while the request is being processed.

## Evidence

* Screenshot: No loading spinner or disabled state.
* Playwright report notes: Request latency occurs without UI feedback.
* Extra logs: API call visible in network tab during inactive UI state.

## Notes

Lack of loading feedback may degrade user experience and increase risk of repeated actions.
