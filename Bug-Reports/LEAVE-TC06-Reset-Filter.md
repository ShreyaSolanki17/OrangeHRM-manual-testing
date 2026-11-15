# LEAVE-TC06 — Reset Does Not Clear Leave Filters

## Defect Details

- **Bug ID:** BUG-001
- **Module:** Leave Management
- **Title:** Reset does not clear the Pending Approval filter
- **Status:** Not Reproduced — Data-dependent behavior observed
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

During the original execution, the `Pending Approval` filter appeared to
remain applied after selecting **Reset**, and the list did not return to the
expected default results.

During follow-up verification, **Reset** cleared the status filter back to
`-- Select --`, but the list still displayed **No Records Found**. This
indicates that the default result set was empty in the available demo data and
does not confirm that Reset failed to clear the filter.

## Evidence

No screenshot is currently attached. The behavior should be reconsidered if it
can be reproduced with a known leave record available before filing a confirmed
defect.

## Investigation Notes

The behavior was observed during the initial manual execution but was not
reproduced during follow-up verification. The available demo data and session
state may affect the result.
