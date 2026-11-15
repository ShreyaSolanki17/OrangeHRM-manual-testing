# LEAVE-TC06 — Reset Does Not Clear Leave Filters

## Defect Details

- **Bug ID:** BUG-001
- **Module:** Leave Management
- **Title:** Reset does not clear the Pending Approval filter
- **Status:** Open — Reproduction confirmation required
- **Severity:** Medium
- **Priority:** Medium
- **Related test case:** LEAVE-TC06
- **Environment:** OrangeHRM Demo, Google Chrome on macOS

## Preconditions

- User is authenticated.
- Leave records are available.
- The Leave List page is accessible.

## Steps to Reproduce

1. Open **Leave → Leave List**.
2. Select `Pending Approval` in the status filter.
3. Select **Search**.
4. Confirm that filtered leave records are displayed.
5. Select **Reset**.

## Expected Result

The status filter and other search criteria are cleared, and the default
unfiltered leave list is restored.

## Actual Result

The `Pending Approval` filter remained applied after selecting **Reset**, and
the leave list did not return to the default unfiltered state.

## Evidence

No screenshot is currently attached. Evidence should be added if the behavior
is reproduced.

## Investigation Notes

The behavior was observed during manual execution of `LEAVE-TC06`. It should
be reproduced in the demo environment before final defect closure or severity
confirmation because the shared demo data and session state may change.
